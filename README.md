# Real-Time DAG Quantile Prediction

This repository contains the implementation of a real-time systems project on
distributional execution-time prediction for DAG nodes running on a heterogeneous
big/little multicore platform with DVFS.

Instead of predicting only the average execution time or a single WCET value, the
project predicts multiple conditional execution-time quantiles for each DAG node
under different hardware and system-state conditions.

## Project Overview

The goal is to estimate execution-time quantiles for DAG nodes based on:

- DAG structure and node features
- predecessor/successor and edge-related information
- big/little core type
- DVFS level
- current system-state features
- memory pressure, bus utilization, temperature, and jitter

The model predicts:

```text
q50, q90, q95, q99
