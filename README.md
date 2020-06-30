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

* Pandas Read CSV
```python
pd.read_csv("file.csv", sep=";")
```

* Pandas Save to CSV
```python
df.to_csv("file.csv", sep=";", index=False, header=True)
```

* Pandas Run SQL Query
```python
import pandas as pd
from sqlalchemy import create_engine

engine = create_engine("postgres://username:password@host:port/db_name")

df = pd.read_sql_query("SELECT * FROM table_name", con=engine)
```

* Pandas Insert to SQL
```python
df.to_sql("table_name", con=engine, if_exists="append", index=False)
```
