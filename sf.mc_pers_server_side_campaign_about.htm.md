

# About Server-Side Campaigns

Learn about how server-side campaigns work and about implementation roles and
responsibilities.

### Required Editions

Available in: Premium Edition.  
---  
  
## How Server-Side Campaigns Work

Your server calls the Marketing Cloud Personalization server-side API and
provides information about the visitor including the ID, context of the visit,
and visitor actions. Personalization compares the information about the
visitor with the campaign logic and uses a JSON payload to return
recommendations, user attributes, or other campaign data targeted to that
visitor. Your server handles the JSON, builds the message that the visitor
sees, and calls the APIs that track campaign impressions and clicks.

## Responsibilities for Business Users and Developers

Typically, business users and developers work together to build, test, and
publish a server-side campaign.

Business User Responsibilities | Developer Responsibilities  
---|---  
  
  * Create the campaign and define the campaign type as rules-based or A/B.
  * Add targeting logic at the campaign and experience levels.
  * Configure control group allocation.
  * Apply server-side templates to the campaign experiences and complete the template configuration.
  * Track published campaign results in the campaign statistics report.

|

  * Build server-side templates needed for each campaign experience.
  * Configure API calling patterns that align with the campaign's authentication and identity requirements.
  * Configure end systems to render the Personalization JSON response payload.
  * Ensure campaign statistics pass to Personalization and populate the campaign statistics report.

