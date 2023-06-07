# Data-Centric AI Toolkit (D-CAT)

![GitHub top language](https://img.shields.io/github/languages/top/seedatnabeel/D-CAT)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

---

## 📝 What is D-CAT? 

Data and hardness characterization are crucial in Data-Centric AI. 

Many methods have been developed for this purpose. D-CAT provides a unified interface for 13 state-of-the-art methods making them easy to use and/or evaluate. 

We also include a benchmark which allows these hardness characterization methods (HCMs) to be evaluated on 9 different types of hardness.

## 🚀 Installation

To install D-CAT, follow the steps below:

1. Clone the repository

2. Create a new virtual environment or conda environment with Python >3.7: 

    ```bash
    virtualenv dcat_env 
    ```
    OR
    ```bash
    conda create --name dcat_env
    ```

3. With the environment activated, run the following command from the repository directory:

    ```bash
    pip install -r requirements.txt
    ```

4. Link the venv or conda env to the kernel:

    ```bash
    python -m ipykernel install --user --name=dcat_env
    ```

## 🛠️ Usage

There are two ways to get started with D-CAT:

1. Have a look at the tutorial notebook: `tutorial.ipynb` which shows you step by step how to use the different D-CAT modules.

2. Using D-CAT on your own data --- you could follow the steps in the tutorial notebook.

3. Running a benchmarking evaluation. `run_experiment.py` runs different experiements. These can be triggered by bash scripts. We provide an example in `run.sh`.

Below is an example of how to use D-CAT:

```bash
# Set the parameterizable arguments
total_runs=3
epochs=10
seed=0

# uniform mnist 
hardness="uniform"
dataset="mnist"
model_name="LeNet"
python run_experiment.py --total_runs $total_runs --hardness $hardness --dataset $dataset --model_name $model_name --seed $seed --prop 0.1 --epochs $epochs
```

## 🔎 Logging
Outputs from experimental scripts are logged to [Weights and Biases - wandb](https://wandb.ai). An account is required and your WANDB_API_KEY and Entity need to be set in wandb.yaml file provided.



## 📄 License

This project is licensed under the Apache 2.0 License - see the [LICENSE](LICENSE) file for more details.



---

<div align="center">
    <strong>Give a ⭐️ if this project was useful!</strong>
</div>

