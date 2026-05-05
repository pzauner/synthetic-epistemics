# synthetic-epistemics

A harness for studying how controlled information environments shape LLM agent beliefs and actions.

## Project Idea

`synthetic-epistemics` explores how language model agents form beliefs and choose actions when their information environment is mediated by tools: search results, retrieved documents, simulated websites, structured source bundles, terminal output, APIs, and other external context.

The main goal is to build a harness for constructing controlled epistemic environments around tool-using LLM agents. Instead of treating retrieval and tool output as neutral facts, the harness should make those information channels explicit, inspectable, and configurable.

This makes it possible to study questions such as:

- How do agents update beliefs when sources conflict?
- How do authority markers influence action selection?
- When does retrieval context change normative or policy-relevant decisions?
- Which agent configurations remain robust under synthetic evidence environments?
- How should evaluations distinguish source use, belief formation, and final actions?

## Status

Project sketch. No implementation yet.

## Related Work

Several existing projects study adjacent parts of this problem:

- [The Synthetic Web](https://arxiv.org/abs/2603.00801) constructs adversarially curated mini-internets for diagnosing epistemic weaknesses of language agents under manipulated search rankings.
- [SeekBench](https://arxiv.org/abs/2509.22391) evaluates epistemic competence in information-seeking agents through trace-level analysis of grounding, search recovery, and calibration.
- [ConflictBank](https://proceedings.neurips.cc/paper_files/paper/2024/hash/baf4b960d118f838ad0b2c08247a9ebe-Abstract-Datasets_and_Benchmarks_Track.html), [MAGIC](https://arxiv.org/abs/2507.21544), [WikiContradict](https://arxiv.org/abs/2406.13805), and [(D)RAGged Into a Conflict](https://research.google/pubs/dragged-into-a-conflict-detecting-and-addressing-conflicting-sources-in-retrieval-augmented-llms/) examine how language models handle conflicting retrieved evidence.
- [WebArena](https://arxiv.org/abs/2307.13854) and [BrowserGym](https://github.com/ServiceNow/BrowserGym) provide reproducible web-agent environments, with a stronger focus on task completion than epistemic manipulation.
- [Inspect AI](https://inspect.aisi.org.uk/) provides general evaluation infrastructure for model and agent evaluations, including tool use, sandboxing, scoring, and traces.

`synthetic-epistemics` is intended to sit closer to the harness layer: a way to construct, vary, and inspect tool-mediated information environments, with benchmarks as one output rather than the only goal.
