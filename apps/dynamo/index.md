# Dynamo

## Searching

The input at the top of the app is for searching. There are a few different ways to use it.
Clicking the input label will toggle between `Scan`, `Query` and `PQL` modes.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/input-mode.png"/>

### Modes

Typically, a `scan` iterates over all rows in a database. Scans are simple, but the trade-off is that
they can be slow and expensive on large tables. A `query` allows you to be more specific about what you
are searching for by only looking at rows within a certain range. `PQL` has the highest amount
of specificity, and its cost varies depending on how complicated and intensive your queries are.

The Operator Dynamo App makes the simple cases truly simple.

### Scanning

Consider a table where a row has a property called `app`. The following query will show all
entries where the `app` value is equal to `buckets`. All you need to type is...

```
app = 'buckets'
```

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/dynamo/images/scan-results.png"/>
