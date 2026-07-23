# Random Features

<p align="center">
  <a href="#license"><img src="https://img.shields.io/badge/license-pending-0E7C66.svg" alt="License"></a> <a href="#paper-or-reference"><img src="https://img.shields.io/badge/paper-reference-1F4E79.svg" alt="Paper or reference"></a> <img src="https://img.shields.io/badge/language-Python-3776AB.svg" alt="Python">
</p>

<p align="center">
  <strong>Random-feature and deep GP experiments for scalable kernel learning.</strong>
</p>

<p align="center">
  <img src="assets/readme-figure.png" alt="Random Features overview" width="100%">
</p>

The overview figure connects input data, random basis projections, approximate kernels, uncertainty bands, and scalability diagnostics into one method pipeline.

## Overview

Random Features implements datasets, losses, likelihoods, MCMC utilities, and experiment scripts for studying random-feature approximations in Gaussian-process-style models. The code is modular enough to reuse pieces across experiments while keeping benchmark folds and experiment scripts in the repository.

## What Is Included

- `dataset.py`: dataset loading and preprocessing helpers.
- `dgp_rff.py`: deep GP random-feature implementation.
- `likelihoods/`, `losses/`, `mcmc/`: modeling components used by experiments.
- `experiments/`: experiment scripts and configuration points.
- `FOLDS/`: fold definitions or saved split assets.

## Quick Start

1. `git clone git@github.com:Hik289/random-features.git`
2. `python -m venv .venv && source .venv/bin/activate`
3. `python -m pip install -U pip numpy scipy scikit-learn matplotlib`
4. Start from `experiments/`, then reuse `dataset.py` and `dgp_rff.py` for new benchmark runs.

## Suggested Workflow

1. Start with the smallest runnable script or notebook listed above.
2. Keep raw data paths and credentials outside the repository.
3. Save generated figures, tables, and reports under the existing result folders.
4. When an experiment becomes stable, record the exact data window, parameters, and command used to reproduce it.

## Repository Map

- `assets/readme-figure.png`: README overview figure.
- Project scripts and notebooks: core research entry points.
- Result or report folders: generated artifacts used for analysis and review.

## Paper or Reference

No external paper link is currently attached to this project. For now, the code, notebooks, and notes in this repository are the primary reference artifact.

## License

No explicit license file is included yet. Add one before public reuse, redistribution, or package release.

## Maintenance Notes

- Add a pinned environment file if this project is prepared for external installation.
- Keep large datasets outside Git and document where each script expects them locally.
- Prefer small, named experiment outputs over overwriting shared result files.
