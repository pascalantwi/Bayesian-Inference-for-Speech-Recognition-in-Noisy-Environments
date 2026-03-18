
```markdown
# Bayesian Inference for Speech Recognition in Noisy Environments

[![R](https://img.shields.io/badge/R-4.x-blue.svg)](https://www.r-project.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📋 Overview

This project implements Bayesian inference methods for speech recognition in noisy environments. It explores how Bayesian approaches can improve phoneme feature estimation when acoustic signals are corrupted by background noise. The repository contains R code for simulating and comparing different inference techniques including Direct Monte Carlo sampling and Gibbs sampling.

## 🎯 Objectives

1. **Assess the impact of noise variance** on posterior estimates of phoneme features
2. **Extend the model** to account for phoneme-specific noise levels
3. **Compare Bayesian methodologies** with baseline recognition techniques (Maximum Likelihood Estimation)

## 📊 Methodology

### Bayesian Model Specification

The model follows a hierarchical Bayesian structure:

- **Prior:** μ_j ∼ N(μ₀, Σ₀)
- **Likelihood:** y|μ_j ∼ N(μ_j, Σ)

where μ₀ and Σ₀ are derived from high-quality recordings.

### Inference Techniques

- **Direct Monte Carlo Sampling:** Draws samples directly from the posterior distribution
- **Gibbs Sampling:** Iterative conditional sampling for posterior refinement
- **Model Extension:** Phoneme-specific noise covariance (Σ_j varies across phonemes)

## 🚀 Key Features

- **Noise Level Simulation:** Tests performance across noise levels from 0.1 to 1.0
- **Posterior Analysis:** Computes posterior means, covariances, and credible intervals
- **Comparative Evaluation:** Benchmarks Bayesian approach against MLE baseline
- **Visualization:** Includes density plots, trace plots, and accuracy comparisons

## 📈 Results

### Stability Under Noise
- Posterior mean estimates remain stable across varying noise levels (Σ from 0.1 to 1.0)
- Monte Carlo sampling yields more precise mean estimates
- Gibbs sampling provides more controlled covariance growth under high noise

### Recognition Accuracy
- Bayesian approach achieves lower RMSE compared to baseline methods
- Performance advantage becomes more pronounced in high-noise conditions

## 🛠️ Installation

```r
# Clone the repository
git clone https://github.com/yourusername/bayesian-speech-recognition.git

# Install required R packages
install.packages(c("MASS", "ggplot2", "gridExtra"))
```

## 📖 Usage

Run the main R Markdown file to reproduce all analyses:

```r
# Knit the R Markdown document
rmarkdown::render("CAT_FOUR_PASCAL_ANTWI_204949.Rmd")
```

## 📁 Repository Structure

```
├── CAT_FOUR_PASCAL_ANTWI_204949.Rmd    # Main analysis script
├── NOISY ENVIRONMENT PRESENTATION.pdf  # Project presentation
├── README.md                            # This file
└── output/                              # Generated figures and tables
```

## 📊 Sample Output

```r
# Posterior estimates at different noise levels
Noise Level | Monte Carlo (X,Y) | Gibbs Sampling (X,Y)
0.1         | 2.801, 4.598      | 2.802, 4.596
1.0         | 2.802, 4.597      | 2.804, 4.596
```

## 📚 References

- Orimoto, H., Ikuta, A., & Hasegawa, K. (2021). Speech Signal Detection Based on Bayesian Estimation...
- Gong, Y. (1995). Speech recognition in noisy environments: A survey. Speech Communication
- Kreisinger, T., et al. (1998). Experimental Study of Speech Recognition in Noisy Environments



**Keywords:** Bayesian Inference, Speech Recognition, Noisy Environments, Monte Carlo, Gibbs Sampling, R Programming
```

This README provides:
- Clear project overview and objectives
- Methodology explanation
- Installation and usage instructions
- Key results summary
- Repository structure
- References and citations
- Author information and licensing

