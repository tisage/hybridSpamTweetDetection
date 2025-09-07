# A Hybrid Ensemble Method for Imbalanced Spam Tweet Detection

## Paper Information

**Title**: A Hybrid Ensemble Method for Imbalanced Spam Tweet Detection  
**Journal**: Information Security Journal: A Global Perspective  
**Status**: This paper is submitted to Information Security Journal: A Global Perspective and under the review process.  
**Authors**: [To be disclosed upon acceptance]

## Abstract

This repository contains the datasets used in our research paper on spam tweet detection using a hybrid ensemble approach. The proposed method combines dual LSTM models (Similarity-based LSTM and Word Embedding LSTM) with an XGBoost meta-classifier to effectively handle imbalanced tweet data. Our two-layer ensemble architecture demonstrates superior performance compared to traditional machine learning approaches.

## Repository Structure

```
tweetBot/
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


## Citation

```bibtex
@article{YourPaper2024,
  title={A Hybrid Ensemble Method for Imbalanced Spam Tweet Detection},
  author={[To be disclosed upon acceptance]},
  journal={Information Security Journal: A Global Perspective},  
  year={2025},
  note={Under review}
}
```

## Data Availability and Ethics

- All data was collected in compliance with Twitter's Terms of Service
- Personal identifiable information has been anonymized
- Dataset is provided for research purposes only
- Commercial use is not permitted

## License

This dataset is provided under the Creative Commons Attribution 4.0 International License (CC BY 4.0) for academic research purposes.

## Contact

For questions about the dataset or research methodology, please contact the corresponding author after paper acceptance.

---

**Note**: The complete model implementation code, training scripts, and evaluation notebooks will be made publicly available upon acceptance of the research paper. This repository currently contains the processed datasets and documentation to support reproducibility of our research findings.