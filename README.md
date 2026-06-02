# Agent Trading Arena: A Study on Numerical Understanding in LLM-Based Agents
<div align="center">

[[arXiv]](https://arxiv.org/abs/2502.17967)
[[PDF]](https://aclanthology.org/2025.findings-emnlp.294.pdf)

[![Python Version](https://img.shields.io/badge/Python-3.10-blue.svg)]()
[![GitHub license](https://img.shields.io/badge/MIT-blue)]()


![](images/Agent_Trading_Arena.png)

</div>

The Agent Trading Arena is a closed-loop, prior-free human-like trading environment designed to evaluate and advance self-play-capable financial agents.

## Papers and Code

This repository hosts our agent-based trading simulation research line.

| Paper | Venue | Code |
| --- | --- | --- |
| Agent Trading Arena: A Study on Numerical Understanding in LLM-Based Agents | Findings of EMNLP 2025 | [`Agent-Trading-Arena/`](Agent-Trading-Arena/) |
| Evolving Quantitative Reasoning through Self-Play in Digital Twin Markets | ICML 2026 | [`decoupledmarket/`](decoupledmarket/) |


# Preparation

## Python Install
```
git clone https://github.com/MTMQuantAI/Agent-Trading-Arena.git
cd Agent-Trading-Arena
pip install -r requirement.txt
```
## Set OpenAI API Key: 
Export your OpenAI API key as an environment variable. Replace "your_OpenAI_API_key" with your actual API key.
```
export OPENAI_API_KEY="your_OpenAI_API_key"
```
You can get an API key from the [OpenAI platform](https://platform.openai.com/api-keys).

For the DecoupledMarket code, see [`decoupledmarket/README.md`](decoupledmarket/README.md).

# Experiment

## Run the code
```
cd Agent-Trading-Arena
sh run.sh
```

# Citation
If you find our work useful, please consider citing us!
```
@inproceedings{ma2025agent,
  title={Agent Trading Arena: A Study on Numerical Understanding in LLM-Based Agents},
  author={Ma, Tianmi and Du, Jiawei and Huang, Wenxin and Wang, Wenjie and Xie, Liang and Zhong, Xian and Zhou, Joey Tianyi},
  booktitle={Findings of the Association for Computational Linguistics: EMNLP 2025},
  pages={5496--5514},
  year={2025}
}
```
