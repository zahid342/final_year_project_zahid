# final_year_project_zahid
final year project "Email phishing Detection"
# **Project Topic**
**A Hybrid Machine Learning Approach for Multilingual Phishing Email Detection** 

---

# Overview
This notebook analyzes a phishing email dataset. It performs text preprocessing (tokenization, stopword removal, lemmatization), vectorizes text using TF-IDF and Word2Vec, trains multiple classifiers, and evaluates them using reports, confusion matrices, and ROC analysis.

---

# Dataset
- **Path/URL:** `/content/Phishing_Email.csv` (via `pd.read_csv`)  
- **Target column:** `label`  
- **Feature count/types:** Not specified in notebook  

---

# Features & Preprocessing
- Regex-based text cleaning (`re.sub`)  
- NLTK stopwords removal  
- WordNetLemmatizer()  
- TfidfVectorizer(max_features=5000)  
- gensim Word2Vec(sentences=tokenized_text, vector_size=embedding_dim, window=5, min_count=1, workers=4)  
- WordCloud(width=800, height=400, background_color='white')  

---

# Models
- LogisticRegression (max_iter=1000)  
- LogisticRegression (max_iter=10000)  
- RandomForestClassifier (random_state=42)  
- KNeighborsClassifier (defaults)  
- DecisionTreeClassifier (random_state=42)  
- GradientBoostingClassifier (random_state=42)  

---

# Evaluation
- **Metrics:** classification_report, confusion_matrix, roc_curve, auc  
- **Visualizations:** seaborn plots, matplotlib plots, heatmap, ROC curve, WordCloud  
- **Tuning:** GridSearchCV (parameter grids for multiple models)  

---

# Environment & Requirements
- **Libraries:** gensim, matplotlib, nltk, numpy, pandas, re, seaborn, sklearn, time, wordcloud  
- **Install example:**
  ```bash
  pip install pandas numpy matplotlib seaborn scikit-learn gensim nltk wordcloud
  ```

---

# How to Run
1. Open the notebook in Jupyter/Colab.  
2. Ensure the dataset path `/content/Phishing_Email.csv` is available.  
3. Run all cells in order to reproduce results.  

---

# Methodology (What the Notebook Does)
1. Load the phishing email dataset (`/content/Phishing_Email.csv`).  
2. Clean and normalize text (regex, stopword removal, lemmatization).  
3. Generate features using TF-IDF and Word2Vec.  
4. Split data using `train_test_split` (test_size=0.2, random_state=42, stratify=y).  
5. Train classifiers (Logistic Regression, Random Forest, KNN, Decision Tree, Gradient Boosting).  
6. Evaluate using classification reports, confusion matrices, and ROC curves.  
7. Tune models with GridSearchCV for hyperparameter optimization.  

---

# Outputs You’ll See
- Classification reports  
- Confusion matrix plots (heatmap)  
- ROC curve plots and AUC scores  
- Word cloud visualizations  
- General seaborn/matplotlib EDA plots  

---

# Reproducibility Notes
- train_test_split test_size=0.2  
- train_test_split random_state=42  
- stratify=y  
- random_state=42 consistently applied  

---

# Repository Tip
Maintain a CHANGELOG and version your notebook to track experiments and results.

---

# Attribution
- **Dataset:** `/content/Phishing_Email.csv`  
- **Author:** Notebook/code authored by the student for academic use.  

---

**Last updated:** 2025-08-30
