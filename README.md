# A Hybrid Ensemble Method for Imbalanced Spam Tweet Detection

[![DOI](https://img.shields.io/badge/DOI-10.1080%2F19393555.2025.2575221-blue)](https://doi.org/10.1080/19393555.2025.2575221)
[![Journal](https://img.shields.io/badge/Journal-Information%20Security%20Journal-orange)](https://www.tandfonline.com/journals/uiss20)

## Paper Information

This is a repo for research paper "A Hybrid Ensemble Method for Spam Tweet Detection using Imbalanced Datasets" on Information Security Journal: A Global Perspective (2025).
**DOI**: [10.1080/19393555.2025.2575221](https://doi.org/10.1080/19393555.2025.2575221)  


## Abstract

A series of incidents showed that many security threats caused by Twitter spam tweets can reach far beyond the social media platform and impact the real world. Many studies have applied machine learning techniques to classify spam tweets to alleviate such threats. However, Twitter spam detection faces significant challenges due to class imbalance and the evolving nature of spam techniques. This paper proposes a heterogeneous ensemble approach combining dual LSTM networks with a meta-classifier to address imbalanced Twitter spam detection. Our architecture integrates a similarity-based LSTM processing user behavioral features with a word embedding LSTM analyzing semantic textual patterns, followed by an XGBoost meta-classifier trained on disagreed instances. Experiments on two benchmark datasets (1KS10KN and HSPAM) demonstrate that our model outperforms existing baseline models, achieving F1 scores of 0.952 and 0.945, respectively. The precision-focused approach achieves effective performance suitable for social media content moderation requirements while maintaining practical deployment feasibility. The heterogeneous ensemble framework shows strong potential for application to other imbalanced text classification domains beyond spam detection, providing a robust foundation for cybersecurity and content moderation systems.

## Dataset Overview

- 1KS-10KN: `data/1ks-10kn`, Imbalanced Dataset
- HSPAM: `data/hspam`, Balanced Dataset

## Key Features

- **Heterogeneous Ensemble Architecture**: Combines dual LSTM networks with XGBoost meta-classifier
- **Behavioral Analysis**: Similarity-based LSTM for user behavioral features
- **Semantic Analysis**: Word embedding LSTM for textual pattern recognition
- **Imbalanced Data Handling**: Designed specifically for highly imbalanced datasets
- **High Performance**: F1 scores of 0.952 (1KS10KN) and 0.945 (HSPAM)
- **Practical Deployment**: Precision-focused approach suitable for content moderation

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

## Data Availability and Ethics

- All data was collected in compliance with X's Terms of Service
- Personal identifiable information has been anonymized
- Dataset is provided for research purposes only
- Commercial use is not permitted

## License

This dataset is provided under the Creative Commons Attribution 4.0 International License (CC BY 4.0) for academic research purposes. See [LICENSE](LICENSE) file for details.
