---
title: date.nanosecond() function
description: >
  The `date.nanosecond()` function returns the nanosecond of a specified time.
  Results range from `[0-999999999]`.
aliases:
  - /v2.0/reference/flux/functions/date/nanosecond/
menu:
  v2_0_ref:
    name: date.nanosecond
    parent: Date
weight: 301
---

The `date.nanosecond()` function returns the nanosecond of a specified time.
Results range from `[0-999999999]`.

_**Function type:** Transformation_  

```js
import "date"

date.nanosecond(t: 2019-07-17T12:05:21.012934584Z)

// Returns 12934584
```

## Parameters

### t
The time to operate on.

_**Data type:** Time_
