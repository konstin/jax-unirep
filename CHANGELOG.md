# Changelog

In the changelog, @ElArkk and @ericmjl would like to acknowledge contributors who have helped us with anything on the project, big or small.

<Please add your contribution to the top>

- 20 April 2020: Code fixes for major bug with negative and NaN losses due to Softmax issue by @ivanjayapurna,
- 20 April 2020: (Also by @ivanjayapurna) Overhauled evotuning.py with major changes including
    1. option to supply an out-domain holdout set and print params as training progresses,
    2. evotuning without Optuna by directly calling fit function,
    3. added avg_loss() function for calculation outputting of training and holdout set loss to a log file (number and length of batches are also calculated and printed to log file),

    4. introduction of "epochs_per_print" to periodically calculate losses and dump parameters
    5. Implemented adamW in JAX and switched optimizer to adamW,
    6. added option to change the number of folds in optuna KFolds,
    7. update evotuning-prototype.py example script
- 30 March 2020: Code fixes for correctness and readability, and a parameter dumping function by @ivanjayapurna,
- 28 June 2020: Improvements to evotuning ergonomics, by @ericmjl
    1. Adds a pre-commit configuration.
    1. Adds an installation script that makes easy the installation of jax on GPU.
    1. Provided backend specification of device (GPU/CPU).
    1. Switched preparation of sequences as input-output pairs exclusively on CPU, for speed.
    1. Added ergonomic UI features - progressbars! - that improve user experience.
    1. Added docs on recommended batch size and its relationship to GPU RAM consumption.
    1. Switched from exact calculation of train/holdout loss to estimated calculation.
- 9 July 2020: Add progress bar to sequence sampler, by @ericmjl
