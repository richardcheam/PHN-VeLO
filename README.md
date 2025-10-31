# Pareto HyperNetworks with VeLO LibMOON for dSprites, extension to LibMOON solvers

## Before running

Run the following command before doing anything, to install all the requirements:

```bash
$> pip install -e .
```

## Train the model

Run the following command in experiments/dsprites to train the model with the default options:

```bash
experiments/dsprites $> python trainer.py
```

Else, run this command to get all the possible arguments:

```bash
experiments/dsprites $> python trainer.py --help
```

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
