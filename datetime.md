# DateTime Property

A date picker input.

![bcdcb5a2-4d28-4bff-8658-21a0734c2848]

The value returned from the selection is structured as an object with a single
`dateTime` property. The property is an array of strings representing the date
and time in ISO 8601 format (for example, 2019-10-08T16:00:00.000Z).

The object structure is as follows:

Even if the `DateTime` picker only intends to return a single date, it still
returns an array.

* * *

The picker can be configured to return a range using the `@range` decorator.

In this case, the returned array value has the start of the range in the 0
index of the array, and the end of the range in the 1 index.

