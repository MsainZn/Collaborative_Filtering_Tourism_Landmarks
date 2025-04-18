# Intelligent Travel Recommendations Using Neural Collaborative Filtering for Iranian Landmarks

![GitHub](https://img.shields.io/github/license/MsainZn/Collaborative_Filtering_Tourism_Landmarks?color=blue) 
![GitHub last commit](https://img.shields.io/github/last-commit/MsainZn/Collaborative_Filtering_Tourism_Landmarks)

This repository contains the code, dataset, and implementation details for the research article:  
**"Intelligent Travel Recommendations Using Neural Collaborative Filtering for Touristic Landmarks of Iran"**.

## Abstract
This study introduces a hybrid recommendation system combining **Neural Collaborative Filtering (NCF)** and **Matrix Factorization (MF)** to enhance personalized tourism experiences in Iran. By leveraging demographic and contextual data from 4,177 user-landmark interactions, our model achieves a **test F1 score of 0.84**, **accuracy of 0.90**, and reduces test error from 0.83 to 0.37. Key contributions include:
- A structured dataset of Iranian landmarks, user ratings, and contextual features.
- Mitigation of the cold-start problem using embedding-based recommendations.
- Empirical validation of hybrid models and pre-training strategies.

## Dataset
The dataset comprises three CSV files stored in the [`/dataset`](https://github.com/MsainZn/Collaborative_Filtering_Tourism_Landmarks/tree/master/dataset) directory:

| Table       | Columns                              | Samples | Size  |
|-------------|--------------------------------------|---------|-------|
| **Landmark**  | ID, Name, Category, City, Province, Payment | 309     | 17 KB |
| **Tourist**   | ID, City, Province, Age              | 200     | 5 KB  |
| **Rating**    | User ID, Landmark ID, Rating (1-5)   | 4,177   | 42 KB |

### Preprocessing Steps:
- **Age Binning**: Users categorized into Young (20-39), Middle-aged (40-59), Elderly (60+).
- **Price Categorization**: Landmarks labeled as Free, Inexpensive (<500K IR-Rial), Expensive (>500K IR-Rial).
- **Feature Encoding**: Categorical variables (e.g., provinces, cities) mapped to numeric IDs.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/MsainZn/Collaborative_Filtering_Tourism_Landmarks.git
   cd Collaborative_Filtering_Tourism_Landmarks
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt  # See requirements.txt for specific packages
   ```

## Results
| Model         | Test F1 Score | Test Accuracy | Test Error |
|---------------|---------------|---------------|------------|
| Matrix Factorization (MF) | 0.60          | 0.58          | 0.83       |
| Neural Network (NN)       | 0.83          | 0.88          | 0.39       |
| **Hybrid (NCF-MF)**       | **0.84**      | **0.90**      | **0.37**   |

- **Cold-Start Mitigation**: Feature embeddings improved test recall by 17%.
- **Pre-training Impact**: Hybrid model with pre-trained components converged 30% faster.

## Citation
If you use this work, please cite:
```bibtex
@article {
author = {Zolfagharnasab, Mohammad Hossein and PourMohammadBagher, Latifeh and Bahrani, Mohammad},
title = {Intelligent Travel Recommendations Using Neural Collaborative Filtering for Touristic Landmarks of Iran},
journal = {Journal of Data Science and Modeling},
volume = {},
number = {},
pages = {119-147},
year  = {2025},
publisher = {Allameh Tabataba’i University Press},
issn = {3060-8082}, 
eissn = {2980-9010}, 
doi = {10.22054/jdsm.2025.82861.1059},
url = {https://jdscm.atu.ac.ir/article_18731.html},
eprint = {https://jdscm.atu.ac.ir/article_18731_7b04b80c1b55eacc2a67481dc7df8a4a.pdf}
}	
```

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE.md) for details.

## Contact
For questions or collaborations, contact:  
**Moe Nasab**  
📧 Email: [moe.nasab@atu.ac.ir](mailto:moe.nasab@atu.ac.ir)  
🌐 GitHub: [MsainZn](https://github.com/MsainZn)  

---

**Explore Iran's hidden gems with AI-powered recommendations!**
