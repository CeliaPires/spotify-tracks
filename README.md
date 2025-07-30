<<<<<<< HEAD
# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

## Template Instructions

Welcome,

This is the Code Institute student template for the Data Analytics capstone project. We have preinstalled all of the tools you need to get started. It's perfectly okay to use this template as the basis for your project submissions. Click the `Use this template` button above to get started.

You can safely delete the Template Instructions section of this README.md file and modify the remaining paragraphs for your own project. Please do read the Template Instructions at least once, though! It contains some important information about the IDE and the extensions we use.

## How to use this repo

1. Use this template to create your GitHub project repo. Click the **Use this template** button, then click **Create a new repository**.

1. Copy the URL of your repository to your clipboard.

1. In VS Code, select **File** -> **Open Folder**.

1. Select your `vscode-projects` folder, then click the **Select Folder** button on Windows, or the **Open** button on Mac.

1. From the top menu in VS Code, select **Terminal** > **New Terminal** to open the terminal.

1. In the terminal, type `git clone` followed by the URL of your GitHub repository. Then hit **Enter**. This command will download all the files in your GitHub repository into your vscode-projects folder.

1. In VS Code, select **File** > **Open Folder** again.

1. This time, navigate to and select the folder for the project you just downloaded. Then, click **Select Folder**.

1. A virtual environment is necessary when working with Python projects to ensure each project's dependencies are kept separate from each other. You need to create your virtual environment, also called a venv, and then ensure that it is activated any time you return to your workspace.
Click the gear icon in the lower left-hand corner of the screen to open the Manage menu and select **Command Palette** to open the VS Code command palette.

1. In the command palette, type: *create environment* and select **Python: Create Environment…**

1. Choose **Venv** from the dropdown list.

1. Choose the Python version you installed earlier. Currently, we recommend Python 3.12.8

1. **DO NOT** click the box next to `requirements.txt`, as you need to do more steps before you can install your dependencies. Click **OK**.

1. You will see a `.venv` folder appear in the file explorer pane to show that the virtual environment has been created.

1. **Important**: Note that the `.venv` folder is in the `.gitignore` file so that Git won't track it.

1. Return to the terminal by clicking on the TERMINAL tab, or click on the **Terminal** menu and choose **New Terminal** if no terminal is currently open.

1. In the terminal, use the command below to install your dependencies. This may take several minutes.

 ```console
 pip3 install -r requirements.txt
 ```

1. Open the `jupyter_notebooks` directory, and click on the notebook you want to open.

1. Click the **kernel** button and choose **Python Environments**.

Note that the kernel says `Python 3.12.8` as it inherits from the venv, so it will be Python-3.12.8 if that is what is installed on your PC. To confirm this, you can use the command below in a notebook code cell.

<<<<<<< HEAD
```console
! python --version
## Hpothesis Testing
```
=======

=======
# **A dataset of Spotify songs with different genres and their audio features**
>>>>>>> 4cba1f27a72b1c0e332ab58e081f3e31e0bdd398


## Exploratory Data Analysis (EDA) Summary

This section visually explores the Spotify dataset to uncover trends, patterns, and relationships in the music data. These insights help guide hypothesis testing and deeper statistical analysis. The objective was to:

- Understand how audio features and popularity are distributed.
- Compare musical genres based on popularity and key audio features.
- Use data visuals to uncover meaningful insights.


### Key Visualizations

**1. Correlation Heatmap**

- Shows how strongly features like popularity, danceability, energy and valence  are related
- Only weak linear relationships are found

**2. Advanced Scatter Plot**

- Plots danceability vs. popularity, with energy shown through color and valence by size
- Result: No clear pattern. Popular songs span many combinations of features

**3. Genre Popularity Bar Chart**

- Compares the average popularity of each music genre
- Result: Pop music stands out with higher popularity, but it is not overwhelmingly dominant


### Main Insights

**Feature Relationships**

- Popularity has weak or no clear correlation with basic audio features like danceability and energy
- Most features are independent from one another
- Popularity is skewed, with only a few tracks achieving very high scores

**Genre Patterns**

- There are noticeable differences in popularity across genres
- Pop tracks generally have higher popularity than most other genres

**Visual Evidence**

- There is no single combination of audio features that guarantees high popularity
- Popular tracks can vary widely in their musical characteristics
- Most tracks fall within moderate ranges across all features


### Implications for Analysis

- Weak correlations call for both Pearson and Spearman correlation tests
- Skewed distributions justify the use of non-parametric tests like the Kruskal-Wallis test
- Genre differences support further analysis through comparative statistical tests

---

### Conclusion

Visual exploration shows that audio features alone offer limited insight into predicting a track's popularity. While pop music tends to be more popular, success comes in many forms. These findings suggest a greater focus on genre classification rather than relying solely on raw audio characteristics.


## **Project introduction**

This is a dataset of Spotify tracks over a range of 125 different genres. Each track has some audio features associated with it. The data is in CSV format which is tabular and can be loaded quickly.

* The dataset can be found in Kaggle: [dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset) 

* License: Database: Open Database, Contents: © Or

* The project aims to analyse music trends and build a recommendation engine.

* **Potential features**:

* Identify trends in music preferences across different demographics.
* Develop a music recommendation system using collaborative filtering.
* Visualise popular songs by genre and time.
* Build an interactive dashboard for exploring music trends.

## Dataset content

* 21 columns
* File type: csv

* **Column description**: 

