# A Hybrid Ensemble Method for Imbalanced Spam Tweet Detection

[![DOI](https://img.shields.io/badge/DOI-10.1080%2F19393555.2025.2575221-blue)](https://doi.org/10.1080/19393555.2025.2575221)
[![Journal](https://img.shields.io/badge/Journal-Information%20Security%20Journal-orange)](https://www.tandfonline.com/journals/uiss20)

## Paper Information

**Title**: A Hybrid Ensemble Method for Spam Tweet Detection using Imbalanced Datasets  
**Authors**: Tianyu Wang, Yegin Genc, and Li-Chiou Chen  
**Journal**: Information Security Journal: A Global Perspective  
**Article ID**: UISS (2575221)  
**DOI**: [10.1080/19393555.2025.2575221](https://doi.org/10.1080/19393555.2025.2575221)  
**Publisher**: Taylor & Francis  
**Year**: 2025

## Abstract

A series of incidents showed that many security threats caused by Twitter spam tweets can reach far beyond the social media platform and impact the real world. Many studies have applied machine learning techniques to classify spam tweets to alleviate such threats. However, Twitter spam detection faces significant challenges due to class imbalance and the evolving nature of spam techniques. This paper proposes a heterogeneous ensemble approach combining dual LSTM networks with a meta-classifier to address imbalanced Twitter spam detection. Our architecture integrates a similarity-based LSTM processing user behavioral features with a word embedding LSTM analyzing semantic textual patterns, followed by an XGBoost meta-classifier trained on disagreed instances. Experiments on two benchmark datasets (1KS10KN and HSPAM) demonstrate that our model outperforms existing baseline models, achieving F1 scores of 0.952 and 0.945, respectively. The precision-focused approach achieves effective performance suitable for social media content moderation requirements while maintaining practical deployment feasibility. The heterogeneous ensemble framework shows strong potential for application to other imbalanced text classification domains beyond spam detection, providing a robust foundation for cybersecurity and content moderation systems.

## Repository Structure

```
hybridSpamTweetDetection/
├── data/                          # Core datasets
│   ├── 1ks-10kn/                 # Main dataset (1K spam, 10K normal users)
│   │   ├── spam.gz               # Raw spam tweet data
│   │   ├── human.gz              # Raw normal tweet data  
│   │   ├── clean.gz              # Cleaned and feature-engineered dataset
│   │   ├── train.gz              # Training dataset
│   │   ├── test.gz               # Testing dataset
│   │   ├── verify/               # Verification experiment datasets
│   │   └── keep_11K/             # Balanced sampling experiments
│   ├── stage/                    # Processed pipeline data
│   │   └── 1ks-10kn/            # Staged data for ensemble modeling
│   ├── icc/                      # Additional evaluation datasets
│   └── hspam/                    # HSPAM14 related data
```

## Dataset Overview

### Primary Dataset: 1KS-10KN
- **Source**: Twitter API collected dataset
- **Composition**: 
  - **Spam users**: 1,000 spam accounts (~142K tweets)
  - **Normal users**: 10,000 legitimate accounts (~1.2M tweets)
- **Features**: 18 engineered features including:
  - **User-based features** (8): verified status, description length, location, follower count, friend count, reputation score, status count, account age
  - **Content-based features** (10): word count, tweet length, capitalized words, exclamation marks, question marks, URLs, hashtags, mentions

### Key Data Files

#### Raw Data
- `data/1ks-10kn/spam.gz`: Original spam tweet collection
- `data/1ks-10kn/human.gz`: Original normal user tweet collection  
- `data/1ks-10kn/clean.gz`: Fully processed dataset with all 18 features

#### Model Training Data
- `data/1ks-10kn/train.gz`: Primary training dataset with similarity features
- `data/1ks-10kn/test.gz`: Primary testing dataset with similarity features
- `data/stage/1ks-10kn/train.gz`: Staged training data with model predictions
- `data/stage/1ks-10kn/test.gz`: Staged testing data with model predictions

#### Experimental Variants
- `data/1ks-10kn/verify/`: Datasets for imbalance verification experiments (10%-100% normal data)
- `data/1ks-10kn/keep_11K/`: Balanced sampling experiments with different spam-to-normal ratios

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

- All data was collected in compliance with Twitter's Terms of Service
- Personal identifiable information has been anonymized
- Dataset is provided for research purposes only
- Commercial use is not permitted

## License

This dataset is provided under the Creative Commons Attribution 4.0 International License (CC BY 4.0) for academic research purposes. See [LICENSE](LICENSE) file for details.

## Contact

For questions about the dataset or research methodology, please contact the corresponding author: Yegin Genc

---

**Note**: If you use the datasets provided in this repository, please ensure proper citation of this work as detailed above.
