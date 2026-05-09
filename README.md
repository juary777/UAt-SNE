# UAt-SNE: Uncertainty-Aware t-SNE

Uncertainty-aware t-SNE (UAt-SNE) is a noise-defending visualization tool tailored for uncertain single-cell RNA-seq data. It extends standard t-SNE by embedding each sample as a probability distribution rather than a single point, enabling uncertainty to be propagated through the visualization process.

## Why UAt-SNE?

Standard t-SNE often fails to account for uncertainties in the original dataset, leading to misleading visualizations where cell subsets with noise appear indistinguishable. Single-cell RNA sequencing data is inherently noisy due to dropout events and amplification bias, making uncertainty awareness essential for accurate visualization.

## How it works

**Fuzzy object representation**: Each sample is represented as a probabilistic object with associated uncertainty, translating transcriptomic variability into stable, quantifiable signals.

**Probabilistic similarity computation**: Pairwise similarities are computed by integrating over all possible realizations of the fuzzy objects, both in high-dimensional and low-dimensional spaces.

**Uncertainty propagation**: High-dimensional uncertainty is propagated to the low-dimensional embedding, revealing significant uncertainties in transcriptomic variability and allowing users to assess embedding reliability for each sample.

This versatile uncertainty-aware visualization tool can be easily adapted to other scientific domains beyond single-cell RNA sequencing, making it valuable for general high-dimensional data analysis.

Check out our [preprint](https://arxiv.org/abs/2410.00473) for more details.

## Installation

```bash
pip install uatsne
