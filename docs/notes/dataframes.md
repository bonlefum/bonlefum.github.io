# Understanding dataframes

R uses dataframes as one of its primary methods of organising data. 

Pandas provides some similar functionality; also mimics some operations of SQL joins (with merge). Not sure what the efficiency is like, though pd does support single or multiple indices so could be fast.


## Resources

* Producing dataframes from lists, dictionaries - example walkthrough (image at top is succinct) [blog post](http://pbpython.com/pandas-list-dict.html)

* [excerpt from DSH](https://jakevdp.github.io/PythonDataScienceHandbook/03.08-aggregation-and-grouping.html)

## Equivalent operations

| R                                             | Pandas                                    |                       |
|---------------------------------------------- |------------------------------------------ |---------------------- |
| df <- read.table("data.csv")                  | df = pd.read_csv("data.csv")              |                       |
| head(df)                                      | df.head()                                 |                       |
| colnames(df) <- c("time", "cost", "harvest")  | df.columns = ["time", "cost", "harvest"]  | see also df.rename()  |
|                                               |                                           |                       |
|                                               |                                           |                       |
