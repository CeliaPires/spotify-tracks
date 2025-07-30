# **A dataset of Spotify songs with different genres and their audio features**


![Project image cover](images/dataset-cover-spotify.jpg)


## **Project introduction**

This is a dataset of Spotify tracks over a range of 125 different genres. Each track has some audio features associated with it. The data is in CSV format which is tabular and can be loaded quickly.

* The dataset can be found in Kaggle: [dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset) 

* License: Database: Open Database, Contents: © Or

## Dataset content

* 21 columns
* File type: csv

* **Column description**: 

| **Milestone** | **Task** |
|-----------------------------------------------------|------------------------------------------------------|
| **track_id** | the Spotify ID for the track |
| **artists** | The artists' names who performed the track. If there is more than one artist, they are separated by a ; |
| **album_name** | the album name in which the track appears |
| **track_name** | name of the track |
| **popularity: The popularity of a track is a value between 0 and 100, with 100 being the most popular** | the popularity is calculated by algorithm and is based, in the most part, on the total number of plays the track has had and how recent those plays are. Generally speaking, songs that are being played a lot now will have a higher popularity than songs that were played a lot in the past. Duplicate tracks (e.g. the same track from a single and an album) are rated independently. Artist and album popularity is derived mathematically from track popularity. |
| **duration_ms** | the track length in milliseconds |
| **explicit** | whether or not the track has explicit lyrics (true = yes it does; false = no it does not OR unknown) |
| **danceability** | danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable |
| **energy** | energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale |
| **key** | the key the track is in. Integers map to pitches using standard Pitch Class notation. E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. If no key was detected, the value is -1 |
| **loudness** | the overall loudness of a track in decibels (dB) |
| **mode** | mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0 |
| **speechiness** | speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks |
| **acousticness** | a confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic |
| **instrumentalness** | predicts whether a track contains no vocals. "Ooh" and "aah" sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly "vocal". The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content |
| **liveness** | detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live |
| **valence** | a measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry) |
| **tempo** | the overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration |
| **time_signature** | an estimated time signature. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure). The time signature ranges from 3 to 7 indicating time signatures of 3/4, to 7/4. |
| **track_genre** | The genre in which the track belongs |

##  Ethics, GDPR, and Compliance

### Data Ethics
While this dataset focuses on audio features and metadata of Spotify tracks, ethical considerations still apply. We have ensured that the use of the dataset aligns with ethical AI and machine learning principles, including fairness, transparency, and accountability.

### GDPR & Personal Data
This dataset does not contain any personally identifiable information (PII) or user data, and therefore is **not subject to GDPR** (General Data Protection Regulation) in its current form. However, if combined with user data (e.g., listening history, recommendations), in the future we will ensure that permissions, storage and use of the data complies with GDPR

### Legal Usage
The dataset originates from publicly accessible Spotify metadata but does not include raw audio. Any changes to the data set we would ensure that;
- it complies with Spotify’s [Developer Terms of Service](https://developer.spotify.com/terms/)
- There is no attempt to redistribute the dataset as-is or claim ownership of the data

### Compliance Considerations
- There is  no attempt to reverse-engineering or using the data in a way that violates Spotify's API terms or copyright laws.
-  Licensing rules have been adhered to in the event this dataset is used alongside other music-related content or services.
- If deploying models using this dataset (e.g., in production systems), we will document data sources and ensure data lineage is clear and compliant with relevant regulations.











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