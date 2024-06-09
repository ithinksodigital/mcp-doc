# Select Property

See Enumerated values within
[String](/docs/marketing/personalization/guide/string.html) and
[Number](/docs/marketing/personalization/guide/number.html).

* * *

Static values for complex configurations can be defined such that they appear
as options within a dropdown menu by using the `@options` decorator. If the
complex type contains a `label` property, it is used for the option's label.

![fa7179ad-9667-450a-8e83-79ba4f73bea6]

* * *

Dynamic options can be loaded using the `@lookupOptions` decorator. If the
options value is a string, the value is used as the label.

![65870332-475a-4b60-8a00-5ce46fd74d00]

* * *

If the class has a `label` property, this property is displayed in the
dropdown.

![356bb86e-eeae-4f14-a6dd-19d43f242d33]

* * *

The `Lookup` class can pass data via a constructor to configure what the
lookup method returns as options.

![d0db901c-dfdb-49f0-887b-4779f633d0e6]

* * *

The `@searchOptions` decorator works similarly to `@lookupOptions`. The
difference is that `@searchOptions` provides a search string that can be used
to filter applicable options.

![0f3e6e9d-02f4-4687-ac7c-054618fc5a72]

