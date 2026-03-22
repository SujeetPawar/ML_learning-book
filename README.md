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

- #### Notes:
		There are lots of opensource datasets providers follwoing is the list of them 
			- UC Irvine Machine Learning Repository(https://archive.ics.uci.edu/)
			- Kaggle datasets(https://www.kaggle.com/datasets)
			- Amazon’s AWS datasets(https://registry.opendata.aws/)
			- Data Portals(https://dataportals.org/)
			- OpenDataMonitor(https://opendatamonitor.eu/frontend/web/index.php?r=dashboard%2Findex)
			- Quandl(http://quandl.com/)
			- Wikipedia’s list of Machine Learning datasets(https://en.wikipedia.org/wiki/List_of_datasets_for_machine-learning_research)
			- The datasets subreddit (https://www.reddit.com/r/datasets/)

-  #### Pipeline
			- A sequence of data processing components is called a data pipeline. Pipelines are verycommon in Machine Learning systems, since there is a lot of data to manipulate and many data transformations to apply
			- Components typically run asynchronously. Each component pulls in a large amountof data, processes it, and spits out the result in another data store. Then, some timelater, the next component in the pipeline pulls this data and spits out its own output.Each component is fairly self-contained: the interface between components is simplythe data store. This makes the system simple to grasp (with the help of a data flowgraph), and different teams can focus on different components. Moreover, if a com‐ponent breaks down, the downstream components can often continue to run nor‐mally (at least for a while) by just using the last output from the broken component.This makes the architecture quite robust

-  #### Statistics definitions and formula needed
			- Mean : Average value of all samples
				- Formula `Mean = (x1 + x2 + x3 + ... + xn) / n`
				- Explanation Mean tells the center of the data
				- Used to understand average trend and sometimes to fill missing values
			- Median : Middle value after sorting the data if its even average of middle 2 values 
				- Formula `Median = middle value after sorting`
				- Explanation If data has extreme outliers then median is more stable than mean
				- Used in skewed data and missing value handling
			- Mode : Most frequently occurring value
				- Formula `Mode = value with highest frequency`
				- Explanation It shows the most common category or repeated number
				- Used mainly for categorical data
			- Range : Difference between maximum and minimum value
				- Formula `Range = Max - Min`
				- Explanation It gives the total spread of data
				- Used for quick understanding of variability
			- Variance : Average squared distance from the mean
				- Formula `Variance = Σ(xi - Mean)^2 / n`
				- Explanation Larger variance means the data points are more spread out
				- Used to measure data spread and for feature analysis
			- Standard Deviation : Square root of variance
				- Formula `Std = sqrt(Variance)`
				- Explanation It shows spread in the same unit as the original feature
				- Used in scaling and understanding dispersion
			- Covariance : Measures how two variables change together
				- Formula `Cov(X,Y) = Σ[(Xi - Mean(X))(Yi - Mean(Y))] / n`
				- Explanation Positive covariance means both move together and negative means they move in opposite direction
				- Used to study relationship between features
			- Correlation : Standardized measure of relationship between two variables
				- Formula `Corr(X,Y) = Cov(X,Y) / (Std(X) * Std(Y))`
				- Explanation Its value lies between `-1` and `1`
				- Used to find strength of linear relation and feature dependency
			- Percentile : Value below which a given percentage of observations fall
				- Formula `Pth percentile = value below which P percent data lies`
				- Explanation Example 90th percentile means 90 percent of values are below it
				- Used in outlier detection and understanding distribution
			- Quartiles : Values that divide data into four equal parts
				- Formula `Q1 = 25th percentile, Q2 = 50th percentile, Q3 = 75th percentile`
				- Explanation `Q2` is the median
				- Used to summarize spread and detect outliers
			- Interquartile Range (IQR) : Spread of the middle 50 percent data
				- Formula `IQR = Q3 - Q1`
				- Explanation It is less affected by outliers
				- Used for robust outlier detection
			- Z Score : Number of standard deviations a value is from the mean
				- Formula `Z = (x - Mean) / Std`
				- Explanation Positive z score means above mean and negative means below mean
				- Used in standardization and outlier detection
			- Skewness : Measure of asymmetry of data distribution
				- Formula `Skewness = E[(X - Mean)^3] / Std^3`
				- Explanation Positive skew means tail on the right and negative skew means tail on the left
				- Used to understand data distribution shape
			- Kurtosis : Measure of heaviness of tails of a distribution
				- Formula `Kurtosis = E[(X - Mean)^4] / Std^4`
				- Explanation Higher kurtosis means more extreme values in tails
				- Used to study outliers and distribution behavior
			- Probability : Chance of an event happening
				- Formula `P(A) = Number of favorable outcomes / Total outcomes`
				- Explanation Probability value lies between `0` and `1`
				- Used in prediction, uncertainty, and probabilistic models
			- Probability Distribution : Describes how values are distributed with probabilities
				- Formula `Discrete: P(X = x)` and `Continuous: f(x)`
				- Explanation It tells which values are more likely to occur
				- Used in model assumptions and statistical learning
			- Normal Distribution : Bell shaped symmetric distribution around the mean
				- Formula `f(x) = (1 / (Std * sqrt(2pi))) * e^(-((x - Mean)^2 / (2Std^2)))`
				- Explanation Mean median and mode are equal in normal distribution
				- Used in many ML assumptions and preprocessing methods
			- Standardization : Transform data to zero mean and unit variance
				- Formula `x_new = (x - Mean) / Std`
				- Explanation After standardization features become comparable in scale
				- Used before many ML algorithms like linear regression logistic regression and SVM
			- Normalization : Scale values to a fixed range usually `0` to `1`
				- Formula `x_new = (x - Min) / (Max - Min)`
				- Explanation It compresses all values into the same range
				- Used in neural networks and distance based algorithms
			- Outlier : A data point that is far from most other points
				- Formula `Outlier by IQR rule if x < Q1 - 1.5 * IQR or x > Q3 + 1.5 * IQR`
				- Explanation Outliers can strongly affect mean variance and model performance
				- Used in data cleaning and preprocessing
			- Sampling : Selecting a subset from the whole population
				- Formula `Sample ⊂ Population`
				- Explanation We often train ML models on sample data instead of full population
				- Used in train test split and dataset creation
			- Population : Complete set of all possible observations
				- Formula `Population = all observations`
				- Explanation It is the full data we want to understand
				- Used as the original source from which samples are drawn
			- Sample : A smaller subset taken from the population
				- Formula `Sample = selected observations from population`
				- Explanation Statistics are usually calculated on samples
				- Used for training analysis and estimation
			- Central Limit Theorem : Distribution of sample means becomes approximately normal for large sample size
				- Formula `If n is large then sample mean approx follows Normal distribution`
				- Explanation This is important even when original data is not perfectly normal
				- Used in inference confidence intervals and many statistical methods

-  #### Steps for starting ML model 
			- Select a Performance Measure(RSME , MAE)
			- Check the Assumptions
			- Get the Data
			- Create a Test Set
			- Discover and Visualize the Data to Gain Insights
			- Visualizing Geographical Data(OPTIONAL : if not geographical data is present)
			- Looking for Correlations
			- Experimenting with Attribute Combinations
			- Prepare the Data for Machine Learning Algorithms
			- Data Cleaning
			- Handling Text and Categorical Attributes
			- Feature Scaling
			- Transformation Pipelines
			- Select and Train a Model
			- Training and Evaluating on the Training Set
			- Analyze the Best Models and Their Errors
			- Evaluate Your System on the Test Set
			- Launch, Monitor, and Maintain Your System

-  #### Functions in ipynb notebook
			- here only chaper_1_2.ipynb to consider checkout that i have added comments to describe it.

-  #### Definitions and concepts 
			- `Stratified` sampling is a sampling technique in which the population is divided into `distinct subgroups` (called `strata`) based on specific characteristics, and samples are drawn from each group in the same proportion as they exist in the overall population.
			- `One-Hot Encoding` transforms a categorical feature with N unique categories into N new binary features, where each feature represents one category and contains 1 if the observation belongs to that category, otherwise 0.
			- Min-max scaling (many people call this normalization) is the simplest: values are shifted and rescaled so that they end up ranging from 0 to 1. We do this by subtractingthe min value and dividing by the max minus the min. Scikit-Learn provides a transformer called MinMaxScaler for this
			- Standardization is different: first it subtracts the mean value (so standardized valuesalways have a zero mean), and then it divides by the standard deviation so that the resulting distribution has unit variance. Unlike min-max scaling, standardization does not bound values to a specific range, which may be a problem for some algorithms (e.g., neural networks often expect an input value ranging from 0 to 1). However, standardization is much less affected by outliers
			- As with all the transformations, it is important to fit the scalers tothe training data only, not to the full dataset (including the test set).Only then can you use them to transform the training set and the test set (and new data).
			-