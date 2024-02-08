# Telecom customer churn prediction


# Dataset:

**The data set includes information about:**

1. Customers who left within the last month – the column is called Churn.
2. Services that each customer has signed up for – phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies.
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

The model was deployed using the Flask framework along with HTML for the user interface.

```python
app = Flask("__name__")
```

The loadPage method calls our home.html.

```python
@app.route("/")
def loadPage():
	return render_template('home.html', query="")
```
 
The predict method is our POST method, which is called when we pass all the inputs from our front end and click SUBMIT.

```python
@app.route("/", methods=['POST'])
def predict():
```

The run() method of Flask class runs the application on the local development server.

```python
app.run()
```

Awesome, the model is ready, let’s test our bot. The above given Python script is executed from a Python shell.

Go to Anaconda Prompt, and run the below query.

```python
python app.py
```

The below message in the Python shell is seen, which indicates that our App is now hosted at http://127.0.0.1:5000/ or localhost:5000

```python
* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```
  
HERE'S WHAT THE FRONTEND LOOKS LIKE:

![image](https://github.com/MisterAare/telecom_churn_prediction/assets/109184556/fe410163-f63c-4eed-8c30-224d3cb3131d)
