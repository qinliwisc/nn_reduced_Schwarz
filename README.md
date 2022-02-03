# A two-layer neural network-based reduced order Schwarz method for fully nonlinear mutitscale elliptic PDEs

The source code for the paper [S. Chen, Z. Ding, Q. Li, S. J. Wright. A reduced order Schwarz method for nonlinear multiscale elliptic equations based on two-layer neural networks. arXiv:2111.02280](https://arxiv.org/abs/2111.02280).

## Organization

- `src`: contains the local PDE solvers, the reduced order Schwarz solvers and all the sub routines
- `examples`: contains one example of semilinear elliptic equations and one example of p-Poisson equations

The run time to generate offline dictionaries could be between several minutes to several hours depending on the parameters, e.g., the discretization and the dataset size.

## Instructions for use

The instructions for running each case are as follows.

### Semilinear elliptic equations

1. Run semilinear_data.m, which will generate training dataset on each local patch and save them in data_semilinear
2. Run semilinear_init.m, which will generate initial weights used in the training of neural networks
3. Run semilinear_NN.py to train the neural networks that learns the boundary-to-boundary operator in the Schwarz iteration
4. Run semilinear_online.m to solve the semilinear elliptic equations

### p-Poisson equations

1. Run pPoi_data.m, which will generate training dataset on each local patch and save them in data_semilinear
2. Run pPoi_init.m, which will generate initial weights used in the training of neural networks
3. Run pPoi_NN.py to train the neural networks that learns the boundary-to-boundary operator in the Schwarz iteration
4. Run pPoi_online.m to solve the p-Poisson equations

## Cite this work

If you use this code for academic research, you are encouraged to cite the following paper:

```
@article{ChDiLiWr:2021reduced,
  title={A reduced order Schwarz method for nonlinear multiscale elliptic equations based on two-layer neural networks},
  author={Chen, Shi and Ding, Zhiyan and Li, Qin and Wright, Stephen J},
  journal={arXiv preprint arXiv:2111.02280},
  year={2021}
}
```

## Questions

To get help on how to use the data or code, simply open an issue in the GitHub "Issues" section.