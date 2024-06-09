

# Configure an SFTP IP Allowlist

Use SFTP IP allow lists to improve system security. Using allowlists to
identify individual IP addresses or ranges of IP addresses that belong to your
network, Personalization can prevent bad actors from gaining SFTP access. If
you don’t create an allowlist, or your allowlist is empty, Personalization
accepts SFTP connections from any IP address.

### Required User Permissions

Permissions Needed  
---  
To modify the SFTP IP allowlist: | Administrator permissions  
  
  1. From the main navigation, select **Security** | **Manage SFTP Configuration.**
  2. On the SFTP Configuration screen, click the **SFTP IP Allowlist** tab.
  3. To add an IP address or range, click **Add IP Range**.
  4. Enter an IPv4 or IPv6 range in [CIDR notation](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation). For example:

**IPv4 range:** 54.161.29.212/24

**IPv6 range:** 2001:db8:1234::/48

  5. Enter a short description for the IP range, such as `Office Network`.
  6. To save the entry, click the check mark. 
  7. To delete an IP range, click the trash can.

