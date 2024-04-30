# MyMLpackage

MyMLpackage is a Python package that provides dedicated functions for various operations and settings related to machine learning training. The package consists the following modules:

- **General utility** General Function to support other functions in graphing etc
- **Data Preparation**: Functions to prepare data for machine learning tasks.
- **Data Transformation and Scaling**: Functions for transforming and scaling data.
- **Feature Engineering**: Functions for feature engineering tasks.
- **Feature Selection**: Functions to select relevant features for modeling.
- **Modelling**: Functions for building machine learning models.
- **Prediction** Functions to make predictions using the trained model
- **Automation class** A python class which can be initialized with data and inputs to automate ML training.
- **Data** A python class which can be initialized with data and inputs to automate ML training.

most of these modules bundle the inputs into a master data dictionary, which is then passed to the Pycaret setup function for further processing.

## Installation

You can install MyMLpackage from `pip install git+https://github.com/wfa19/myMLpackage.git`

```bash
 pip install git+https://github.com/wfa19/myMLpackage.git
```
## Usage
```bash
import myMLpackage                                               
from myMLpackage import general_utility as gu
from myMLpackage import Data_preparations as dp
from myMLpackage import automation_class as ac

data=gu.load_experimental_dataset('heart')
data['target'] = data['target'].replace({1: 'Heart disease', 0: 'No Heart disease'})
data.head()
```
## Print data info
```bash
data.info()
```
## Data preparation settings 
### Setting up data types 
```bash
 datypess()
```
### processing missing cases
```bash
processs_missing(missing)
```
### Set up outlier processing 
```bash
processs_outliers(remov_outliers='Yes',outliers_method="iforest",thresh=0.05)
```
see documentation about the other modules

```bash
help(myMLpackage)  # Package documentation
help(myMLpackage.general_utility) # general utility module documentation
help(myMLpackage.Data_preparations) # data preparation module documentation
```
## Automated Class
MyMLpackage features an automated class that initializes with data and inputs for training, tuning, evaluating, and visualizing ML models. This class streamlines the machine learning workflow and provides convenient methods for managing the entire process.

### using automation class
Minimal initialization
```bash
model=ac.Modelling(data,'target')
```

### get model configuration
```bash
model.model_configs_info
```
### see data information
```bash
model.calculate_variable_info()
```
### See trained model type
```bash
model.determine_model_type()
```
### Graph categorical target
```bash
model.plot_countplot()
```



