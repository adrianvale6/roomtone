# roomtone
A harness for long running conversations between language models. 


Python, agents, evaluation. Mostly interested in what language models do over
long horizons — the failure modes that only show up at turn 200, not turn 5.
Current work
roomtone — a harness for
long-running conversations between language models. Turn budgets, an observer
pass that scores divergence, a full SQLite archive, live transcript streaming.
I built it because most multi-agent demos run for six turns and stop before
anything interesting happens. The behaviour worth studying starts well after
that: drift, repetition loops, one participant quietly dominating the others.
Those are the things the turn budget and the observer pass exist to measure.
What I'm working on next
driftcheck — a small eval harness for agent loops. Fixed scenario set,
re-run after every prompt change, diff the outcomes. Answers the question
"did that edit actually improve things, or does it just read better?"
tokenledger — cost and context accounting for long sessions. Tracks spend
per run and flags the turn where context started getting expensive.
Interests
Agent evaluation — test sets, LLM judges, and why most agent benchmarks
measure the wrong thing
Long-horizon behaviour: context management, memory, drift over hundreds of turns
The unglamorous infrastructure — retries, rate limits, resumability. Most
agent projects die on these rather than on anything conceptual.
Stack
Python for most things, Rust when it needs to be fast, SQLite far more often
than it probably should be.
Notes
I write up things that broke and what fixed them. If something here is useful
and under-documented, open an issue — that's usually the fastest way to get me
to write the docs.