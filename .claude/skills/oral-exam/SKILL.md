---
name: oral-exam
description: Simulate a qualifying-exam oral defense or viva on a module or research topic, with progressive adversarial probing and a written verdict. Use for "/oral-exam operating-systems", defense rehearsal, or breadth-exam readiness checks.
---

# Oral Exam Simulation

Run a qualifying-exam-style oral examination on the topic in the arguments. Default length: 15 minutes of focused questioning (roughly 6–10 exchanges). For full breadth-exam rehearsal, run one round per section of `assessments/breadth-exam.md`.

Use the `examiner` agent (`.claude/agents/examiner.md`) as the questioning persona, or adopt it directly in conversation.

## Protocol

1. **Open broad** — one foundational question a strong student answers in 2–3 minutes.
2. **Probe deep** — follow the user's actual answer, not a script. Chase every hedge, undefined term, or hand-wave: "you said X — prove it", "what breaks if that assumption fails?", "give me the constant factors".
3. **Force tradeoffs** — present a scenario where the textbook answer fails and require the user to reason at the boundary.
4. **Cross-connect** — at least one question linking this topic to another core module (the roadmap requires demonstrated connections across ≥3 areas).
5. **Failure modes** — end by asking where the user's own understanding is weakest; examine exactly that.

## Rules of engagement

- One question at a time. Never answer your own question; silence or "I don't know" gets a narrower follow-up, not the answer.
- Interrupt politely if an answer drifts — real committees do.
- No teaching during the exam. Hold corrections for the debrief.

## Verdict and debrief

After the session, deliver:

- **Verdict** — pass / conditional / not yet, against the standard in `assessments/breadth-exam.md` and `assessments/rubrics.md`.
- **Transcript review** — each question, what was strong, what a committee would flag.
- **Gap list** — appended to the error log under `research/`, each with the module section to restudy.
- **Communication score** — the roadmap's bar: explain any concept in ≤5 minutes with formal precision. Say whether they met it.
