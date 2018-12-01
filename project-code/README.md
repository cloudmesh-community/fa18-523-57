
# Historical Storm Data Analysis with Cosmos DB

| Authors: Divya Rajendran, Pramod Duvvuri

This project is divided into two components. In the first part, we visualize and analyze the data. In the second part, we use various machine learning algorithms to predict the type of storm given the various features of it as input to our machine learning model.

## Data:

* storm_data.csv - This is the data file which is located in the [*data*](https://github.com/cloudmesh-community/fa18-523-57/tree/master/project-code/data) folder. This file contains more than 190,000 rows. The data will be stored in a Cosmos DB instance and then used for visualizations and applying machine learning techniques

## Requirements

These are the main requirements to setup and run the code.
  1. Microsoft Azure Account
  2. Python 3
  3. Git
  4. Mongo DB

## Installation

Both the authors used a machine running *macOS Mojave Version 10.14.1*, the below steps can be followed to run this code on any operating system.

### Data Setup

This section will help setup a Microsoft Azure account and import data into the Cosmos DB instance.

1. Install all the software requirements listed above (Python 3, Mongo DB, Git)

2. Clone our project repository from GitHub using the following command into a directory

```bash
$ git clone https://github.com/cloudmesh-community/fa18-523-57.git
```

3. Microsoft Azure [*link*](https://portal.azure.com/) offers 200$ credit every month for 12 months for free. We signed up for this trial using an email account. The next step is to create a default resource group before we can create an instance of the Cosmos DB.

   3.1. Click on *Create a Resource* in Azure Portal page on the left hand pane.

   3.2. Under the *Basic* tab use the default resource group you created in Step 1 and     the values for the other fields are as follows:
    *  Subscription: Free Trial
    *  Resource Group: {give-any-name}
    *  Account Name: {give-any-name
    *  API: MongoDB
    *  Location: Central US

    These are the mandatory fields before the instance can be created. The instance takes a few minutes to be created and the Azure Portal will notify you once it has been created.

   3.3. Once we have our instance up and running now we can go ahead and create a    database *test* in our project instance and a collection *storm_data* before we can start to import our data into the Cosmos DB instance using the Mongo API. To create a new database and collection in our Cosmos DB instance we need to navigate to our instance which can be seen on the *Dashboard*. Click on the tab *Data Explorer* on the left hand pane and we should be able to see the GUI option to create a new database. Click on it and create a new database named *test*. Once this step is finished we can create a new collection in our test database. Call the collection *storm_data*.

   3.4. Importing data into our data was a challenge since there was no easy one-button click to do this. To import we need to connect to our Cosmos DB instance using the Mongo Shell, when in the options section of your Cosmos DB instance navigate to the *Connection String* tab and copy the primary connection string to our instance, we can use this connection string to connect to our instance and import data into it. The below command requires you have Mongo DB installed and configured on your machine. Create a new file names *cosmos_db.config* and save it in the code directory of our project. This *cosmos_db.config* file should contain the primary connection string we just copied earlier, we shall use this file to connect to our Cosmos DB instance from our Jupyter Notebook. This config file ensures our credentials are not publicly exposed when our code is pushed onto Github.

    3.5. After successful connection is established we can start to import our data from our local machine to the Cosmos DB instance. To start the data import first navigate to the directory where our data file is located in the git repository we have just cloned earlier. Once in the directory, run the following command:

   3.6. Run in your bash $ mongo {your-connection-string}
   
   3.7. Run in your bash $ mongoimport --host {host-name} -u {user-name} -p {primary-password} --ssl --sslAllowInvalidCertificates --db test --collection storm_data --type csv --file "./storm_data.csv" --headerline --numInsertionWorkers 4 --batchSize 24  

    3.8. Please replace the placeholders with the relevant information of your instance and run the command in the directory where the data file *storm_data.csv* is located. This process will take a while and will output the status to the console. It tooks about 30 minutes to import the data from our machines to the the Cloud. The time depends on the Read Units (RUs) for our instance, RUs cost more money per the minute so the default number when we create an instance in Azure is 400. The highest we can use is 10,000 RUs but this is very costly and uses up our Azure credit.

   3.9. *This option must be used only as an alternative to run the code, we have commented out a line in Jupyter notebooks that connects to our csv data directly using a pandas read command this can also be used to run the code without setting up the Azure instance to connect and fetch the data*

4. The authors used *virtualenv* to create a folder for the project and run the code, the *requirements.txt* file contains all the python packages required to run the code. This was create using the pip freeze command in the virtual environment.

5. The following python packages need to be installed before we can run the code in the Jupyter Notebooks. To simplify this process we provide to options, the user can install using the requirements text file or run the commands in the CLI to install these packages separately.

```bash
$ pip install -r requirements.txt
```
*OR*

```python
pip install jupyter
pip install scipy
pip install numpy
pip install pandas
pip install sklearn
pip install matplotlib
pip install xgboost
pip install folium
pip install pymongo
pip install seaborn
```
6. Run the Code files in the following order
   6.1. Exploratory Analysis of Storm Data.ipynb
   6.2. Machine Learning.ipynb
