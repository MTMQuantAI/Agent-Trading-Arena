# Agent Trading Arena

<p align="center">
  <b>Agent-based trading simulation environments for studying LLM financial reasoning.</b>
</p>

<p align="center">
  <a href="https://arxiv.org/abs/2502.17967"><img src="https://img.shields.io/badge/arXiv-2502.17967-b31b1b.svg" alt="arXiv"></a>
  <a href="https://aclanthology.org/2025.findings-emnlp.294.pdf"><img src="https://img.shields.io/badge/Findings%20of%20EMNLP-2025-blue.svg" alt="EMNLP 2025"></a>
  <a href="decoupledmarket/papers/decoupledmarket.pdf"><img src="https://img.shields.io/badge/ICML-2026-2ea44f.svg" alt="ICML 2026"></a>
  <img src="https://img.shields.io/badge/Python-3.9%2B-blue.svg" alt="Python">
  <img src="https://img.shields.io/badge/License-MIT-lightgrey.svg" alt="License">
</p>

<p align="center">
  <a href="#papers-and-code">Papers</a> |
  <a href="#quick-start">Quick Start</a> |
  <a href="#repository-layout">Repository Layout</a> |
  <a href="#citation">Citation</a>
</p>

This repository hosts our research line on LLM-based trading agents, numerical understanding, and quantitative reasoning in controllable market environments. It contains the original **Agent Trading Arena** code for Findings of EMNLP 2025 and the newer **DecoupledMarket** code for ICML 2026.

## Papers and Code

| Project | Paper | Venue | Code |
| --- | --- | --- | --- |
| **Agent Trading Arena** | Agent Trading Arena: A Study on Numerical Understanding in LLM-Based Agents | Findings of EMNLP 2025 | [`Agent-Trading-Arena/`](Agent-Trading-Arena/) |
| **DecoupledMarket** | Evolving Quantitative Reasoning through Self-Play in Digital Twin Markets | ICML 2026 | [`decoupledmarket/`](decoupledmarket/) |

## Project Overview

### Agent Trading Arena

<p align="center">
  <img src="images/Agent_Trading_Arena.png" width="82%" alt="Agent Trading Arena">
</p>

Agent Trading Arena is a closed-loop, prior-free, human-like trading environment designed to evaluate and advance self-play-capable financial agents. It focuses on numerical understanding in LLM-based agents and provides the code for our Findings of EMNLP 2025 paper.

### DecoupledMarket

<p align="center">
  <img src="decoupledmarket/assets/figures/framework.png" width="92%" alt="DecoupledMarket framework">
</p>

DecoupledMarket extends this research line toward quantitative reasoning. It decouples high-level LLM planning from numerical computation, delegates quantitative operations to explicit tools, and evaluates agents through self-play in a controllable digital twin market.

## Highlights

- Closed-loop market environments for LLM-based financial agents.
- Reproducible simulation workflows for comparing agent behavior.
- Self-play trading settings with memory, reflection, and strategy feedback.
- Decoupled reasoning-computation workflow for quantitative finance.
- Parallel execution and performance monitoring in DecoupledMarket.

## Quick Start

Clone the repository:

```bash
git clone git@github.com:MTMQuantAI/Agent-Trading-Arena.git
cd Agent-Trading-Arena
```

### Agent Trading Arena

```bash
pip install -r requirement.txt
cd Agent-Trading-Arena
sh run.sh
```

### DecoupledMarket

```bash
cd decoupledmarket
pip install -e .
python scripts/run_parallel.py --mode parallel --executor thread
```

For a quick smoke test:

```bash
python -m pytest -q
```

## API Keys

API keys should be provided through environment variables. Do not hard-code keys in source files.

```bash
export OPENAI_API_KEY="..."
export GLM_API_KEY="..."
export DEEPINFRA_API_KEY="..."
export DEEPSEEK_API_KEY="..."
export GOOGLE_API_KEY="..."
```

DecoupledMarket reads keys from environment variables. See [`decoupledmarket/README.md`](decoupledmarket/README.md) for project-specific details.

## Repository Layout

```text
Agent-Trading-Arena/
|-- Agent-Trading-Arena/   # Findings of EMNLP 2025 code
|-- decoupledmarket/       # ICML 2026 DecoupledMarket code
|-- docs/                  # Additional documentation
|-- images/                # Root README figures
|-- requirement.txt        # Dependencies for Agent Trading Arena
`-- README.md              # Repository landing page
```

## Citation

If you find this repository useful, please cite the relevant paper.

### Agent Trading Arena

```bibtex
@inproceedings{ma2025agent,
  title={Agent Trading Arena: A Study on Numerical Understanding in LLM-Based Agents},
  author={Ma, Tianmi and Du, Jiawei and Huang, Wenxin and Wang, Wenjie and Xie, Liang and Zhong, Xian and Zhou, Joey Tianyi},
  booktitle={Findings of the Association for Computational Linguistics: EMNLP 2025},
  pages={5496--5514},
  year={2025}
}
```

### DecoupledMarket

```bibtex
@inproceedings{ma2026decoupledmarket,
  title     = {Evolving Quantitative Reasoning through Self-Play in Digital Twin Markets},
  author    = {Ma, Tianmi and Huang, Wenxin and Du, Jiawei and Li, Lin and Zhong, Xian and Zhou, Joey Tianyi},
  booktitle = {Proceedings of the 43rd International Conference on Machine Learning},
  year      = {2026}
}
```

## Contact

For questions about the projects, please open an issue or contact the corresponding authors listed in the papers.
