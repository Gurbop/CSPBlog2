---
comments: true
layout: post
title: Data Structures Writeup
comments: true
courses: { "compsci": {"week": 27} }
type: tangibles
---

## Collections:
From VSCode using SQLite3 Editor, show your unique collection/table in database, display rows and columns in the table of the SQLite database.
<img width="1279" alt="Screenshot 2024-04-23 at 10 20 40 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/5ccf3371-3022-407c-8b59-e824bf309b1b">
This table displays a list of all the tournaments a user saves.

From VSCode model, show your unique code that was created to initialize table and create test data.
<img width="857" alt="Screenshot 2024-04-23 at 10 21 32 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/78321367-4f4b-45d9-b150-801108f6dfaa">
<img width="828" alt="Screenshot 2024-04-23 at 10 22 02 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/d2142a13-2e38-47de-9dfe-d1c7892ae2b5">
This code initializes a table with the columns uid, id, and tournament name, the test values are passed with the tournament name of clash 1 and clash 2. It creates a relationship between the user id to the tournament name.

## Lists and Dictionaries
In VSCode using Debugger, show a list as extracted from database as Python objects.
<img width="1166" alt="Screenshot 2024-04-17 at 5 16 58 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/bf903069-44ed-4017-855c-5cc751104983">
When I step through the debugger it starts here where the tournament list is being extracted as a python json object.

In VSCode use Debugger and list, show two distinct example examples of dictionaries, show Keys/Values using debugger.
<img width="697" alt="Screenshot 2024-04-17 at 5 18 22 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/9ef6e50c-c797-47d7-a329-bee84177889e">
This shows two dictionaries of the data  with attributes like uid and tournament name.

## APIs and JSON:

In VSCode, show Python API code definition for request and response using GET, POST, UPDATE methods. Discuss algorithmic condition used to direct request to appropriate Python method based on request method.
<img width="782" alt="Screenshot 2024-04-17 at 5 21 37 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/3b3e71b5-fc8d-4ad5-aea1-1d0d26ba18b1">

This code snippet shows a part of a web API for managing "tours" within a system. The post method adds a new tour with an ID and name to a database when called. The get method retrieves all tours from the database and formats them into a JSON response.

In VSCode, show algorithmic conditions used to validate data on a POST condition.
<img width="795" alt="Screenshot 2024-04-17 at 5 22 28 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/8484eb7b-774a-4ae1-b4bc-903381d16e6d">
These are the parameters required to make a user as there is a minimum characters on the username and password.

In Postman, show URL request and Body requirements for GET, POST, and UPDATE methods.
<img width="860" alt="Screenshot 2024-04-17 at 5 27 11 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/7f68996b-7cfa-4f75-97a2-151a3374bb51">

In Postman, show the JSON response data for 200 success conditions on GET, POST, and UPDATE methods.
<img width="863" alt="Screenshot 2024-04-17 at 5 27 57 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/bd441b0b-e920-48d2-817f-7948fb05d6c8">
<img width="639" alt="Screenshot 2024-04-17 at 5 28 18 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/7b804964-fdc1-40ce-baf1-abc526e40eef">

In Postman, show the JSON response for error for 400 when missing body on a POST request.
<img width="586" alt="Screenshot 2024-04-17 at 5 28 36 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/64f78092-3b2b-4dc0-9841-a7fb9f1ffaf6">
<img width="828" alt="Screenshot 2024-04-17 at 5 28 58 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/b9e2ae1e-146b-445d-ad59-dede22f7c420">

In Postman, show the JSON response for error for 404 when providing an unknown user ID to a UPDATE request.
<img width="878" alt="Screenshot 2024-04-17 at 5 37 45 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/19c44bfe-df5a-43f3-bfc1-fe5dd3ecde0e">
<img width="621" alt="Screenshot 2024-04-17 at 5 38 02 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/59ca22bc-4752-44e0-b6c3-4e876d220b05">

