# ML Learning Book Notes

## Description
This repository contains my machine learning learning journey and chapter-wise notes from:

`Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow (2nd Edition) - Aurelien Geron`

## Setup (For Anyone Using This Repo)

### 1. Clone and move into the project
```bash
git clone <your-repo-url>
cd ML_learning-book
```

### 2. Install system packages (Ubuntu/Debian)
If `python3 -m venv` fails with an `ensurepip` error, install:
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
