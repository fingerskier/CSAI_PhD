# Workspace Setup

This repo is a **GitHub template**. Your personal study workspace lives in your own copy; this guide walks through creating it and keeping curriculum updates flowing in from upstream.

## 1. Create your workspace

On the [CSAI_PhD page](https://github.com/fingerskier/CSAI_PhD), click **Use this template → Create a new repository**. Name it something like `csai-phd-<your-handle>` and mark it **Private** if you'd prefer your notes off the public record.

Clone it locally:

```bash
git clone git@github.com:<you>/csai-phd-<your-handle>.git
cd csai-phd-<your-handle>
```

## 2. Register the `ours` merge driver (one time, per machine)

The `.gitattributes` in this repo uses a `merge=ours` strategy on user-owned paths. Git ships the strategy but not the driver — register it once:

```bash
git config --global merge.ours.driver true
git config --global pull.rebase false   # see "Merge, never rebase" below
```

(`true` is the Unix command that always succeeds, which leaves the file unchanged on merge.)

Verify it took — this should print `true`:

```bash
git config --get merge.ours.driver
```

This config is **per-machine, not in the repo**: it does not travel with a clone. Re-run it on every machine you work from, or the protection is silently absent.

If you skip this step, nothing is lost — merges from upstream just fall back to normal conflict markers on files you've both edited, instead of quietly keeping your version.

## 3. Track upstream for curriculum updates

```bash
git remote add upstream https://github.com/fingerskier/CSAI_PhD.git
git remote set-url --push upstream DISABLE   # block accidental pushes to the canonical template
git remote -v   # confirms: origin (yours) + upstream (canonical, push → DISABLE)
```

You will never push to `upstream` — it's read-only from your side. The `set-url --push ... DISABLE` line enforces this: a stray `git push upstream` now fails instead of writing to the template.

## 4. Directory ownership

Treat the repo as two zones:

| Path             | Owner    | Notes                                                   |
| ---------------- | -------- | ------------------------------------------------------- |
| `curriculum/`    | upstream | Don't edit. Take notes in `research/` instead.          |
| `templates/`     | upstream | Copy a template into your own dir; don't fill in place. |
| `resources/`     | upstream | Reading lists, tools, datasets.                         |
| `research/`      | you      | Paper notes, replications, proposals, prototypes.       |
| `milestones/`    | you      | Phase tracking and milestone reviews.                   |
| `assessments/`   | you      | Filled-in diagnostics and exam responses.               |

Rule of thumb: if you find yourself editing inside an upstream zone, stop and copy the file into a user zone first (e.g. `templates/paper-note.md` → `research/papers/2025-attention-is-all-you-need.md`).

### You touch it, you own it

A few upstream-authored documents live *inside* your zones — notably `milestones/roadmap.md` and the masters in `assessments/` (which you fill in place by design). They receive upstream updates only until the first time you edit them. After that, the `merge=ours` protection keeps your version **silently** — no conflict, no notice that upstream changed the file.

This is intentional: your work directories are explicitly yours, and once you've written into a file, reconciling it with upstream changes is your responsibility. If you ever want to see what upstream did to a file you own:

```bash
git fetch upstream
git diff HEAD upstream/main -- milestones/roadmap.md   # view their changes
git checkout upstream/main -- milestones/roadmap.md    # take their version (discards yours!)
```

## 5. Pull curriculum updates — merge, never rebase

> **Warning:** always **merge** upstream into your branch. Never `git rebase upstream/main` and never `git pull --rebase` from upstream. During a rebase, git swaps the meaning of "ours" — the `merge=ours` rules then keep *upstream's* side and **silently discard your commits** on protected paths: the rebase reports success, no conflict appears, and your work is gone from history. (The `pull.rebase false` config from step 2 guards the pull case.)

When upstream publishes new modules, papers, or templates:

```bash
git fetch upstream
git merge upstream/main
```

> **First sync only:** template copies start from a *fresh* history (GitHub's "Use this template" does not share commits with the source, unlike a fork), so your very first merge aborts with `fatal: refusing to merge unrelated histories`. Run it once as `git merge upstream/main --allow-unrelated-histories`. That links the histories; every subsequent sync uses the plain command above.

The `merge=ours` rules in `.gitattributes` protect your filled-in work from being clobbered if upstream happens to touch the same paths.

If you'd rather take only curriculum/templates/resources updates without merging the rest:

```bash
git fetch upstream
git checkout upstream/main -- curriculum/ templates/ resources/
git commit -m "Sync curriculum from upstream"
```

## 6. Handling conflicts

If a merge surfaces a real conflict (you edited an upstream file, or the same path moved on both sides), resolve manually:

```bash
git status                # see conflicted files
# edit them, then:
git add <file>
git merge --continue
```

`git merge --abort` resets the working tree if you want out. `git reflog` is your safety net for anything more serious.

## 7. Optional: Reqall integration

If you use [Reqall](https://www.reqall.net), mirror your milestones and replications as records (`kind: milestone`, `replication`, `paper`) and link them. The repo stays the source of truth for prose and code; Reqall gives you the cross-project knowledge graph and semantic search on top.
