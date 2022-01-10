
# Credit Card Defaulters Prediction



## Introduction


To build a classification methodology to determine whether a person defaults the credit card payment for the next month. 

Recently, the state vigorously promotes the economic construction of large- and medium-sized cities, which not only improves people’s living standards but also changes people’s consumption concept and consumption mode. People are more and more inclined to spend ahead of time and mortgage their “credit” to the bank to enjoy certain things in advance. However, when consuming, people often lack rational thinking and overestimate their ability to repay loans to banks in time. On the one hand, it increases the loan risk of banks; on the other hand, it increases the credit crisis of consumers themselves . With a large number of banks selling credit cards, the phenomenon of credit card default emerges one after another. It is very important for banks to effectively identify high-risk credit card default users.

In this project,On multiple parameters we predict Whether a person shall default in the credit card payment or not.



## Project Architecture :
![architecture](https://user-images.githubusercontent.com/72031522/148733619-752dbac8-9ded-4aed-a652-d8d98950e23c.jpg)

## Data Description

The client will send data in multiple sets of files in batches at a given location. The data has been extracted from the census bureau. 

Labels:

-   1.]LIMIT_BAL: continuous.Credit Limit of the person.
-   2.]SEX: Categorical: 1 = male; 2 = female
-   3.]EDUCATION: Categorical: 1 = graduate school; 2 = university; 3 = high school; 4 = others
-   4.]MARRIAGE: 1 = married; 2 = single; 3 = others
-   5.]AGE-num: continuous. 
-   6.]PAY_0 to PAY_6: History of past payment. We tracked the past monthly payment records (from April to September, 2005)
-   7.]BILL_AMT1 to BILL_AMT6: Amount of bill statements.
-   8.]PAY_AMT1 to PAY_AMT6: Amount of previous payments. 

Target Label:

Whether a person shall default in the credit card payment or not.

-   default payment next month:  Yes = 1, No = 0.



## Demo
- Now first see the project folder structure:
![folder_structure](https://user-images.githubusercontent.com/72031522/148736464-362f3e66-c550-416a-9e02-d5617e9ede20.png)
----------------
- main.py is the entry point of our application, where the flask server starts
![main](https://user-images.githubusercontent.com/72031522/148736617-842d3206-cd9e-4f1b-90f8-6f0d630ca5aa.png)
---------------

- This is the predictionFromModel.py file where the predictions take place based on the data we are giving input to the model
![predFromModel](https://user-images.githubusercontent.com/72031522/148736903-bdaccf5b-c459-493a-b40d-9467f9ad1653.png)
------------------


- Now run the main.py file which is entry point of application, The web app link is created by flask,Open the link in browser.
![host_link](https://user-images.githubusercontent.com/72031522/148737091-d07d9cd1-04be-4139-bd44-bc9d2d1b1d77.png)

-Open this link in browser, The Home Page of web app will open:
![HomePage](https://user-images.githubusercontent.com/72031522/148740742-36babca7-6db5-48a6-9b27-656e33a5747f.png)

--------------


- Now enter the folder directory where batch files are stored And click on predict.
![batchfilespredictpath](https://user-images.githubusercontent.com/72031522/148741515-185ae239-95ee-45c3-aee9-42a4645e0471.png)


- predictions:
![prediction](https://user-images.githubusercontent.com/72031522/148741682-f7a7cf13-c423-44b3-8878-4f5a2f3b6005.png)

All the files from batch directory are extracted and the data is saved on sql server. After that from sql server all data extracted in single '.csv' file. 
First Data from csv file sent to clustering algorithm and as per the cluster number final predictions are made from differnt differnt ML algorithms as per the cluster.
At the end all the predictions from all ML algorithms are saved in single CSV file in defined directory.

![prediction_output](https://user-images.githubusercontent.com/72031522/148742275-f29ea7d2-1b4c-4d3b-b1f2-172dc4321a8f.png)














## Installation

- The Code is written in Python 3.6.10. If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. 
- The all code written through Moduler approach.I suggest to use PyCharm IDE as it is well designed for python.
- Modular programming is a software design technique that emphasizes separating the functionality of a program into independent, interchangeable modules, such that each contains everything necessary to execute only one aspect of the desired functionality.
- Therefore in this project for each funtion different module is made and we just have to import required modules where it is required
- To install the required packages and libraries, run this command in the project directory after cloning the repository.

```bash
pip install -r requirements.txt
```


    
## Deployement on Heroku

Login or signup in order to create virtual app. You can either connect your github profile or download ctl to manually deploy this project.

[![](https://i.imgur.com/dKmlpqX.png)](https://heroku.com)

Our next step would be to follow the instruction given on [Heroku Documentation](https://devcenter.heroku.com/articles/getting-started-with-python) to deploy a web app.

## Technologies Used

![](https://forthebadge.com/images/badges/made-with-python.svg)

[<img target="_blank" src="https://flask.palletsprojects.com/en/1.1.x/_images/flask-logo.png" width=170>](https://flask.palletsprojects.com/en/1.1.x/) [<img target="_blank" src="https://number1.co.za/wp-content/uploads/2017/10/gunicorn_logo-300x85.png" width=280>](https://gunicorn.org) [<img target="_blank" src="https://scikit-learn.org/stable/_static/scikit-learn-logo-small.png" width=200>](https://scikit-learn.org/stable/)

[![Heroku](https://github.com/jalbertsr/logo-badge-images/blob/master/img/rsz_heroku.png?raw=true)](https://www.heroku.com/)

[![Python](https://github.com/jalbertsr/logo-badge-images/blob/master/img/rsz_python.png?raw=true)](https://www.python.org/)

<a title="Marc Garcia, BSD &lt;http://opensource.org/licenses/bsd-license.php&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Pandas_logo.svg"><img width="128" alt="Pandas logo" src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Pandas_logo.svg/128px-Pandas_logo.svg.png"></a>

<a title="JetBrains, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:PyCharm_Icon.svg"><img width="128" alt="PyCharm Icon" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/PyCharm_Icon.svg/128px-PyCharm_Icon.svg.png"></a>





## Bug / Feature Request

If you find a bug (the website couldn't handle the query and / or gave undesired results), kindly open an [issue](https://github.com/Mandal-21/Flight-Price-Prediction/issues) here by including your search query and the expected result
## Future Scope

* Optimize Flask app.py
* Front-End 

## Deployed Heroku app link 
App link : https://credit-card-defaulters646.herokuapp.com/
