# Apache Spark Programming

xxx

## xxx

```python
df = spark.createDataFrame(
    [
        ("Alan", "curry", 221.15),
        ("Dan", "golf balls", 978.16),
        ("Rosie", "fancy trainers", 199.95)
    ],
    ["name", "item", "spend"]  
)

df.printSchema()
df.show()
```

Click run. After a short time, we will see the results displayed:

![Spark DataFrame print schema and show results](/images/dataframe-schema-show.png)
