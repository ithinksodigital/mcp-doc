# Attributes

Attributes are custom-configured, type-safe fields that can store additional
custom data at various levels in the platform. You can configure attributes
for users, accounts, catalog objects, and profile objects.

The following table details the value types supported by Attributes.

Value Type| Description  
---|---  
String| Text information  
Integer| Whole numbers  
Decimal| Floating point numbers  
Date| Date and time, specifically the JavaScript
[`Date`](https://developer.mozilla.org/en-
US/docs/Web/JavaScript/Reference/Global_Objects/Date) object  
Boolean| `true` or `false`  
null| Attribute present but without an object value  
  
Attribute collections are keyed off the attribute name/id, as depicted in the
following example.

Each `Attribute` contains a `value` and optional `metadata` about the value.

A value can be of type `string`, `number`, `boolean`, `null`, `Date`, or a
(potentially nested) collection containing them.

The optional `metadata` can contain detailed information about the value, as
depicted in the following example.

The `publishedDate` attribute must be exclusively used for articles and blogs.
For other use cases, create a new custom attribute.

Attribute TypeScript declarations can almost always contain a `read-only`
modifier. Attribute collections are mutable, which means you can add, replace,
and remove attributes. However, each attribute is immutable after it is
created, ensuring that an attribute value and its optional associated metadata
remain in sync. This immutability also means that you must define a value and
its optional associated metadata together. Currently, you cannot replace or
remove an entire collection of attributes. Instead, you can mutate the
existing collection.

