# A Statistical Approach to Assessing Neural Network Robustness

Here you can find a [PyTorch](http://pytorch.org/) implementation of [Adaptive Multilevel splitting](http://www.nowozin.net/sebastian/blog/multilevel-splitting.html) and code to reproduce the experiments in [our paper](https://arxiv.org/abs/1811.07209).

## Instructions

To run Experiment 6.2:

1. Install [Gurobi](https://www.gurobi.com). (This is required for the PLNN package to load, but is not actually used by the core code itself.)
2. Activate Gurobi license.
3. From the base directory:
	* `python -m exp_6_2.process_data`
	* `python -m exp_6_2.run_exp`
	* `python -m exp_6_2.plot_exp`

## Pertinent files

* `/exp_6_2`
	* `plot_exp.py` Produces Figures 1 and 4 from the paper for Experiment 6.2.
	* `process_data.py` Converts the CollisionDetection property files into pickled objects and a summary file. Also produces naive MC estimates.
	* `run_exp.py` Run AMLS on the 500 properties to produce results for Experiment 6.1 and 6.2.
* `/plnn` A modified version of the [PLNN package](https://github.com/oval-group/PLNN-verification) with some bug fixes for the latest PyTorch.

## Notes

* The experiments of sections 6.2/6.3 in the paper are currently available. Please contact me if you would like to obtain the code for Section 6.1.
* The code to run the experiments was not completely rerun due to the need for computational resources, so contact me if you are having trouble getting them to run.
* You may wish to modify the code to run the experiments so that it runs different values in parallel across multiple GPUs.

## TODO

* Experiment code for Section 6.4.