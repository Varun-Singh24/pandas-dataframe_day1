
**Pandas_as_dataframe **
import pandas as pd
import numpy as np

# --- Creating a DataFrame with NaN ---
df2 = pd.DataFrame(
    {
        "Name": [
            "Varun, Mr harris",
            "Allen",
            np.nan
        ],
        "Age" : [22, 35, 58],
        "Sex" : ["male", "male", "male"]
    }
)
# df2

# --- Creating the main DataFrame ---
df = pd.DataFrame(
    {
        "Name": [
            "Varun, Mr harris",
            "Allen",
            "Bob John"
        ],
        "Age" : [22, 35, 58],
        "Sex" : ["male", "male", "male"]
    }
)

# We can get the Dtypes of the columns of the df
# df.dtypes

# Accessing a column gives a pandas Series
age_series = df['Age']
# type(age_series) returns <class 'pandas.core.series.Series'>

# Alternative access for a column
# df.Name

# Explicitly creating a Series
ages = pd.Series([22, 35, 58], name="Age")
# ages

# Unnamed Series
ages1 = pd.Series([22, 35, 58] )
# ages1


# --- How to Read and Write Tabular Data ---

# Supported Formats:
# CSV, XLSX, JSON, PARQUET, AVRO, SQL, XML, HDF5, GBQ, TSV

# We can read tabular data using pandas' read_ methods:
# pd.read_csv, pd.read_excel, pd.read_json, etc.

# Example: Read a CSV (assuming 'titanic.csv' is available)
# titanic = pd.read_csv("/content/titanic.csv") 

# Example: Save DataFrame to Excel
# titanic.to_excel("titanic.xlsx", sheet_name="passengers", index=False)

# Inspecting the Data:
# titanic.head()      # View first 5 rows (default)
# titanic.head(20)    # View first 20 rows
# titanic.tail(20)    # View last 20 rows

# Getting data types
# titanic.dtypes      # Returns a Series
# titanic.dtypes.reset_index() # Converts dtypes Series to a DataFrame
