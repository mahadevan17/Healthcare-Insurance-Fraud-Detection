<h2>📊 Machine Learning Component</h2>

<h3>🧠 Healthcare-Insurance-Fraud-Detection</h3>
<p>
This part of the project focuses on detecting fraudulent healthcare insurance claims using supervised Machine Learning techniques. The dataset used is from Kaggle:  
<a href="https://www.kaggle.com/datasets/rohitrox/healthcare-provider-fraud-detection-analysis" target="_blank">Healthcare Provider Fraud Detection Dataset</a>.
</p>

<p><b>Note:</b> <code>Train_Outpatientdata.csv</code> could not be uploaded due to GitHub’s 25MB file size limit.</p>

<p>The dataset consists of 8 files (4 for training, 4 for testing), including Inpatient, Outpatient, Beneficiary, and Target files.</p>

<ul>
  <li><b>Missing Value Handling:</b> Features with more than 50% missing values were dropped. KNN imputation was used for numerical values and random imputation for categorical values.</li>
  <li><b>Data Merging:</b> Beneficiary data was joined with both Inpatient and Outpatient datasets separately. Then, target labels were added accordingly.</li>
  <li><b>Feature Selection:</b> Random Forest was used as a feature selector:
    <ul>
      <li>Threshold of 0.04 was set for Inpatient data (resulting in shape: <code>(40474, 6)</code>)</li>
      <li>Threshold of 0.02 for Outpatient data (resulting in shape: <code>(517737, 12)</code>)</li>
    </ul>
  </li>
  <li><b>Data Scaling:</b> StandardScaler was used for normalization.</li>
  <li><b>Balancing:</b> Oversampling and undersampling techniques were applied to address class imbalance.</li>
  <li><b>Modeling:</b> Random Forest and Decision Tree classifiers were trained and evaluated using F1-score and AUC (Area Under ROC Curve).</li>
</ul>

<h3>🧪 Insurance_Fraud_Detection.ipynb</h3>
<p>
This version followed an alternate preprocessing approach using the same dataset.
</p>

<ul>
  <li><b>Missing Value Handling:</b> This time, features with more than 70% missing values were dropped.</li>
  <li><b>Imputation:</b> KNN for numerical and random imputation for categorical values.</li>
  <li><b>Data Merging:</b> Inpatient and Outpatient were combined, then merged with Beneficiary data using <code>BeneficiaryID</code> and <code>Provider</code>. The resulting dataset was then joined with target values based on <code>Provider</code>.</li>
  <li><b>Feature Selection & Modeling:</b> Random Forest was used for feature importance ranking and the selected features were used for training ML models as in the previous version.</li>
</ul>
