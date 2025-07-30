


![Project image cover](images/dataset-cover-spotify.jpg)











## Machine Learning

This phase of the project focused on building and evaluating predictive models to classify songs into music genres based on their audio features.

### Models Evaluated

- **Random Forest Classifier** – main model used for multi-class genre prediction  
- **K-Nearest Neighbors (KNN)** – used for music recommendation based on similarity in audio features

### Key Techniques Used

- **Label Encoding**: Converted genre labels into numeric format for classification  
- **Standardisation**: Scaled audio features to ensure fair comparison across dimensions  
- **Train/Test Split with Stratification**: Maintained genre distribution across training and test sets  
- **Classification Report & F1-Score Visualisation**: Used to evaluate model performance per genre  
- **Genre Filtering**: Focused on top 15 genres with the highest F1-scores to improve accuracy

### Results Summary

- The initial model struggled with over 100 genres, achieving ~33% accuracy due to high class imbalance and genre overlap  
- After narrowing the focus to the top 15 genres, overall accuracy improved significantly to **88%**  
- Genres like `comedy`, `grindcore`, and `salsa` showed the highest F1-scores, suggesting more distinct audio patterns  
- KNN was also used to recommend songs that are similar in sound by comparing their audio features.

These results demonstrate that focusing on the most distinguishable genres improves model performance and usability for real-world applications such as recommendation engines or music analytics dashboards.

### Next Steps

- Tune model hyperparameters for even better performance  
- Integrate with a user-facing interface or dashboard  
- Explore multi-label classification to reflect songs with blended genres