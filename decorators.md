# Decorators

The label for the input, to be used instead of the default title case
conversion of the property name.

![422bff87-4cc1-4454-a738-c9b5cb80290f]

* * *

A subtitle for the input.

![e51e64cb-42b6-412c-b0ce-a881c3b6e944]

* * *

For information on the `@units` decorator, see [Number
Property](/docs/marketing/personalization/guide/number.html).

* * *

Adds a header before the decorated property, indicating all properties below
this decorator (until the next header) are intended to be a section on
configurables.

![0b3897d2-5610-4eb6-b183-6138473286ba]

In the preceding example, `simpleProperty2` and `simpleProperty3` fall under
the header "Section Header".

* * *

Additional text to describe a section, can be used to provide the end user
with instructions.

![44ae107d-05f9-4618-98fa-e48d68e1cdb4]

Basic Markdown rendered before the decorated property. Syntaxes are limited to
the following examples.

![c626123b-f5eb-4d14-9ce5-62d118151f9f]

* * *

The `@optional` decorator enables you to flag properties as either optional or
required.

Personalization doesn’t prevent you from saving a campaign with empty or
incomplete template properties that are flagged as required. For example, even
if a `simpleText: string` property is tagged as required by using the
`@optional(false)` decorator, a campaign developer can still save a campaign
with the `simpleText` property field left empty or incomplete.

* * *

Hides the input from the user.

This decorator can also accept a function in order to hide configurables
conditionally. The arguments for the decorator are `this`, and a function
whose first argument is `self`, the instance of this class.

The function MUST return a boolean `true` or `false`. Returning a non-boolean
`truthy` or `falsy` value (for example, 0, 1, 'some string') throws an error.

* * *

The inverse of the `@hidden` decorator, displays the field if true, hides the
field if false.

* * *

For information on the `@richText` decorator, see [String
Property](/docs/marketing/personalization/guide/string.html).

* * *

For information on the `@options` decorator, see [Select
Property](/docs/marketing/personalization/guide/select.html).

* * *

Renders a static list of options as a button group.

* * *

For information on the `@range` decorator, see [DateTime
Property](/docs/marketing/personalization/guide/datetime.html).

* * *

Displays the fields of a complex object horizontally.

Arrays of complex objects are rendered like a table. Include `headersPerRow:
true` to show field titles on each row. Optionally render a line to visually
divide each row by including `dividerLine: true`.