| **Column** | **Description** |
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


## **Project plan**

* During the ideation and organisation phase, as the Project Manager, brainstormed a series of user stories with milestones and deadlines to ensure that the deadline for completion was met. I also agreed the data cleanse and transformation strategy with the rest of the team.

* Roles were distributed as follows:

| **Role** | **Name**
|-----------------------------------------------------|------------------------------------------------------|
| **Project Management** | Celia |
| **Data Architect** | Natalie |
| **Data Analyst** | Gregory |
| **Data Scientist** | Ivy |


* The detail of the project Kanban board can be found here: [Kanban board](https://github.com/users/CeliaPires/projects/10/views/1)



## **The rationale to map the business requirements to the data visualisations** 

* Placeholder text **Gregory to update**


## **Analysis techniques used**

* **Data visualisation** to identify patterns and communicate insights visually.

* **Hypothesis testing** to assess statistical significance of observed relationships.

* **Data cleaning and preparation** to ensure data quality and integrity before analysis.

* **Feature engineering** to create new variables that add meaning or improve analysis.
=======
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

##  ETL Process (Extract, Transform, Load)

### Extract

The dataset was initially provided in CSV format, containing thousands of Spotify tracks across 125 genres. The structure was clean and well-tabulated, which allowed for a straightforward import using pandas.

At this stage, all columns were loaded, including raw identifiers and audio-related metadata. Our goal was to prepare this dataset for effective exploratory data analysis (EDA), visualization, and machine learning workflows.

### Transform
**Column Pruning**
We removed the track_id column as it served only as a unique identifier for Spotify’s internal system and had no analytical value. This helped reduce dimensionality and declutter the dataset.

**Missing Data**
Upon inspection, we discovered that only three entries contained missing values — a remarkably clean dataset. Since these represented an insignificant portion of the data, they were removed to avoid unnecessary null handling logic during analysis and model training.

**Duplicate Records**
One of the most critical steps involved handling duplicate records. These could arise due to:

• Reissues or remasters

• Appearances of the same track on multiple albums (e.g. original + greatest hits)

• API aggregation from different Spotify endpoints.

We took the following approach; 570 fully duplicated rows were found — these were identical across all columns, not just duplicates by track name or ID. We removed the duplicates while keeping the first occurrence. However, given the relatively low proportion of duplicates (577 out of 114k total records), we saved a copy of the original duplicates for potential future use or inspection.

This cautious approach preserved data integrity while eliminating unnecessary repetition, whilst small.

**Feature Engineering**
To enhance interpretability and enable more effective visualizations and segmentation, we created several binned features from continuous variables:

These bins enabled:
    • Clearer histograms and category-based plots
    • Simplified grouping for aggregation and pivoting
    • Easier interpretation by non-technical stakeholders
This step was particularly useful in exploratory data analysis, allowing us to explore how features like danceability and energy varied across genres or popularity levels.

 **Load**
The transformed dataset was saved as a clean version for future use in modelling, dashboards, and EDA.



## Dashboard

## Hypothesis Tested

This section presents the results of statistical analysis conducted to test two key assumptions about music popularity, using correlation methods and group comparison techniques.

### Hypotheses

1. **Audio Features Hypothesis**
   *Songs with higher danceability and energy tend to be more popular.*

2. **Genre Classification Hypothesis**
   *Pop songs tend to have higher popularity than songs from other genres.*

### Methods Used

The following statistical tests were applied:

- **Pearson Correlation** – Measures linear relationships
- **Spearman Correlation** – Captures rank-based (monotonic) relationships
- **Kendall's Tau** – Useful for handling tied data and smaller samples
- **Independent t-test** – Compares average popularity between pop and non-pop tracks
- **Mann-Whitney U Test** – A non-parametric alternative to the t-test
- **Effect Size (Cohen’s d)** – Assesses practical significance of group differences


### Results and Interpretation

#### Hypothesis 1: Audio Features vs. Popularity

* All correlation tests (Pearson, Spearman, Kendall) show statistically significant but **very weak** relationships between popularity and audio features like danceability, energy and valence.
* Due to the large sample size, even small effects appear statistically significant, but they lack real-world importance.
* **Conclusion**: Danceability and energy have minimal practical impact on popularity. This hypothesis is not supported.

#### Hypothesis 2: Pop Songs vs. Other Genres

* Statistical tests confirm that **pop songs are more popular** than other genres on average. This reinforces the popular narrative among music executives that pop songs tend to have more commercial success.
* The difference is **statistically significant**, and the **effect size is small but meaningful**

* **Conclusion**: Pop tracks do tend to have higher popularity, although the advantage is modest.


### Key Takeaways

* **Correlation does not imply causation**: Audio features alone do not determine popularity.
* **Large datasets can exaggerate significance**: It's important to distinguish between statistical and practical significance.
* **Multi-method approach ensures robustness**: Using several methods strengthens the reliability of results.
* **Genre matters more than individual audio features**: Pop songs generally perform better, but not dramatically.


### Limitations and Future Directions

* The dataset does not include external factors like artist fame, marketing, or release timing.
* Non-linear or interaction effects may exist but are not captured through basic correlation analysis.
* Future research could explore contextual data, and time-based trends to better understand music popularity.


### Final Conclusion

Basic audio features like danceability and energy do not meaningfully predict a song’s popularity. While pop music has a small edge, success is likely driven by a combination of external factors beyond the sound itself.
>>>>>>> spotify

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