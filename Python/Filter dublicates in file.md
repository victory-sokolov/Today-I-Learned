# Filter dublicates in the file

Reading csv file and filter dublicates then write filtered data to new file

```python
with open('temp.csv','r', encoding="utf-8") as in_file,
    open('ShopeeData.csv','a', encoding="utf-8") as out_file:
    data = set()
    for line in in_file:
        if line in data: continue

        data.add(line)
        out_file.write(line)
```
