# Programming-Assignment-3

ReadMe File 
Munsayac, Angela Ysabhelle C
2ECE-B

Programming Assignment 3 
Python Data Analysis (Pandas)

I am tasked to do and use pandas to perform and use different types of dataframes, importing an excel file to use for the activity.  In problem 1:

PROBLEM 1: Save your file as Surname_Pandas-P1.py
Using knowledge obtained from the experiment and demonstrations:
a. Load the corresponding .csv file into a data frame named cars using pandas
b. Display the first five and last five rows of the resulting cars.

1.	Firstly, I downloaded the car.csv file that I will be using for this problem, and put it in the same folder as my python file so that I can load it earlier. 
2.	import pandas as pd – This function serves as library  and gives it the short alias pd. pandas provides the DataFrame structure and functions like read_csv, head, and tail that I will be using in the program.
3.	cars = pd.read_csv("cars.csv") – Loading the csv file into a dataframe named cars. So I can continue making the program. 
4.	cars.head()
print("First five rows of cars:") – returns and print the first five rows of the csv car file and display it as a table.
5.	cars.tail()
print("Last five rows of cars:")
– prints the first question in the program. And for the second code, it will return the last five rows of the csv file. 
So, in this question knowing and understanding how to load a csv into a data frame is important, it helps us to make our job easier by knowing this dataframe. 

PROBLEM 2: Save your file as Surname_Pandas-P2.py
Using the dataframe cars in problem 1, extract the following information using subsetting, slicing and
indexing operations.

I started by downloading the cars.csv file and saving it in the same directory as my Python script. Keeping both files together makes it easier to access the dataset directly without needing a long file path.

1.	 Import the pandas library- import pandas as pd -This line loads the pandas library and assigns it the short alias pd. The pandas package is widely used for data analysis because it introduces the DataFrame structure and provides helpful functions such as read_csv(), head(), and tail().

2.	Load the CSV into a DataFrame - cars = pd.read_csv("cars.csv") - The CSV file is read into a DataFrame object named cars. A DataFrame is similar to a table in Excel—it contains rows (individual cars) and columns (attributes like model, cylinders, horsepower, gears, etc.).
For the problems that I will do:

a.	Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7...) of cars.
 	cars.iloc[:5, ::2]
In this code, I am going to display the first row with odd numbered columns which is the first five rows (:5) and each of the second columns (::2), or columns 1, 3, 5, 7, and so forth, are chosen by the expression iloc[:5, ::2] and it will print the given code above. This displays the dataset with only the odd-numbered columns for the first five rows displayed.

b.	Display the row that contains the ‘Model’ of ‘Mazda RX4’.
cars.loc[cars['Model'] == 'Mazda RX4'].iloc[0]
This part of the code, it prints the car model of Mazda RX4 and it will display the details fot the Mazda RX3 Model, 

c.	How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?
cars.loc[[23],['Model', 'cyl']]
 In this code, I am trying to locate the number of cylinder of Camaro Z28. The .loc function selects specific rows and columns in the DataFrame. Here, index 23 points to the "Camaro Z28" row, and ['Model', 'cyl'] displays only its model and cylinder count, showing that the Camaro Z28 has 8 cylinders.

d.	Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda  RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.’
cars.loc[[1, 28, 18], ["Model", "cyl", "gear"] 
I use the .loc function to get specific rows and columns. In rows 1, 28, and 18     correspond  to  Mazda RX4 Wag, Ford Pantera L, and Honda Civic, while ["Model", "cyl", "gear"] shows only their model, cylinder count, and gear type.

This shows that the use of .loc to quickly filter and display only the needed information.

