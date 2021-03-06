---
title: union() function
description: The `union()` function concatenates two or more input streams into a single output stream.
aliases:
  - /v2.0/reference/flux/functions/transformations/union
  - /v2.0/reference/flux/functions/built-in/transformations/union/
menu:
  v2_0_ref:
    name: union
    parent: built-in-transformations
weight: 401
---

The `union()` function concatenates two or more input streams into a single output stream.
In tables that have identical schemas and group keys, contents of the tables will be concatenated in the output stream.
The output schemas of the `union()` function is the union of all input schemas.

`union()` does not preserve the sort order of the rows within tables.
A sort operation may be added if a specific sort order is needed.

_**Function type:** Transformation_  
_**Output data type:** Object_

```js
union(tables: [table1, table2])
```

## Parameters

### tables
Specifies the streams to union together.
There must be at least two streams.

_**Data type:** Array of streams_

## Examples
```js
bucket1 = from(bucket: "example-bucket-1")
  |> range(start: -5m)
  |> filter(fn: (r) => r._field == "usage_guest" or r._field == "usage_guest_nice")

bucket2 = from(bucket: "example-bucket-2")
  |> range(start: -5m)
  |> filter(fn: (r) => r._field == "usage_guest" or r._field == "usage_idle")

union(tables: [bucket1, bucket2])
```
