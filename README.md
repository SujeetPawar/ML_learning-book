# ML Learning Book Notes

## Description
- This repository contains my machine learning learning journey and chapter-wise notes from:

`Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow (2nd Edition) - Aurelien Geron`

## Setup (For Anyone Using This Repo)

### 1. Clone and move into the project
```bash
git clone https://github.com/SujeetPawar/ML_learning-book.git
cd ML_learning-book
```

### 2. Install system packages (Ubuntu/Debian)
- If `python3 -m venv` fails with an `ensurepip` error, install:
```bash
sudo apt-get update
sudo apt-get install -y python3.12-venv python3-pip
```

### 3. Create and activate virtual environment
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 4. Install dependencies
```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 5. Register Jupyter kernel
```bash
python -m ipykernel install --user --name ml-learning-book --display-name "Python (.venv ml-learning-book)"
```

### 6. Open notebooks in VS Code
1. Install VS Code extensions: `Python` and `Jupyter` (Microsoft).
2. Open any `.ipynb` file.
3. Click `Select Kernel` and choose `Python (.venv ml-learning-book)`.
4. Run cells using `Shift+Enter`.

## Other Ways to Use These Notebooks

### Jupyter Notebook (directly in browser)
```bash
source .venv/bin/activate
jupyter notebook
```

### Google Colab
- Open [https://colab.research.google.com](https://colab.research.google.com)
- Upload any `.ipynb` from this repo and run it directly.
- If needed, install missing packages in a cell:
```python
!pip install numpy pandas matplotlib scikit-learn
```

### Windows Setup (PowerShell)
```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
python -m ipykernel install --user --name ml-learning-book --display-name "Python (.venv ml-learning-book)"
```

## Repository Hygiene
- A `.gitignore` is included to ignore virtual environments, notebook checkpoints, Python cache files, and editor/temp files.

## Chapter-wise Notes

### Chapter 1
- Notes:
- 1.Types of Machine Learning -> supervised learning , unsupervised learning , semi-supervised , online vs batch etc.
  - Supervised/Unsupervised Learning
    - 1.It is based on the supervisions they get during training four major categories
      - A.supervised
        - training set is provided with the desired outcome called `labels`
        - typical example would be classification (spam or not spam)
        - another example would be prediction of numeric values these are called predictors this sort of task is called `regression`
        - Note regression can be used as classification vice-versa.
        - Algorithms: k-Nearest Neighbors , Linear Regression, Logistic Regression , Support Vector Machines (SVMs), Decision Trees and Random Forests , Neural networks
      - B.unsupervised
        - traning set is not provided that is it is unlabeled the system lerns without teacher like us 😮‍💨
        - Algorithms : k-means , DBSCAN , HCA , one-class SVM , Ioslation Forest , PCA, Kernal PCA , Locally Linear Embedding (LLE) , t-Distributed Stochastic Neighbor Embedding (t-SNE), Apriori , Eclat
        - typical example would be to detect similar type of user in your website , visualization algos
        - A dimensity reduction algorithm which is more important here as it is necessary step also unsupervised
      - C.semi-supervised
      - D.Reinforcement
        
