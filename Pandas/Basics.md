## Filter only few Columns

` df['col_name'] `

` df[['col_name1', 'col_name2']] `

## Iterate over rows

```
for index, row in df.iterrows():
    print(row['c1'], row['c2'])
```

## Drop Columns by Name

` df.drop(['C', 'D'], axis = 1) `

## Drop Columns by Index

` df.drop(df.columns[[0, 4, 2]], axis = 1, inplace = True)  `