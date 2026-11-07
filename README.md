# Wei-Cheng Hsu

**Software Engineering · ML Systems · Developer Tools**

I am an M.S. student at **National Yang Ming Chiao Tung University (NYCU)**. My work includes tools for machine learning (ML) experiments and independent open-source contributions to **PyTorch**, **Apache TVM**, and **Modular / Mojo**, covering compiler frontend conversion, Python compatibility, and regression tests.

**Open to software engineering opportunities** in ML systems, compilers, AI infrastructure, and developer tools. Based in Hsinchu, Taiwan.

[Email](mailto:willie103006@gmail.com) · [LinkedIn](https://www.linkedin.com/in/hsuweicheng/)

## Independent Open Source Contributions

### PyTorch — TorchDynamo repr / str compatibility

**3 fixes integrated upstream.** Improved CPython-compatible `repr` / `str` formatting under `torch.compile`, with regression tests covering recursive formatting, mutation handling, and compilation-cache reuse. These contributions removed **7 CPython 3.13 expected-failure markers**.

- **Mapping proxies:** added `repr` / `str` support while preserving mutation guards and recursive formatting. [#196902](https://github.com/pytorch/pytorch/pull/196902) · [Upstream commit](https://github.com/pytorch/pytorch/commit/755122e63e7b5644dae7233166b7ff24cf816b6b)
- **Sets and set subclasses:** corrected recursive placeholders and preserved subclass names. [#198476](https://github.com/pytorch/pytorch/pull/198476) · [Upstream commit](https://github.com/pytorch/pytorch/commit/056b6cac6a66edc0b9690e4648297056aee55120)
- **UserList / UserDict:** corrected cycle handling so recursive representations match CPython, with full-graph regression tests. [#198512](https://github.com/pytorch/pytorch/pull/198512) · [Upstream commit](https://github.com/pytorch/pytorch/commit/1ee8175f5b55fdf34390c700365ec6176fd77383)

### Apache TVM — Compiler frontend and validation

**3 merged PRs** extending the Relax TFLite frontend and validating generated IR.

- **Conv3D:** implemented operator conversion, kernel layout, stride, dilation, padding, and fused activation handling. [#19523](https://github.com/apache/tvm/pull/19523)
- **Conv3D Transpose:** handled kernel layout, SAME / VALID padding, and output padding. [#19530](https://github.com/apache/tvm/pull/19530)
- **Gather / GatherND:** corrected GatherND index typing from int32 to int64 and added expected-IR tests. [#19516](https://github.com/apache/tvm/pull/19516)

### Modular / Mojo — Standard library type safety

Added a compile-time constraint to `Tuple.__contains__` to reject incompatible lookup types, with **one compile-fail regression test covering four type-mismatch cases**. Integrated into the public upstream repository.

[#7234](https://github.com/modular/modular/pull/7234) · [Upstream commit](https://github.com/modular/modular/commit/169207304e2c37c88483f3a41fc33b9ab519e02b)

## Selected Projects

### herdr-chat — Multi-agent coordination tool

A personal Python project that connects coding-agent command-line interface (CLI) sessions through a shared group chat, using Herdr.

- Implemented incremental message delivery and a claim/submit protocol controlling a single speaking slot.
- Added session resume and recovery, interruption controls, and agent rejoin handling.
- Tested message coordination, interruption, and recovery with a simulated Herdr backend, used Linux PTYs to test terminal interactions, and automated test execution with GitHub Actions.

**Built with:** Python, Linux PTYs, automated testing, GitHub Actions  
[Repository and demo](https://github.com/weicheng-hsu/herdr-chat)

### HyperOpt Viz Studio — Experiment analysis and replay

A personal Flask / React dashboard for inspecting hyperparameter optimization (HPO) experiments.

- Connected experiment, task, method, and run navigation to a Flask data service.
- Built a visual replay of saved trial results, parallel coordinates, and metric plots to inspect the search process.

**Built with:** React, TypeScript, Vite, Flask  
[Repository](https://github.com/weicheng-hsu/HyperOpt-viz-Studio)

### BrowserOS — C++ split-pane prototype

Developed a Chromium-based C++ split-pane prototype with toolbar actions, pane layout, and resizing, and added four browser-test cases. **Prototype PR #1015 was closed without merging.**

## Research & Skills

**Graduate research, NYCU · September 2024–present**

- Built reproducible federated learning and hyperparameter optimization pipelines with PyTorch, Flower, FedML, Optuna, and Hyperopt.
- Benchmarked TPE and other Bayesian optimization methods against random search under non-IID data distributions.
- Investigated how early trial results influence exploration and exploitation in LLM-guided hyperparameter search.

**Languages:** Python, C, C++, Bash  
**ML & compilers:** PyTorch / TorchDynamo, TVM Relax, Optuna  
**Systems & testing:** Linux, Git, Docker, pytest, GitHub Actions, regression testing  
**Course project experience:** Kubernetes

I welcome conversations about roles involving debugging, testing, and building developer tools.
