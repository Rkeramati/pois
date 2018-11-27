<img src="data/logo.png" width=25% align="right" />

# POIS (NeurIPS 2018)

This repository contains the implementation of the [POIS algorithm](https://arxiv.org/abs/1809.06098).
Click [here](https://t3p.github.io/NIPS/) for more info about our NeurIPS 2018 paper.

The implementation is based on OpenAI [baselines](https://github.com/openai/baselines).
We are working on synchronising this repository to the current version of baselines.

## What's new
We provide 3 different flavours of the POIS algorithm:
- **POIS1**: control-based POIS (cpu)
- **POIS2**: control-based POIS (gpu optimized, used in complex environments or complex policies)
- **PBPOIS**: parameter-based POIS (cpu)

## Minimal install with Docker
To test POIS on classic control environments within minutes, you can build a Docker image. This solution does not support Mujoco environments.

First, you need to [install Docker](https://docs.docker.com/get-started/#prepare-your-docker-environment). 
Then, clone the repository and build the image:

```bash
git clone https://github.com/T3p/pois
cd pois
docker build -t pois .
```

You can run the image as:


```bash
docker run -it pois
```

This will create a docker container and give you access to an interactive shell.
To test your installation (within the container):


```bash
cd pois1
python run_rllab.py
```

This should run pois1 (action-based POIS for CPU) on the 'cartpole' environment (rllab version)

## Full install

## Citing
To cite the POIS paper:

    @misc{metelli2018policy,
      title={Policy Optimization via Importance Sampling},
      author={Alberto Maria Metelli and Matteo Papini and Francesco Faccio and Marcello Restelli},
      year={2018},
      eprint={1809.06098},
      archivePrefix={arXiv},
      primaryClass={cs.LG}
    }
    
 ## Acknoledgements
 The gpu-optimized version of POIS was developed by [Nico Montali](https://github.com/nicomon24), who also contributed to the overall refining of the code.
