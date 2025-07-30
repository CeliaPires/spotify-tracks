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

```console
! python --version
## Hpothesis Testing
```

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