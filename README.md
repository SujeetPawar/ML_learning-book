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
		- Here chapter wise Notes which are typed by me forgive typos 😓

### Chapter 1

- #### Notes:
		Machine Learning is the field of study that gives computers the ability to learn without being explicitly programmed.

-  #### Types/Categorization of Machine Learning
		Following are the types of Machine leraning in broader specs

	- ##### Supervised/Unsupervised Learning

			- It is based on the supervisions they get during training four major categories

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
				- Mixture of labelled and ulabelled data mostly time contraint or data availability so combination of supervised and unsupervised 
				- Examples like photo hosting services like google photo 
				- Most algo's are combination of supervised and unsupervised e.g deep belief networks (DBNs) are based on unsu‐pervised components called restricted Boltzmann machines (RBMs) stacked on top of one another. RBMs are trained sequentially in an unsupervised manner, and then the whole system is fine-tuned using supervised learning techniques

			- D.Reinforcement
				- Learning system called as agent in context,  it different ball game from other types it observe in the environment performs actions gets rewards it lerns by itself the best startegy called `policy` in short this policy defines what actions should choose in the given situation.
				- Example Many robots lerant walk by this algo 
		

	- ##### Batch and Online Learning

			- Another critria used to classify ML Systems whether system can learn incremently or not based on that following types are there 

			-A.batch/offline learning 
				- System is incapble of incremental leraning so it must be trained all available data this is called offline leraning 
				- Any new data or new feature for that it is needed to train from scratch from old to new 
				- This might take longer time to train as well as heavy computings better option is to use those are capable of incremental learning 

			-B.online leraning
				- In this data is trained incrementally by feeding data instances sequentially 
				- It is great for where data is continusoly feded or receives like stock markets and all and have limited compute power
				- It can be used where huge data that can't be saved on memory of machine's (this is called out-of-core learning [ps: out of core is done offline it just that it uses online method])
				- One imp parameter is how fast it adapts this is called `learning rate`
				- Challeges like if leraning rate is too fast it will tend to forget old too slow then intertia of data is stagent also if bad patch of data comes it will drop the quality and malfunction 


	- ##### Instance-Based Versus Model-Based Learning

			- Based on how they generlize(predicts in simpler terms) there is Categorization of it.

			-A.Instance-based learning
				- Most trivial , match and flag not the best but not the worst 
				- It learns by the example given so there might cases it falsely do the job
			
			-B.Model-based learning
				- Another way is Build the model based on the example and then predict 
				- Here the cost function is for how bad it predicts 

-  #### Challenges of Machine Learning
		- Following are challeges or ML

	- ##### Insufficient Quantity of Training Data

	- ##### Nonrepresentative Training Data

	- ##### Poor-Quality Data

	- ##### Irrelevant Features

			- Here the feature engineering comes in picture as feature selection , extraction needed to happen.
	
	- ##### Overfitting the Training Data
			
			- Overfitting happens when the model is too complex relative to the amount and noisiness of the training data
			- Solution is Reduce Noise , Simplyfy , Gather more to train
			- Constraining a model to make it simpler and reduce the risk of overfitting is called `regularization`.
			-The amount of regularization to apply during learning can be controlled by a `hyper‐parameter`. A hyperparameter is a parameter of a learning algorithm (not of the model).
	
	- ##### Underfitting the Training Data

			- It occurs when your model is too simple to learn the underlying structure of the data.
			- Solution is More powerful model , better feature modeling and algo's , reduce the constraints(regularization , hyper-parameters)
			

-  #### Testing and Validating

		- The most important thing is to Now evaluate what you have build the model and all for that 
		- Common is using 20% data as for test and 80% for actually works but is depends on the volume of the data 
	
	- ##### Hyperparameter Tuning and Model Selection

			- Check the generalisation error and based on that select the appropriate model 
	
	- ##### Data Mismatch

			-  large of amount data but not we needed in the prod 






### Chapter 2