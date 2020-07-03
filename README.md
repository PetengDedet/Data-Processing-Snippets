* Pandas Move Column Position
```python
"""
1. Make a copy of column
2. Drop column
3. Insert copied column into new position index
"""

column_copy = df['column_name']
df.drop(labels='column_name', axis=1, inplace=True)
df.insert(1, 'column_name', column_copy)
```
---

* Pandas Read CSV
```python
pd.read_csv("file.csv", sep=";")
```
---

* Pandas Save to CSV
```python
df.to_csv("file.csv", sep=";", index=False, header=True)
```
---

* Pandas Run SQL Query
```python
import pandas as pd
from sqlalchemy import create_engine

engine = create_engine("postgres://username:password@host:port/db_name")

df = pd.read_sql_query("SELECT * FROM table_name", con=engine)
```
---

* Pandas Insert to SQL
```python
df.to_sql("table_name", con=engine, if_exists="append", index=False)
```
---

* Pandas Copy or Duplicate Dataframe

Make a copy of dataframe to keep original one untouched
```python
df2 = df.copy()
```
---

* Pandas get unique values of a acolumns
```python
df['column_name'].unique()
```
---

* Pandas Change or Modify string column case
```python
df['column_name'] = df['column_name'].str.upper()
df['column_name'] = df['column_name'].str.lower()
```
---

* Pandas Where IN query

Get dataframe that has column match to a list
```python
df[df['column_name'].isin(['a', 'b', 'c'])]
```
---

* Pandas delete row by condition
```python
df = df.drop(df[df['column_name'] == ''].index)
```
---

* Pandas Update row by condition
```python
old_value = 'old_val'
new_value = 'new_val'

df.loc[df['column_name'] == old_value, 'column_name'] = new_value
```
---

* Pandas sort value by

Pandas order by multiple column
```python
df = df.sort_values(by=['column_1', 'column_2'], ascending=True)
```
---

* Pandas group by dataframe without index
```python
df2 = df.groupby(["column_1", "column_2"]).size().reset_index(name='count')
df2.drop(columns=['count'], axis=1, inplace=True)
```
---

* Pandas Lookup other table

Lookup value or left join to another dataframe
```python

new_df = pd.merge(left_df, right_df,  how='left', left_on=['left_col'], right_on=['right_col'])
```
---

* Pandas where column is null
```python
df[df['column_name'].isnull()]
```
---

* Pandas change column data type
```python
df['column_name'] = df['column_name'].astype(int)
```
---
