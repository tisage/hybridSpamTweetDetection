# A Hybrid Ensemble Method for Spam Tweet Detection using Imbalanced Datasets

[![DOI](https://img.shields.io/badge/DOI-10.1080%2F19393555.2025.2575221-blue)](https://doi.org/10.1080/19393555.2025.2575221)
[![Journal](https://img.shields.io/badge/Journal-Information%20Security%20Journal-orange)](https://www.tandfonline.com/journals/uiss20)

## Overview

This repository contains the implementation of a heterogeneous ensemble approach for Twitter spam detection that addresses the challenges of class imbalance and evolving spam techniques. Our method combines dual LSTM networks with an XGBoost meta-classifier to achieve superior performance on imbalanced datasets.

Twitter spam poses significant security threats that extend beyond social media platforms into the real world. This research proposes an innovative solution that integrates behavioral and semantic analysis through a carefully designed ensemble architecture.

## Abstract

A series of incidents showed that many security threats caused by Twitter spam tweets can reach far beyond the social media platform and impact the real world. Many studies have applied machine learning techniques to classify spam tweets to alleviate such threats. However, Twitter spam detection faces significant challenges due to class imbalance and the evolving nature of spam techniques. This paper proposes a heterogeneous ensemble approach combining dual LSTM networks with a meta-classifier to address imbalanced Twitter spam detection. Our architecture integrates a similarity-based LSTM processing user behavioral features with a word embedding LSTM analyzing semantic textual patterns, followed by an XGBoost meta-classifier trained on disagreed instances. Experiments on two benchmark datasets (1KS10KN and HSPAM) demonstrate that our model outperforms existing baseline models, achieving F1 scores of 0.952 and 0.945, respectively. The precision-focused approach achieves effective performance suitable for social media content moderation requirements while maintaining practical deployment feasibility. The heterogeneous ensemble framework shows strong potential for application to other imbalanced text classification domains beyond spam detection, providing a robust foundation for cybersecurity and content moderation systems.

## Key Features

- **Heterogeneous Ensemble Architecture**: Combines dual LSTM networks with XGBoost meta-classifier
- **Behavioral Analysis**: Similarity-based LSTM for user behavioral features
- **Semantic Analysis**: Word embedding LSTM for textual pattern recognition
- **Imbalanced Data Handling**: Designed specifically for highly imbalanced datasets
- **Practical Deployment**: Precision-focused approach suitable for content moderation

## Datasets

This project uses two benchmark datasets for Twitter spam detection:

### 1KS10KN Dataset
Located in `data/1ks-10kn/`

### HSPAM Dataset
Located in `data/hspam/`

Both datasets contain Twitter data with significant class imbalance, reflecting real-world spam detection scenarios.

## Citation

If you use this code or datasets in your research, please cite our paper:

```bibtex
@article{wang2025hybrid,
  title={A Hybrid Ensemble Method for Spam Tweet Detection using Imbalanced Datasets},
  author={Wang, Tianyu and Genc, Yegin and Chen, Li-Chiou},
  journal={Information Security Journal: A Global Perspective},
  year={2025},
  publisher={Taylor \& Francis},
  doi={10.1080/19393555.2025.2575221},
  url={https://doi.org/10.1080/19393555.2025.2575221}
}
```

## Publication

**Article Title:** A Hybrid Ensemble Method for Spam Tweet Detection using Imbalanced Datasets

**Journal:** Information Security Journal: A Global Perspective

**Article ID:** UISS (2575221)

**DOI:** [10.1080/19393555.2025.2575221](https://doi.org/10.1080/19393555.2025.2575221)

**Publisher:** Taylor & Francis

## License

See [LICENSE](LICENSE) file for details.
