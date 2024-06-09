

# Merge Using Shared Identity Type Data

Merge user profiles based on shared identity type data.

You can create a Unified Customer Profile from multiple sources when there’s
clear identity information in those sources, such as a customer ID or an email
address. However, each user doesn’t always have a clear identifier for every
interaction within each channel. Personalization uses specific identifiers,
called identity types, to determine how to process web events, API events, and
channel events to identify users from various sources.

Personalization merges user profiles based on shared identity type data. When
the identity system receives events with populated identity types and
attributes, Personalization determines whether the event is for a new or an
existing user profile. Personalization assigns an event to an existing user
profile when the event meets the following conditions:

  * There’s at least one identity type with a uniqueness of **Identity Namespace**.

  * The identity type matches the value for the same identity type in an existing user profile.

