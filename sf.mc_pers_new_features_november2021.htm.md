

# November 2021 Features in Interaction Studio

The following functionality was released in November, 2021.

## Update Your Launcher Extension by 12/31/2021

The Salesforce Interactions SDK Launcher replaces the Evergage Launcher and is
now available in the [Salesforce Chrome
Store](https://chrome.google.com/webstore/detail/salesforce-
interactions-s/mhmpepeohaddbhkhecaldflljggicedf?hl=en#:~:text=Salesforce%20Interactions%20SDK%20Launcher&text=Provides%20support%20for%20launching%20either,Visual%20Editor%20on%20any%20domain).
With the new SDK Launcher, your Customer Data Platform users now have access
to a sitemap editor. There's no change to functionality for your Interaction
Studio users.

When: The Evergage Launcher extension expires on December 31, 2021.

Where: This change applies to the Interaction Studio Campaigns and Templates
system. With Interaction Studio Classic, use the existing Evergage Visual
Editor Chrome extension.

How: Remove the Evergage Launcher extension from chrome://extensions/. Then
add the SDK Launcher from the [Salesforce Chrome
Store](https://chrome.google.com/webstore/detail/salesforce-
interactions-s/mhmpepeohaddbhkhecaldflljggicedf?hl=en#:~:text=Salesforce%20Interactions%20SDK%20Launcher&text=Provides%20support%20for%20launching%20either,Visual%20Editor%20on%20any%20domain).

## Time Your Campaign Launch with Campaign Scheduler

Use the Campaign Scheduler to select the dates and times that your web and
server-side campaigns show to qualified visitors. Campaign Scheduler rules are
similar to campaign qualification rules. You can schedule campaigns to run
between dates, on days of the week, and hours of the day.

Where: This change applies to the Interaction Studio Campaigns and Templates
system.

How: From a web or server-side campaign, in **Campaign Targeting** | **>**Add Rule****. Select **Date Range** or **Time of Day** and the configuration options that fit your campaign.

## Permit Connections to Your Data Warehouse with an IP Allowlist

Use the Data Warehouse IP Allowlist to improve system security and help
prevent unauthorized access to your Interaction Studio Data Warehouse. After
an administrator adds an IP range, Interaction Studio permits connections only
from the IP ranges on the allowlist. If your allowlist is empty, Interaction
Studio doesn’t accept connections from any IP address.

Who: To add IP addresses to the Data Warehouse IP Allowlist, you need
administrator permissions for Interaction Studio.

How: From the main navigation, select **Security** | **Manage Data Warehouse**. On the **Data Warehouse IP Allowlist** tab, add an IPv4 or IPv6 range in CIDR notation with a short description.

## Improve System Security with an SFTP IP Allowlist

Use an SFTP IP Allowlist to improve system security and to help prevent
unauthorized access to your SFTP account. After an administrator adds at least
one IP address or range, Interaction Studio permits connections only from the
IP addresses and ranges on the allowlist. If your allowlist is empty,
Interaction Studio permits connections from any IP address.

Who: To add IP addresses to the SFTP IP Allowlist, you need administrator
permissions for Interaction Studio.

How: From the main navigation, select **Security** | **Manage SFTP Configuration**. On the **SFTP IP Allowlist** tab, add an IP address or range in CIDR notation with a short description.

