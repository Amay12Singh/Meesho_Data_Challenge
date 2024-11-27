# CODS-COMAD Data Challenge (Sponsored by Meesho)

A comprehensive solution for tackling the CODS-COMAD Data Challenge, leveraging state-of-the-art deep learning models to predict attributes for multiple product categories.

---

## Dependencies

Ensure the following dependencies are installed (matching the Kaggle environment):

- **Python Version**: `3.10.14`
- **NumPy Version**: `1.26.4`
- **Pandas Version**: `2.2.3`
- **TensorFlow Version**: `2.16.1`
- **TQDM Version**: `4.66.4`
- **Matplotlib Version**: `3.7.5`
- **Scikit-learn Version**: `1.2.2`

### Installation

To set up the environment, ensure Python `3.10.14` is installed and run the following command to install the dependencies:

```bash
pip install numpy==1.26.4 pandas==2.2.3 tensorflow==2.16.1 tqdm==4.66.4 matplotlib==3.7.5 scikit-learn==1.2.2
```
## How to Run the Training Code

### Steps for Training Models:

#### 1. Model Training Files:
The repository contains three model training files:
- `EfficientNetV2S`
- `Xception`
- `InceptionResNetV2`

#### 2. Configure Paths:
At the start of each file, define the paths for:
- **Image directory** (path to training images)
- **Train.csv** file

Look for comments in the code indicating where to set these paths.

#### 3. Training Recommendations:
- Train **one category at a time** by commenting out the other categories in the `CATEGORY_ATTRIBUTES` section of the code.
- Run the respective script to train the model. The process will generate:
  - **Model files**
  - **Encoders** for the trained category

#### 4. Saving Outputs:
- Download and securely store the model and encoder files generated during training.

---

## How to Run the Prediction Code

### Steps for Generating Predictions:

#### 1. Configure Paths:
At the start of the prediction script (`Prediction_ensemble`), define the paths for:
- **Test image directory** (path to test images)
- **Test.csv** file

#### 2. Model and Encoder Files:
Pre-trained models and encoders are available for download at:  
[Google Drive - Model Files](https://drive.google.com/drive/folders/1Ns17cJCJGXbyW_7zIFmN-7-AtUJzSZOG?usp=drive_link)

The folder contains:
- **Model files** for the 5 categories:
  - Men Tshirts, Sarees, Kurtis, Women Tshirts, Women Tops & Tunics
- **Pre-trained weights** for 3 models:
  - `EfficientNetV2S`, `Xception`, and `InceptionResNetV2`
- **Encoder files** for each category

#### 3. Update File Paths:
Specify the downloaded model and encoder paths in the `Prediction_ensemble` script for each category.

#### 4. Run the Code:
Execute the script. A `Submission.csv` file will be generated, containing predictions for the test set.

---

## Single Model Prediction

For testing predictions with a single model:

1. Use the respective prediction file, e.g., `Prediction_EfficientNet`.
2. Update the paths in the script to include:
   - Model paths for `EfficientNetV2S`
   - Corresponding encoder files
3. Run the script to generate a submission file based only on the selected model.

---

## Notes
- **Efficient Training**: Training one category at a time is recommended for optimal performance.
- **Flexibility**: You can test single-model predictions or use ensemble predictions by updating the paths in the respective scripts.
- **Submission Output**: The output `Submission.csv` file adheres to the competition requirements.
- **Sample Notebook for Men Tshirts category**: The jupyter notebook `efficientnetv2-s-mens-tshirt.ipynb` contains the EfficientNetV2S training code.
