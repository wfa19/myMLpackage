# MyMLpackage

MyMLpackage is a Python package that provides dedicated functions for various operations and settings related to machine learning training. These functions include:

- **Data Preparation**: Functions to prepare data for machine learning tasks.
- **Data Transformation and Scaling**: Functions for transforming and scaling data.
- **Feature Engineering**: Functions for feature engineering tasks.
- **Feature Selection**: Functions to select relevant features for modeling.
- **Modelling**: Functions for building machine learning models.

These functions bundle the inputs into a master data dictionary, which is then passed to the Pycaret setup function for further processing.

## Installation

You can install MyMLpackage from `pip install git+https://github.com/wfa19/myMLpackage.git`

```bash
 pip install git+https://github.com/wfa19/myMLpackage.git

## Usage
import myMLpackage                                               
from myMLpackage import automation_class as ac
from myMLpackage import general_utility as gu
data=gu.load_experimental_dataset('heart')
data['target'] = data['target'].replace({1: 'Heart disease', 0: 'No Heart disease'})
data.head()
## Print data info
data.info()
## Data preparation settings 
### Setting up data types 
 datypess()
### processing missing cases
processs_missing(missing)

