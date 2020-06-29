* Pandas Move Column Position
```python
# Make a copy of column
column_copy = df['column_name']
# Drop column
df.drop(labels='column_name', axis=1, inplace=True)
# Insert copied column into new position index
df.insert(1, 'column_name', column_copy)
```