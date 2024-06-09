

# About Personalization API Tokens

Learn more about API tokens in Marketing Cloud Personalization.

## Data Access Levels

Personalization's REST API provides access to read and update data at several
levels:

  * Create and update users and accounts within Personalization

  * Receive behavioral data from offline systems

  * Receive historical transaction data

  * Create and update catalog data, including products and content

## Using an API Token in an API Request

When making an API request, you must set the HTTP authorization header using
Basic encoding:

  * Most REST clients provide the option to set Basic credentials using a username and password. In this situation, supply the API Key ID as the username, and the API Secret Key as the password.

  * If you must construct the HTTP authorization header value manually, use Basic encoding as follows: 

Basic <encoded-credential> where <encoded-credential> is a strict Base64
encoding of: <api-key-id>:<api-secret-key>

