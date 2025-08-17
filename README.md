### Data Cleaning and Preprocessing
```python
import pandas as pd

# Load the dataframe.
df_africa = pd.read_csv('datasets/africa.csv')

# Clean column names by removing leading/trailing spaces
df_africa.columns = df_africa.columns.str.strip()

# Drop any duplicate rows
df_africa.drop_duplicates(inplace=True)

# Drop rows with missing values
df_africa.dropna(inplace=True)

# Save the cleaned data to a new CSV file
df_africa.to_csv('datasets/cleaned_africa.csv', index=False)
print("Saved Successfully")
```