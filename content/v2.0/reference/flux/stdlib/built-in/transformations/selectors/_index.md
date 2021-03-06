---
title: Flux built-in selector functions
list_title: Built-in selector functions
description: Flux's built-in selector functions return one or more records based on function logic.
aliases:
  - /v2.0/reference/flux/functions/transformations/selectors
  - /v2.0/reference/flux/functions/built-in/transformations/selectors/
menu:
  v2_0_ref:
    parent: built-in-transformations
    name: Selectors
    identifier: built-in-selectors
weight: 401
v2.0/tags: [selectors, built-in, functions]
---

Flux's built-in selector functions return one or more records based on function logic.
The output table is different than the input table, but individual row values are not.

The following selector functions are available:

{{< children type="functions" >}}


### Selectors and aggregates
The following functions can be used as both selectors or aggregates, but they are
categorized as aggregate functions in this documentation:

- [median](/v2.0/reference/flux/stdlib/built-in/transformations/aggregates/median)
- [quantile](/v2.0/reference/flux/stdlib/built-in/transformations/aggregates/quantile)
