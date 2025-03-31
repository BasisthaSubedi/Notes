## Part 2: Advanced Operations and Data Manipulation

**4. Handling Missing Data:**

* **Checking for Missing Values:**

    ```python
    print(df.isnull().sum()) #Number of missing values per column.
    ```

* **Dropping Missing Values:**

    ```python
    df_cleaned = df.dropna()  # Drop rows with any missing values
    df_cleaned_col = df.dropna(axis=1) #Drop columns with missing values.
    ```

* **Filling Missing Values:**

    ```python
    df_filled = df.fillna(0)  # Fill with a specific value
    df_filled_mean = df.fillna(df.mean()) #Fill with the mean of each column.
    ```

**5. Data Transformation:**

* **Adding New Columns:**

    ```python
    df['Age_Squared'] = df['Age'] ** 2
    ```

* **Applying Functions:**

    ```python
    def categorize_age(age):
        if age < 25:
            return 'Young'
        elif age < 35:
            return 'Adult'
        else:
            return 'Senior'

    df['Age_Category'] = df['Age'].apply(categorize_age)
    ```

* **Grouping and Aggregation:**

    ```python
    grouped = df.groupby('City')['Age'].mean()
    print(grouped)
    ```

* **Pivot Tables:**

    ```python
    pivot_table = pd.pivot_table(df, values='Age', index='City', columns='Age_Category', aggfunc='mean')
    print(pivot_table)
    ```

* **Merging and Joining:**

    ```python
    df1 = pd.DataFrame({'ID': [1, 2, 3], 'Value1': ['A', 'B', 'C']})
    df2 = pd.DataFrame({'ID': [2, 3, 4], 'Value2': ['X', 'Y', 'Z']})

    merged_df = pd.merge(df1, df2, on='ID', how='inner')  # Inner join
    print(merged_df)
    ```

* **Concatenation:**

    ```python
    combined_df = pd.concat([df1, df2])
    print(combined_df)
    ```

**6. Time Series (If Applicable):**

* **Converting to Datetime:**

    ```python
    df['Date'] = pd.to_datetime(df['Date'])
    ```

* **Setting Index:**

    ```python
    df = df.set_index('Date')
    ```

* **Resampling:**

    ```python
    daily_mean = df.resample('D').mean()  # Resample to daily frequency
    print(daily_mean)
    ```

Pandas is an essential tool for any data scientist or analyst working with Python. Its intuitive data structures and powerful functions make it easy to clean, transform, and analyze data.