Postman is used to test API requests between a user and the backend. Based on what data is being ran with POST, GET, UPDATE, or DELETE, different errors or success will occur.
## Frontend:
In Chrome inspect, show response of JSON objects from fetch of GET, POST, and UPDATE methods.	
![Screenshot 2024-04-18 2 42 41 PM](https://github.com/Gurbop/CSPBlog2/assets/142458920/bb20b43f-2817-41dd-adfb-e1086c5121e3)
This response happens when the user searches for a tournament. Based on the name a GET request will be sent to a clash royale API that will send back JSON objects matching what the user wants.
In the Chrome browser, show a demo (GET) of obtaining an Array of JSON objects that are formatted into the browsers screen.
I will demo getting the leaderboard data from the clash royale API
<img width="1440" alt="Screenshot 2024-04-23 at 10 36 33 PM" src="https://github.com/Gurbop/CSPBlog2/assets/142458920/33a0afbe-bc85-4649-8144-ceae81f6fe56">
An array of json objects that has information on different tournaments is obtained using a GET request to a clash royale API. This information is formatted into a table so a user can see it.

In JavaScript code, describe fetch and method that obtained the Array of JSON objects.
![Screenshot 2024-04-18 2 46 47 PM](https://github.com/Gurbop/CSPBlog2/assets/142458920/02a1513e-5456-444e-9a4b-ea38eafd8112)
This code fetches JSON data from the clash royale API so it can be through interactions in order to be displayed.

In JavaScript code, show code that performs iteration and formatting of data into HTML.
![Screenshot 2024-04-18 2 57 03 PM](https://github.com/Gurbop/CSPBlog2/assets/142458920/fe2b5bf0-a0e5-4efc-a760-8f161b7c358b)
This code loops through the array of JSON objects and displays them in an HTML table based on what the data is representing. For example players, name duration, and rewards.

In the Chrome browser, show a demo (POST or UPDATE) gathering and sending input and receiving a response that show update. Repeat this demo showing both success and failure.

I will demo searching the leaderboard without the backend running for failure and a demo for success.
![Screenshot 2024-04-18 3 14 19 PM](https://github.com/Gurbop/CSPBlog2/assets/142458920/6a64f68b-b88f-48c5-9382-cee8c937043b)
![Screenshot 2024-04-18 3 13 05 PM](https://github.com/Gurbop/CSPBlog2/assets/142458920/b99e48b3-b6a4-4b0d-bfd0-902818a51199)
Without the backend running the requests can't be sent causing errors.

In JavaScript code, show and describe code that handles success. Describe how code shows success to the user in the Chrome Browser screen.
![Screenshot 2024-04-18 2 57 03 PM](https://github.com/Gurbop/CSPBlog2/assets/142458920/ab21500e-26a1-4e33-b7c5-dd75c8c43043)
Upon success, a table with information will be displayed, and if data is saved it will be sent to the backend database. 200 code in terminal/console.

In JavaScript code, show and describe code that handles failure. Describe how the code shows failure to the user in the Chrome Browser screen.
![Screenshot 2024-04-18 3 03 43 PM](https://github.com/Gurbop/CSPBlog2/assets/142458920/5510e3b3-a841-43e1-b2d0-3cf126cd9033)
This code does error handling notifying the user when an error occurs and in console outputs wether the code(400,403,404,500)

## Extras:
Show algorithms and preparation of data for analysis. This includes cleaning, encoding, and one-hot encoding.
![Screenshot 2024-04-18 3 07 28 PM](https://github.com/Gurbop/CSPBlog2/assets/142458920/b2b2fc77-9ea1-4c06-9652-ab3d6a9ce0da)
 When an instance of the datamodel class is created, it tries to load a machine learning model from a file using Python's pickle module; if the model file isn't found or isn't a logistic regression model, it initializes a new logistic regression model. It also reads data from a CSV file into a pandas DataFrame. The class includes methods to display the head of the data, preprocess the data.

Show algorithms and preparation for predictions.
![Screenshot 2024-04-18 3 08 16 PM](https://github.com/Gurbop/CSPBlog2/assets/142458920/50513193-c5ec-44ca-b7df-f9edc7aaa706)
The preprocess_data method prepares the data for modeling by setting certain columns as features and a target variable. The train_model method invokes data preprocessing and then presumably trains the logistic regression model. The predict method uses the trained model to make predictions given new input data, and there are also methods to add new data to the existing dataset (add_data) and retrieve the current dataset (get_data).

Discuss concepts and understanding of Linear Regression algorithms.

Linear regression is a statistical method used to model the relationship between a dependent variable and one or more independent variables by fitting a linear equation to observed data. The main goal is to find a straight line that best predicts the dependent variable based on the values of the independent variables.
Discuss concepts and understanding of Decision Tree analysis algorithms.

Decision tree analysis is a machine learning method that models decisions and their possible consequences as a tree-like structure, where each branch represents a choice between alternatives. The algorithm splits the data into branches at decision nodes, based on feature values that lead to the most distinct subsets, aiming to classify or predict the outcome accurately. 

Summary:
My feature uses API requests from clash royales database to display data the user wants, tournaments/challanges, and a user can save a tornament and it will be stored in my own database under the users account.