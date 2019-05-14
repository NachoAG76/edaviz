# Before you read the docs

We implemented edaviz in a way so that it is as user-friendly as possible. The best way to learn the api is to call `eda.overview(df)` and click through the tabs. For each module, we display the code that produced the output. Simply copy-paste the code into another Jupyter cell if you want to play around with the functions.

## edaviz.overview(df, target=None)

Shows an overview widget of a given dataframe. This is the main entry point of the edaviz library. If you specify a target, the overview will be re-arranged.

#### Example

```python
import edaviz as eda
df = eda.get_titanic_df()
eda.overview(df)                       # for general overview
eda.overview(df, target="Survived")    # for overview with focus on a target
```

## edavz.plot(df, x, y)

Plots two columns against each other. The plot will adjust to the data types of the columns specified with `x` and `y`.

#### Example

```python
import edaviz as eda
df = eda.get_titanic_df()
eda.plot(df, "Age", "Survived")
```

## eda.patterns(df)

Shows an interactive heatmap comparing all columns with each other. It is like a correlation matrix, but uses a predictive power score instead.
