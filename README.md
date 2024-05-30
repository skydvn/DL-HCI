# DL-HCI: Disentanglement Learning - Hierarchical Causality Invariant 

# Envinronment Setup
```
python3 -m venv .env
source .env/bin/activate
python -m pip install -U pip
pip install -r requirements.txt
```
The project is conducted using the Nvidia Driver version of ```535.xx``` and CUDA version of ```12.1```, hence Pytorch can be installed as follows:
```
pip3 install torch torchvision torchaudio
```



# Simulation Conducting
After generate needed data set, repo user can conduct experiment. First cd to ```system``` folder.
```
cd /path/to/DL-HCI/system
``` 
then use the params in ```main.py``` to conduct the simulation, the follow command is an example:
```
python -u main.py -lbs 16 -nc 20 -jr 1 -nb 10 -data Cifar10 -m dnn -algo FedFomo -gr 2000 -M 5 -did 1 -go dnn --log
```

## Wandb and Tensorboard
If you want to track your experiment, consider use ```--log``` args, toggle it to use the wandb and tensorboard along with a automated folder structure.

## Benchmark and Visualization
If you want to clone all experiments from Wandb and visualize them, consider use the two following files:
- ```/path/to/DL-HCI/benchmark/gather_online_data.py``` to gather all experiments
- ```/path/to/DL-HCI/benchmark/benchmark.py``` to create an offline benchmark, which is saved to ```/path/to/FedLAG/benchmark/results_plot/```

# Citation
```
```
