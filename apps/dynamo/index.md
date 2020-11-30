# Dynamo

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

```sql
app = 'buckets'
```

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/scan-results.png"/>

You can check for multiple properties by adding more conditions...

```sql
app = 'buckets' AND tag = 'beta'
```

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/more-scan-conditions.png"/>

If you want help deciding how to formulate your search, click the down arrow
at the end of the input box and an input form will appear. This form will help
you add more conditions, choose how to compare your search value with the values
in the database, discover property names and input the correct value type.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/scan-form.png"/>

### Querying

Tables are rows of related data. All rows of data are just objects with properties.
But when you create your table, you pick one or two special properties that are
known as `partition` or (`hash`) and `range` properties.

Dynamo uses these partition (hash) properties as the `keys` to organize your tables.
A query will give you faster results because it can focus-in on a single partition of
your table and look at only rows that match.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/query-form.png"/>
