# Capture User and Account Attributes

The `onActionEvent` method captures user and account attributes to add user
data to an event before sending it to Personalization. For more information on
the `user` and `account` objects, see the [user
object](/docs/marketing/personalization/guide/event-options-
salesforceinteractions.html#the-user-object) and the [account
object](/docs/marketing/personalization/guide/event-options-
salesforceinteractions.html#the-account-object) documentation.

The following are examples of using the `onActionEvent` method in the `global`
configuration.

The following are examples of using the `onActionEvent` method in the
`pageTypes` configuration.

In the following code samples, the `onActionEvent` method is used in the
`global` configuration. It listens on every page for a form in the footer to
be submitted. It then sends an event containing the user's ID and captures the
user's email address, which you can then configure for use as an identity. To
know more about using captured data as an ID, see the [Event
API](/docs/marketing/personalization/guide/event-options-
salesforceinteractions.html#the-user-object) documentation.

The following examples depict a listener in the `pageTypes` configuration. You
can see that the event's structure is the same as the structure of the event
sent by the listener in the `global` configuration in the previous namespace-
specific examples.

Capturing `account` attributes works the same way as capturing `user`
attributes. For the full structure of the `account` object, see the [account
object](/docs/marketing/personalization/guide/event-options-
salesforceinteractions.html#the-account-object) documentation.

  * _Salesforce Help_ : [Create a User Profile Object](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_object_create.htm)

