## GOPS

A new parallel global surrogate-based algorithm Global Optimization in Parallel with Surrogate (GOPS) for the minimization of continuous black-box objective functions that might have multiple local minima, are expensive to compute, and have no derivative information available.

The GOPS algorithm improves on earlier algorithms by (a) new center points are selected based on bivariate non-dominated sorting of previously evaluated points with additional constraints to ensure the objective value is below a target percentile and (b) as iterations increase, the number of centers decreases, and the number of evaluation points per center increases. These strategies and the hyperparameters controlling them significantly improve GOPS’s parallel performance on high dimensional problems in comparison to other global optimization algorithms, especially with a larger number of processors. 

GOPS is tested with up to 128 processors in parallel on 14 synthetic black-box optimization benchmarking test problems (in 10, 21, and 40 dimensions) and one 21-dimensional parameter estimation problem for an expensive real-world nonlinear lake water quality model with partial differential equations that takes 22 min for each objective function evaluation.

Details of GOPS are described in the GOPS paper https://link.springer.com/article/10.1007/s11081-020-09556-1.
The  pseudo-code and  a proof of convergence of GOPS are described in the Supplementary Material of GOPS paper https://static-content.springer.com/esm/art%3A10.1007%2Fs11081-020-09556-1/MediaObjects/11081_2020_9556_MOESM1_ESM.pdf

## Install

Preparing your system to use GOPS
------------------------------------

**python** & **pySOT**

Before starting you will need to Python installed. Recommend python 2.7 since GOPS was developed and tested based on this verison.
You will need to have pySOT (0.1.36) installed. 
To install the pySOT (0.1.36) package with conda run one of the following:

```

		conda install -c conda-forge pysot
```
or
```
		conda install -c conda-forge/label/gcc7 pysot
```

pySOT is a open source toolbox is for optimization of computationally expensive black-box objective functions. 
more information about pySOT refer to: https://pysot.readthedocs.io/en/latest/index.html


## Citing US
If you use GOPS, please cite the following paper: Xia, W., & Shoemaker, C. (2020). GOPS: efficient RBF surrogate global optimization algorithm with high dimensions and many parallel processors including application to multimodal water quality PDE model calibration. Optimization and Engineering, 1-37. https://doi.org/10.1007/s11081-020-09556-1

```
@article{xia2020gops,
  title={GOPS: efficient RBF surrogate global optimization algorithm with high dimensions and many parallel processors including application to multimodal water quality PDE model calibration},
  author={Xia, Wei and Shoemaker, Christine},
  journal={Optimization and Engineering},
  pages={1--37},
  year={2020},
  publisher={Springer}
}
```
