# Wei-Cheng Hsu

**ML Systems · Compiler Correctness · Developer Tools**

M.S. student at National Yang Ming Chiao Tung University (NYCU) and open-source contributor to **PyTorch**, **Apache TVM**, and **Modular / Mojo**. My work spans Python runtime compatibility, ML compiler frontends, and tools for reproducible experiments.

Interested in software engineering roles in ML systems, compilers, and AI infrastructure.

[Email](mailto:willie103006@gmail.com) · [LinkedIn](https://www.linkedin.com/in/hsuweicheng/)

## Selected Open Source Contributions

### PyTorch — TorchDynamo correctness

**2 contributions merged upstream.** Fixed differences between `torch.compile` and CPython when formatting self-referential containers, with full-graph regression tests.

- **UserList / UserDict:** corrected cycle handling so recursive representations match CPython. [#198512](https://github.com/pytorch/pytorch/pull/198512)
- **Sets and set subclasses:** corrected recursive placeholders and preserved subclass names. [#198476](https://github.com/pytorch/pytorch/pull/198476)

### Apache TVM — ML compiler frontend

**3 merged PRs.** Extended the Relax TFLite frontend with operator conversion and tests against expected IRModules.

- **Conv3D:** implemented conversion with layout, stride, dilation, padding, and fused activation handling. [#19523](https://github.com/apache/tvm/pull/19523)
- **Conv3D Transpose:** handled kernel layout, SAME / VALID padding, and output padding. [#19530](https://github.com/apache/tvm/pull/19530)
- **Gather / GatherND:** added IR validation tests and corrected GatherND index typing. [#19516](https://github.com/apache/tvm/pull/19516)

### Modular / Mojo — Standard library type safety

Added a compile-time type constraint and regression tests to `Tuple.__contains__`, so incompatible lookup types produce a compile-time error. [#7234](https://github.com/modular/modular/pull/7234)

**Merged upstream and landed in the public repository.** [Upstream commit](https://github.com/modular/modular/commit/169207304e2c37c88483f3a41fc33b9ab519e02b).

## Selected Projects

### CCG-TUI — Terminal workspace for coding agents

A Python terminal interface for working with Codex, Claude Code, Gemini CLI, and Antigravity CLI.

- Unified backend adapters and activity reporting across multiple coding CLIs.
- Persisted transcripts and recovery state, with explicit context handoff between backends.

**Built with:** Python, prompt_toolkit, JSON transcripts  
[Repository](https://github.com/weicheng-hsu/ccg-tui) · [Demo (simulated backend)](https://github.com/weicheng-hsu/ccg-tui/blob/main/docs/assets/ccg-tui-demo.gif) · [Tests](https://github.com/weicheng-hsu/ccg-tui/tree/main/tests)

### HyperOpt Viz Studio — Experiment analysis and replay

An interactive dashboard for inspecting hyperparameter optimization experiments.

- Connected a Flask data service to a React interface for browsing experiments, tasks, methods, and runs.
- Added optimization replay, parallel coordinates, and metric plots to inspect the search process.

**Built with:** TypeScript, React, Vite, Flask  
[Repository](https://github.com/weicheng-hsu/HyperOpt-viz-Studio)

## Skills & Research

- **Languages:** Python, C/C++, TypeScript, Bash
- **ML systems:** PyTorch, TVM Relax, compiler frontends, regression testing
- **Engineering tools:** Linux, Git, Docker

My research explores LLM-assisted Bayesian optimization and hyperparameter optimization for federated learning under limited evaluation budgets.
