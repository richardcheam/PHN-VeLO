# Pareto HyperNetworks with VeLO LibMOON for dSprites, extension to LibMOON solvers

## How to run locally?

Make sure to have virtual environment. If not, in terminal do ```pip3 install virtualenv```. Then,
```bash
git clone https://github.com/richardcheam/PHN-VeLO.git
cd PHN-VeLO
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt
```

> ⚠️ **Warning:** there could be dependencies issue with different libraries and utility functions at first, but it is fast to solve!  

## Train the model with VeLO

Run the following command in experiments/dsprites to train the model with the default options:

```bash
experiments/dsprites $> python trainer.py
```

Else, run this command to get all the possible arguments:

```bash
experiments/dsprites $> python trainer.py --help
```

use script `trainer_adam.py` to train with Adam and `trainer_libmoon.py` to train with LibMOON solver for gradient combinations. **Note that** only EPO LibMOON solver is available which provides as an example. More solvers can be added in `PHN-VeLO/phn/libmoon_wrapper.py`.

## Visualize Pareto front

Works only when trained on 2 tasks.
Train a model, then with the JSON results file in the outputs folder, run the following command:

```bash
experiments/dsprites $> python plot.py --resultspath outputs/val_results_[DATETIME].json
```

To get all the possible options, run the following command:

```bash
experiments/dsprites $> python plot.py --help
```

## Inference

To inferere the model on the data with the default options, run the following command:

```bash
experiments/dsprites $> python run.py --modelpath outputs/hnet_[DATETIME].pt
```

To get all the possible options, run the following command:

```bash
experiments/dsprites $> python run.py --help
```
