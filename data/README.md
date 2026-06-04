# NyayaAnumana


The NyayaAnumana directory is organized into three types(train, validation and text), each containing data for different stages of model training and evaluation:

1. **train**: Contains the training dataset required for model training, organized into:
	 - binary: Data for binary classification tasks.
	 - ternary: Data for ternary classification tasks.
2. **dev**: Contains the validation dataset for model training, organized into:
	 - binary: Data for binary classification tasks.
	 - ternary: Data for ternary classification tasks.
3. **test**: Contains the test dataset used to evaluate the model, organized into:
	 - binary: Data for binary classification tasks.
	 - ternary: Data for ternary classification tasks.
 
 ## CSV File types
 
The CSV files within each subfolders of dev, test, and train are categorized based on the sources of the cases:
 1. Data from the Supreme Court only.(csv file with prefix *"CJPE_ext_SCI_"*).
 2. Data from the Supreme Court and High Courts.(csv file with prefix *"CJPE_ext_SCI_HCs_"*).
 3. Data from the Supreme Court, High Courts, and Tribunal Courts. (csv file with prefix *"CJPE_ext_SCI_HCs_Tribunals_"*).
 4. Data from the Supreme Court, High Courts, Tribunal Courts, and Daily Orders from District Courts(csv file with prefix *"CJPE_ext_SCI_HCs_Tribunals_daily_orders_"*).
 
 ## Usage instructions:
 
To train and evaluate models(in classification_prediction folder in parent directory), use the datasets from the NyayaAnumana folder as follows:
 
1. Navigate to the train,dev and test types to select the data based on the classification task you wish to perform (binary or ternary).
	- **Binary Classification Task**: Fine-tuning models to classify a given case as either accepted (label-1/class-1) or rejected (label-0/class-0).

	- **Ternary Classification Task**: Fine-tuning models to classify a given case into one of three classes:
	   - *Rejected* (label-0/class-0): Cases where single or multiple judgments are present, all are rejected.
	   - *Accepted* (label-1/class-1): Cases where single or multiple judgments are present, all are accepted.
	   - *Multi-label* (label-2/class-2): Cases where multiple judgments are present, with some accepted and some rejected.
   
 - (Optional)  For consistency, you may choose to use the same csv type (from csv types mentioned in CSV File types header e.g., SCI only) across the training, validation, and test datasets. While different court types can be used, maintaining consistency can help ensure more reliable model performance.
 
 - Make sure to select the appropriate CSV files for each dataset type to match your classification task and ensure compatibility with the classification_prediction folder requirements.

## Access the Dataset
The dataset is **free to use for academic research purposes**. Commercial usage of the dataset is strictly prohibited.

### How to Request Access
All the datasets in [Hugging Face L-NLProc: Legal Natural Language Processing](https://huggingface.co/L-NLProc) collection [L-NLProc/NyayaAnumana-and-InLegalLegalLlama Datasets](https://huggingface.co/collections/L-NLProc/nyayaanumana-and-inlegalllama-dataset)

---

## Terms of Use
By requesting access, you agree to the following terms:
1. The dataset will be used **ONLY for research purposes**.
2. You will **NOT use the dataset for any commercial purposes**.
3. You will **NOT share the dataset publicly or upload it to any online platforms**.

Failure to comply with these terms may result in the revocation of access and legal actions.

---

	 
 ### NOTE
 
1. While training, specifically for binary classification tasks, you can use **binary_multi_train** datasets. These are intended for experimental purposes, merging **Multi-label (label-2/class-2)** cases into the **Accepted** label from the ternary classification task. You may choose to use or disregard these datasets based on your experimental needs.

2. During testing also, we used 2020_2024_single, a temporal test set designed to evaluate model performance on recent case descriptions. This set includes data from January 2020 to April 2024, covering various court types (Supreme Court of India, High Courts, Tribunals, and Daily Orders). This dataset is provided to assess how the model performs on more recent cases, as other CSV files are limited to data up to December 2019.
 
