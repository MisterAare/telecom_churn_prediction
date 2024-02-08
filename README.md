# Telecom customer churn prediction


# Dataset:

**The data set includes information about:**

a. Customers who left within the last month – the column is called Churn
b. Services that each customer has signed up for – phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies
c. Customer account information – how long they’ve been a customer, contract, payment method, paperless billing, monthly charges, and total charges
d. Demographic info about customers – gender, age range, and if they have partners and dependents

# Libraries and Frameworks:

# Model Building:

# Deployment:

The model was deployed using the Flask framework along with HTML for the user interface.

app = Flask("__name__")

The loadPage method calls our home.html.

@app.route("/")
def loadPage():
	return render_template('home.html', query="")
 
The predict method is our POST method, which is called when we pass all the inputs from our front end and click SUBMIT.

@app.route("/", methods=['POST'])
def predict():

The run() method of Flask class runs the application on the local development server.

app.run()

Awesome, the model is ready, let’s test our bot. The above given Python script is executed from Python shell.

Go to Anaconda Prompt, and run the below query.

python app.py

The below message in the Python shell is seen, which indicates that our App is now hosted at http://127.0.0.1:5000/ or localhost:5000

* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
  
HERE'S HOW OUR FRONTEND LOOKS LIKE:

![image](https://github.com/MisterAare/telecom_churn_prediction/assets/109184556/fe410163-f63c-4eed-8c30-224d3cb3131d)
