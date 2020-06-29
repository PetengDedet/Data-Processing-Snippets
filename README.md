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
