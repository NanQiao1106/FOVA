<div align="center">
  <h1>FOVA: Offline Federated Reinforcement Learning with Mixed-Quality Data</h1>
</div>

---

# FORL: Federated Offline Reinforcement Learning Framework

![MIT](https://img.shields.io/badge/license-MIT-blue)

FORL is a federated offline reinforcement learning framework based on PyTorch, implementing the FOVA algorithm for handling mixed-quality data in distributed settings.

## Features

- **Federated Learning**: Supports distributed training across multiple clients with local data
- **Mixed-Quality Data**: Handles datasets with varying quality levels from different sources
- **CQL-based**: Built on Conservative Q-Learning for offline RL stability
- **Flexible Architecture**: Easy to extend with new algorithms and datasets

## Supported Algorithms

- **FVCQLCSL**: Federated Variational Conservative Q-Learning with Contrastive Skill Learning
- Multiple variants available in the `forl/` directory

## Installation

### Prerequisites
- Python 3.8+
- PyTorch
- MuJoCo (for D4RL environments)
- D4RL datasets

### Setup
```shell
# Install D4RL
git clone https://github.com/Farama-Foundation/d4rl.git
cd d4rl
pip install -e .

# Install FORL
python setup.py install
```

## Quick Start

### Training
```shell
# Run FVCQLCSL on antmaze-umaze environment
python forl/fvcqlcsl.py --task antmaze-umaze --local-num 5 --local-data-size 2000
```

### Key Parameters
- `--local-num`: Number of local clients
- `--local-data-size`: Data size per client
- `--lmbda`: Lambda parameter for skill learning
- `--beta`: Beta parameter for contrastive learning

## Project Structure

```
FORL/
├── forl/          # Federated offline RL algorithms
├── offlinerlkit/  # Base offline RL toolkit
├── D4RL/         # D4RL dataset support
└── setup.py      # Installation script
```

## Citing FORL

If you use FORL in your research, please cite:

```bibtex
@misc{forl2024,
  title={FOVA: Offline Federated Reinforcement Learning with Mixed-Quality Data},
  author={Nan Qiao},
  year={2024},
  publisher={GitHub},
  journal={GitHub repository},
  howpublished={\url{https://sites.google.com/view/fova/}},
}
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

*Code will be updated soon*
