# DATAPROJECT-SQL

## Table of contents
-  Aim
-  Download Data
-  Setup
-  How To run
-  Output
-  Note

## Aim

The aim of this project is to load csv into the database and
get the json file with the help of SQL queries in postgres.

## Download Data

To get the data please visit the [link](https://data.gov.in/resources/company-master-data-maharashtra-upto-28th-february-2019)

## Setup

1. First clone this repository 
2. Create virtual Environment
3. After that put the downloaded csv file into the cloned folder.
4. Install all the requirements required to run this project by:
```
$ pip install -r requirements.txt

```
##  How To Run

1. First you have to go in database environment by following command
   ```
   sudo -u postgres psql
   ```
2. then create role and data base by running the create script
    ```
    \i sql_script/create.sql
    ```
3. After that exit the postgres by typing <b>\q</b>
   
4. Then run models.py for defining our schema.
    ```
    $ python3 models.py
    ```
5. After that run db.py for loading csv to database(Takes approx 2-3 minutes)
    ```
    $ python3 db.py
    ```
6. Finally run company_master.py for performing transactions
    ```
    $ python3 company_master.py
    ```
7. After getting the json files for plotting drop the user and database by running drop script in postgress.
   ```
   \i sql_script/drop-script.sql
   ```

## Output

1. Start the python http server in terminal
   ```
   $ python3 -m http.server
   ```

After getting the server link open it on any browser then click on visualize to visualize the graph.

Options are: 

1. Bar plot of Authorized Capital
2. Bar Plot of Company registered by year
3. Top Registrations By "Principal Business Activity" In 2015
4. Group Bar Plot
5. Exit

## Note

1. If want to run python file don't change the name of downloaded csv file.

2. After visualizing the output of plot press back button there to visualize another plots.

3. Loading csv to database takes 2-3 minutes.

# Demo 
  <b>[live](https://dataproject-javascript.herokuapp.com/)</b>
