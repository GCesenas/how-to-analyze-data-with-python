Análisis de datos banco.csv

# Analysis of CSV Bank data 💻

Data analysis for the CSV file called **'bank'** which is a series of bank customer data, with more than 10,000 records.

## First steps 🚀

_These instructions will allow you to obtain detailed information from the CSV file 'bank', where in the part below I will provide you with the necessary commands so that you can do it quickly and easily. 🙂_

See **Deployment** for how to run the resulting .py file.

### Pre-requirements 📋

_What things do you need to install the software and how to install them:_ 
**\- Python programming language (in this case)**  
**\- Python virtual environment**  
**\- Pandas library for managing datasets**

You can install the latest version of **Python** from its official website:
[Click here to download Python.](https://www.python.org/downloads/)

Once you have **Python** installed, you can check that it is properly installed and check its version simply by typing **'python'** in your preferred command prompt:

```
# Type 'python'
PS C:\Users\user> python

# If everything is in order, it will return the following code (depending on the version you have)
Python 3.9.1 (tags/v3.9.1:1e5d33e, Dec  7 2020, 17:08:21) [MSC v.1927 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.

```

-   **In macOS:** Go to Applications > Utilities > Terminal and type **‘python.’** If you downloaded Python 3, type **‘python3’**.
-   **In Linux:** Open your terminal and type**‘python’** or **‘python3’** depending on the version you have installed.

Una vez que tienes **Python** instalado, para crear el entorno virtual donde se hará la auditoría de los datos, se tiene que instalar el paquete **‘virtualenv’**:

> For all operating systems:

```
pip install virtualenv

```

To create the virtual environment, you will need to specify the directory. For example, to create it in the location where the console is currently and create the virtual environment with the name **'venv'** type the following:

```
virtualenv venv

```

Once the virtual environment called **'venv'** has been created, it's time to activate it with the following command:

> MacOS and Linux

```
source venv/bin/activate

```

> Windows

```
venv\scripts\activate

```

Before being ready, it remains to install the **pandas** library to do the data analysis:

```
pip install pandas

```

Very well! At this point, we are ready to start performing the data analysis.✅

## How will we do the analysis? 🥷

### Following steps 👩‍💻👨‍💻

- Import **pandas** library
- Read the **csv file** with which we are going to do the analysis
- Know the **dimensions** of the dataset
- Know the **missing data** per column
- Know the **null values**
- Know the **types of data** that the dataset has (in general)
- Know the **data types** that the dataset has (by column)
- Make use of the **info() function**
- Make use of the **function describe()**
- Know the **duplicate data** in sum

### Import pandas library

Importing the pandas library is very simple, we will do it with the following line of code:

```
import pandas as pd

```

### Read the CSV file with which we are going to do the analysis

To read the CSV file in question, the variable **'df'** will be declared to refer to the dataframe later:

```
# Read the csv that we will use, in this case, 'banco.csv'
df  =  pd.read_csv('datasets/banco.csv')

```

### Know the dimensions of the dataset

The **shape** method of the dataframe will be printed in the console to know its dimensions:

```
print(df.shape)

```

### Know the missing data by column

To know the **missing data** for each of the columns of the csv file, we will create a foreach loop and print each result in the console:

```
col_names = df.columns.tolist()
for column in col_names:
    print("Valores nulos en <" + column + ">: " + str(df[column].isnull().sum()))

```

### Know null values

To know the **null values** there are, the isnull() function is used and it is printed on the console:

```
print(df.isnull())

```

### Know the types of data that the dataset has (in general)

The **dtypes** method is used to the dataframe to know the data types in general:

```
print(df.dtypes)

```

### Know the types of data that the dataset has (by column)

A foreach loop is created to specify what data type each column has:

```
for column in col_names:
    print("The column <" + column + ">: has the data type: " + column.dtypes())

```

### Know the types of data that the dataset has (by column)

A foreach loop is created to specify what data type each column has:

```
for column in col_names:
    print("La columna <" + column + ">: Has the datatype: " + column.dtypes())

```

### Make use of the info() function

Calling the **info()** function is very simple, you just have to print and call it with the previously created dataframe variable:

```
print(df.info())

```

### Make use of the describe() function

Calling the function **describe()** is very simple, you just have to print and call it with the previously created dataframe variable:

```
print(df.describe())

```

### Know the duplicate data in sum

Viewing duplicate data in sum involves calling two functions simultaneously, first the **duplicated()** function to get the duplicates, and then the **sum()** function to add the results:

```
print(df.duplicated().sum())

```

## Deployment 📦

To test each of the points together or one by one, just use the **python** command, and then the name of the file that we have created to carry out the previous steps:

```
(venv) PS C:\Directory> python file.py

```

## Built with 🛠️

_The tools needed to build this project are as follows:_

-   [Python](https://www.python.org/) \- Used programming language
-   [Pandas](https://pandas.pydata.org/) \- Data analysis library

## Author ✒️

-   **Gerardo Ceseñas Rivera** \- _Data Analytics Developer_

## License 📄

This project is freely licensed, in case of replicating it, credits would be appreciated. 😄

## Expressions of Gratitude 🎁

-   I thank anyone who is reading this, for reaching the end, I hope it has been useful. Shall we parse another CSV?

----------

⌨️ with ❤️ by Gerardo Ceseñas Rivera 😊
