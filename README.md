# Telecom customer churn prediction

![Code_qYpVAXuBDQ](https://github.com/MisterAare/telecom_churn_prediction/assets/109184556/1f91ef4d-37d8-48df-832a-59d003576f78)

# Dataset:

**The data set includes information about:**

1. Customers who left within the last month – the column is called Churn.
2. Services each customer has signed up for – phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies.
3. Customer account information – how long they’ve been a customer, contract, payment method, paperless billing, monthly charges, and total charges
4. Demographic info about customers – gender, age range, and if they have partners and dependents.

# Libraries and Frameworks

The Python libraries used in this project include pandas, numpy, scikit-learn, matplotlib, plotly, pickle, Flask, and other related libraries for data manipulation, model building, visualization, and deployment.

# Model Building:

For this project I:

1. Train and Evaluate a Logistic Regression model
2. Train and Evaluate a Random Forest Classifier model
3. Train and Evaluate a K-Nearest Neighbor model
4. Train and Evaluate a Naive Bayes Classifier model
5. Compare the trained models by calculating AUC score and plot ROC curve

![image](https://github.com/MisterAare/telecom_churn_prediction/assets/109184556/7339fe6c-ccb2-4733-b4be-13d9367b2c93)


# Deployment:

The model was deployed using the Flask framework and HTML for the user interface.

```python
app = Flask("__name__")
```

The loadPage method calls our index.html.

```python
@app.route("/")
def loadPage():
	return render_template('index.html', query="")
```
 
The predict method is our POST method when I pass all the inputs from our front end and click SUBMIT.

```python
@app.route("/", methods=['POST'])
def predict():
```

The run() method of Flask class runs the application on the local development server.

```python
app.run()
```

Awesome, the model is ready, time to test my bot. The above given Python script is executed from a Python shell.

to run my application on Google Colab, I run the below query.

```python
from google.colab.output import eval_js
print(eval_js("google.colab.kernel.proxyPort(5000)"))
```

The below message in the Python shell is seen, which indicates that our App is now hosted and I can run it by clicking on the URL

```python
* https://29k4de7ski4-496ff2e9c6d22116-5000-colab.googleusercontent.com/
```

  
HERE'S WHAT THE FRONT-END LOOKS LIKE:

![chrome_KyRJ43SHJW](https://github.com/MisterAare/telecom_churn_prediction/assets/109184556/405b05a5-b81e-4552-bb62-76da3e25cbb6)

