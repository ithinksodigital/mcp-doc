

# Plan Data Sharing Between Personalization and Salesforce CRM

Before initializing data sharing, decide what data you want to exchange
between Salesforce CRM and Personalization and how you want to match data for
merging. After initialization, Marketing Cloud Personalization shares data
with Salesforce CRM on a nightly basis. Contacts and accounts are shared
automatically, but leads sharing is optional.

## Determine Match Field for Merging

Determine whether you have a unique identifier for each account and user in
Personalization that you can use to match Personalization data with Salesforce
CRM data. Typically, this data is an email address for the user and an account
number or key for accounts. The data must exist in both Salesforce CRM and
Personalization.

## Match and Merge User Data

If you pass the user email address to Personalization, the user syncs to the
Salesforce CRM contact with that email address. Match fields are case-
sensitive, so User.Email@company.com doesn't match user.email@company.com.

## Match and Merge Account Data

If you pass the Personalization account (company) name, and there’s a text
match, the account syncs. If there isn't a text match between the
Personalization account (company) name and the Account name in Salesforce CRM,
you must pass a unique identifier as a custom field to Personalization. For
example, the unique identifier can be a portalID or accountID. The unique
identifier must also be on the account object in Salesforce CRM.

Often, the account name in Personalization doesn’t exactly match the account
name in Salesforce CRM. For example, your contact John Doe is listed under the
account name of “Acme” in Personalization, but the John Doe contact in
Salesforce CRM is associated with the account name Acme Fireworks. The
following option in Personalization pulls account IDs from Salesforce CRM
instead of Personalization to match users who have the same contact name in
Personalization and Salesforce CRM.

  * In Personalization, select **Third Party > Integrations > Salesforce CRM**, scroll to **Advanced Options** , and select **For Salesforce accounts that can’t otherwise be matched to Marketing Cloud Personalization, obtain account IDs from matched Salesforce contacts**.

## Match and Merge Lead Data

In addition to contacts and accounts, you can share leads between
Personalization and Salesforce CRM. Review the following considerations before
deciding whether to match and merge leads:

  * A corresponding Personalization user isn’t created when a new Salesforce CRM contact or lead is created.

  * A corresponding Salesforce CRM contact or lead isn’t created when a new Personalization user or account is created.

  * Only matched users are synchronized.

  * Match fields are case-sensitive.

  * Salesforce CRM contacts take precedence over leads. If there’s a match on both the lead and contact, Personalization syncs only the contact.

  * There’s a separate lead attribute. If a lead converts to a contact, then data synchronizes with the contact record.

## How Matching Works According to Match Priority Order

Before a match occurs, Personalization checks the value of a specific
Salesforce CRM field for the Salesforce user against the value of any
configured Personalization match fields. If any of the match fields are
identical, the Salesforce CRM user is matched to the corresponding
Personalization user.

Contact matches occur on the following Salesforce CRM fields from highest to
lowest priority:

Priority Order | Field to Match by  
---|---  
1 | Salesforce ID  
2 | Any other configured Salesforce match fields  
3 | Salesforce Name or Salesforce Email. In Personalization, select **Only use designated match fields for matching users and accounts, if match fields are specified** in **Advanced Options** under the **Setup** tab for Salesforce CRM.  
  
![126a1263-fefc-4559-b78d-e635615af20c]

Note When you add more than one field for matching, the match condition
follows “OR” logic.

Lead and Account matching follow the same protocol as Contact matching,
except:

  * Lead matching is disabled by default. Contact matches take priority. 
  * Account matching doesn’t use the Salesforce email.

