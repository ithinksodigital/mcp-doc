

# B2B Detect

B2B Detect lets you access firmographic data about your users, such as their
industry, beginning with their first interaction. The addition of firmographic
data allows Marketing Cloud Personalization to provide more targeted
personalization to your accounts and their users.

## Firmographic Information Based on IP Address

At the time of a user's first page view or app event, Personalization provides
firmographic information about that user based on their IP address. The
initial firmographic information automatically updates as Personalization
learns a user’s email address, account domain, or account ID, so you always
have the most up-to-date firmographic data.

## Account Origin

The account origin determines the account where a user belongs. The more
explicit the account origin, the more confidence Personalization has in it.

Personalization uses the origin that provides the highest level of confidence
until another origin becomes available that instills equal or higher
confidence. The four account origins, in increasing order of confidence, are:

**Account origin** |  **Example** |  **Likely sources** |  **Derivation of organization**  
---|---|---|---  
IP address | 25.25.25.1 | First event from site or mobile visit | IP address > location/organization > match in firmographic database  
Email address | user@salesforce.com | Form submission, user login | Domain > match in firmographic database  
Account domain | salesforce.com | Third-party sync, user login, user upsert | Domain > match in firmographic database  
Account ID* | evg:343536nto | UpsertThird-party sync, user login, user upsert | ExactExact  
  
*An “evg:” prefix indicates an account with associated firmographic data. A nonprefixed account ID doesn’t have firmographic data.

## Account Detection

The user’s account assignment can change if one of the origins updates and is
of the same or higher confidence level than the existing account origin.
Therefore, the account assignment can only improve. For example, if Teresa Lee
provides her email address, teresa.lee@acme.com, Personalization assigns her
to the Acme account. Personalization doesn’t use Theresa's IP address as an
origin, even if it changes, because an IP address has a lower confidence level
than an email address.

## Account Assignment Process

When you have B2B Detect enabled in Personalization, the following occurs
automatically whenever there’s an update to the account origin:

  * Personalization looks up an organization based on the account origin:

Origin | Description  
---|---  
**IP address** | Personalization looks up the corresponding location and organization.  
**Email address or account domain** | Personalization uses the domain to look up the organization.  
**Account ID** | Personalization looks up the organization with that same ID as the account.  
  * If Personalization finds an organization, it looks up or creates a corresponding account.

  * Personalization adds or updates the firmographic data about the organization for the account record. The firmographic data is read-only and is visible along with any other account attributes that are in Personalization.

  * Personalization adds the user to the account.

## Firmographic Data

Firmographic data gives you a more in-depth profile of each account, so you
can segment on any of the following properties:

  * Name

  * NAICS code/Industry name

  * Revenue

  * Employee count

  * Category—The category consists of a list of keywords that Personalization extracts from the company description. In fast-moving sectors, such as technology, the category can be more useful than a standard NAICS code.

Updates to the firmographic organizational data come from Personalization’s
service providers on a monthly basis.

#### See Also

  * [Create a Segment Based on B2B Detect Data](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_create_b2b_detect.htm&language=en_US&type=5 "Create segments for your campaigns that target users according to IP data sources and NAICS industry codes. This feature is available only with B2B Detect. Using B2B Detect, you can create personalized calls-to-action, case studies, and banner images based on a user’s industry or company name. You use three location rules to create the segment for B2B Detect data.")

