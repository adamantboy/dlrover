# DLRover: An Automatic Distributed Deep Learning System

 [![Build](https://github.com/intelligent-machine-learning/easydl/actions/workflows/main.yml/badge.svg)](https://github.com/intelligent-machine-learning/easydl/actions/workflows/main.yml)

DLRover, as it says, is making deep learning models' training easy. It helps model developers focus on model algorithm itself, without taking care of any engineering stuff, say, hardware acceleration, distribute running, etc. It provides static and dynamic nodes' configuration automatically, before and during a model training job running on k8s. Detail features as,

- Fault-Tolerance.
- Static and Dynamic resource configuration.
- Automatic distributed model training.

DLRover consists three components:

- ElasticTrainer: A framework to use DLRover in training.
- ElasticOperator: A k8s controller to manage training nodes.
- Brain: An optimization service to generate resources plans, distributed running plans, etc.

## Why DLRover

### Fault-tolerance

DLRover can recover failed parameter servers and workers and resume the training.
Some failed nodes do not interrupt the training and hurt the convergence
accuracy.

### Elastic Scheduling

DLRover can scale up and down the number of nodes (parameter servers or workers)
at runtime of a training job. In an ElasticJob of DLrover, nodes can come and
go at any time without interruptting the training process and wasted
work (e.g., initialization and iterations since the number of nodes changes)


### Automatic Resource Optimization

DLRover can automatically configure the resources to start a training job.
After the job starts, DLRover monitors the performance (e.g. throughput and workload)
of a training job and dynamically adjusts the resources to
improve the training performance.

## Quick Start

[TensorFlow Estimator on Aliyun ACK](docs/tutorial/dlrover_cloud.md)
