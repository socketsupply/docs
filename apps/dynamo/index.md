# Dynamo

The _Dynamo_ app is a GUI for the DymanoDB database.

## Searching

The input at the top of the app is for searching. There are three different
ways to use it. Clicking the input's label will toggle between `Scan`, `Query`
and `PQL` modes.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/input-mode.png"/>


### The difference between modes

A `scan` iterates over all rows in a database. Scans are simple, but the
trade-off is that the larger the table gets, the slower the scan will be.
A `query` allows you to be more specific about what you are searching for
by only looking at rows within a certain range. `PQL` has the highest amount
of specificity, and its cost varies depending on how complicated and intensive
your queries are.


### Scanning

Consider a table where a row has a property called `app`. The following query
will show all entries where the `app` value is equal to `buckets`. All you need
to type is...

```
app = 'buckets'
```

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/scan-results.png"/>

You can check for multiple properties by adding more conditions...

```
app = 'buckets' AND tag = 'beta'
```

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/more-scan-conditions.png"/>

If you want help deciding how to formulate your search, click the up/down arrow
inside the input box (right side) and a form will appear. This form will help
you add more conditions. From here you can choose how to compare the value you
are searching for with the values in the database. This form will also help you
discover property names and input the correct value type for your search.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/scan-form.png"/>

### Querying

Tables are rows of related data. All rows of data are just objects with properties.
But when you create your table, you pick one or two special properties that are
known as the `partition` and `range` properties.

Dynamo uses the `partition` and `range` properties as the `keys` to organize your
tables. A query will give you faster results because it can focus-in on a single
partition of your table and look at only rows that match.

> Note: DynamoDB requires your `partition` property when for queries (your `range`
> is optional).

```
hash = 'release' AND begins_with(range, 'alpha')
```

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/query-form.png"/>

In this example, we used a `function`. You can see a complete list of functions and
operators [here][0].

### SQL-compatible queries

DynamoDB data can be relational. And sometimes you want to query it that way.
[PartiQL][1] is a SQL-compatible language that allows you to query dynamodb in the
same way you would query a regular relational database.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/pql-form.png"/>

## Query Inspector

A search will generate JSON that cab be used as the parameters to the with the
DynamoDB [aws-sdk][2]. You can inspect, edit and copy this value with the Query
inspector. This can be useful if you are trying to test and develop a query for
your app.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/inspector.png"/>


## Editing

When you select a row, it will open the value editor. Since DynamoDB rows are just objects,
a tree is a good way to progressively disclose the value. From here you can change the type of
a property, edit, delete and add new properties.

> Note: the `partition` and `range` properties are only editable on new records.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/value-editor.png"/>

If you want to edit the DynamoDB value directly, click the code icon at the bottom of the panel.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/value-editor-code.png"/>

[0]:https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Expressions.OperatorsAndFunctions.html
[1]:https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/ql-reference.html
[2]:https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GettingStarted.html
