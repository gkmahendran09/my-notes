## Filter only few Columns

` df['col_name'] `

` df[['col_name1', 'col_name2']] `

## Iterate over rows

```
for index, row in df.iterrows():
    print(row['c1'], row['c2'])
```
