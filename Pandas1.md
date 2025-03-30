# Pandas in Python: Data Analysis Powerhouse

Pandas is a powerful and versatile Python library for data manipulation and analysis. It provides data structures like DataFrames and Series, which make it easy to work with structured data.

## Part 1: Core Data Structures and Basic Operations

**1. Series:**

* A Series is a one-dimensional labeled array capable of holding any data type (integers, strings, floats, Python objects, etc.).
* It's like a column in a spreadsheet or a SQL table.
* **Creating a Series:**

    ```python
    import pandas as pd

    s = pd.Series([10, 20, 30, 40, 50])
    print(s)
    ```

* **Custom Index:**

    ```python
    s = pd.Series([10, 20, 30, 40, 50], index=['a', 'b', 'c', 'd', 'e'])
    print(s)
    ```

* **Accessing Elements:**

    ```python
    print(s['b'])  # Access by label
    print(s[1])     # Access by position
    ```

* **Slicing:**

    ```python
    print(s['b':'d']) #Slicing by label.
    print(s[1:3]) #Slicing by position.
    ```

**2. DataFrame:**

* A DataFrame is a two-dimensional labeled data structure with columns of potentially different types.
* It's like a spreadsheet or a SQL table.
* **Creating a DataFrame:**

    ```python
    data = {'Name': ['Alice', 'Bob', 'Charlie', 'David'],
            'Age': [25, 30, 22, 35],
            'City': ['New York', 'London', 'Tokyo', 'Paris']}
    df = pd.DataFrame(data)
    print(df)
    ```

* **Accessing Columns:**

    ```python
    print(df['Name'])  # Access a single column (Series)
    print(df[['Name', 'Age']]) #Access Multiple columns (DataFrame)
    ```

* **Accessing Rows:**

    ```python
    print(df.loc[0])    # Access row by label (index)
    print(df.iloc[0])   # Access row by position
    ```

* **Slicing Rows and Columns:**

    ```python
    print(df.loc[1:2, ['Name', 'City']]) #Slicing by label.
    print(df.iloc[1:3, 0:2]) #Slicing by position.
    ```

**3. Basic Operations:**

* **Reading Data:**

    ```python
    df = pd.read_csv('data.csv')  # Read from CSV
    df = pd.read_excel('data.xlsx') #Read from excel
    ```

* **Writing Data:**

    ```python
    df.to_csv('output.csv', index=False)
    df.to_excel('output.xlsx', index = False)
    ```

* **Descriptive Statistics:**

    ```python
    print(df.describe())  # Summary statistics of numerical columns
    print(df['Age'].mean()) #Mean of the age column.
    print(df['Age'].max()) #Max value of the age column.
    ```

* **Sorting:**

    ```python
    df_sorted = df.sort_values(by='Age')
    print(df_sorted)
    ```

* **Filtering:**

    ```python
    filtered_df = df[df['Age'] > 25]
    print(filtered_df)
    ```
