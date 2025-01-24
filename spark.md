# Introducing Apache Spark

[Apache Spark] is a

> multi-language engine for executing data engineering, data science, and machine learning on single-node machines or clusters.

Within the Databricks product, Spark is tightly integrated with Python, R, Scala and Java bindings. This allows us to use any of these languages to access Spark features.

And it has many features! Fundamentally, Spark manages Big Data, supervises parallel processing of that data alongside result collation, and makes all kinds of transform and analyis tasks simple.

Spark is perfect for creating our [medallion architecture](https://github.com/bjss-data-academy/data-engineering-fundamentals/blob/main/medallion-architecture.md) data pipelines.

Let's get started by writing some Spark code in a notebook.

## Creating a Spark DataFrame
In a new editor block, type the following Python code:

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

A _DataFrame_ is a Spark object that holds and manages data. They are the central piece of Spark enabling us to analyse and transform large data sets.

Above, we created a DataFrame from inline data, as we would do for unit testing. We created a table of 3 rows, each one describing the favourite item and associated spend of one of our esteemed Academy staff. In Rosie's case, that's just one pair of trainers ...

Anyway.

Note the methods available on the DataFrame object. The first is:

```python
df.printSchema()
```

which displays the _inferred schema_ of the DataFrame. The list of tuples is read in, data types inferred, and the DataFrame object beomces aware of the implicit data schema present in the data.

The next method is:

```python
df.show()
```

which lists the rows in the DataFrame object.

## Working with DataFrames
There are many things we can do with a DataFrame. 

For analysis, DataFrame query and aggregate methods are ideal. Look at this code and its output:

![Querying a DataFrame](/images/dataframe-methods.png)

Similar to an SQL query, this Python code has filtered the data frame by comparing a column value, and stored the result in a new DataFrame object. The original is left intact.

The code goes on to count the number of rows in this new data frame.

## Much, much more with DataFrames!
There are many other methods we can use on DataFrames.

They can read and write different formats of data, including the _parquet_ format used in a Databricks Data Lake. They easily convert to and from popular data formats like csv and json - and can infer schema from these sources.

Under the covers, DataFrame objects can work in parallel to partition large amounts of data, divide the processing up amongst a cluster of compute resources, then pull together the result. All of that is programming we don;t have to do.

We'll leave our tour of Spark there for now. For more, see the Apache Spark Programming course.

# Next
[Back to Contents](/contents.md)
