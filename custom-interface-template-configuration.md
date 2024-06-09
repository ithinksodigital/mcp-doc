# Custom Interface and Template Configuration

The Gears configuration system enables the development of custom interface
configurations to users of the Marketing Cloud Personalization UI. With this
system, a Gear developer can tailor the setup interface for business
requirements. These custom interface configurations can be used in the
development of Personalization Campaign Templates as well as configuration
screens within the Gears system.

The following Gear types support configuration:

  * GearLifecycle
  * SegmentExporter
  * UserSegmentRule
  * AccountSegmentRule
  * ContextualRule
  * CampaignTemplate

The specification of configuration inputs is done by adding properties to the
configurable component. Configuration types can also be shared with
CampaignTemplate gears so that templates can use the configuration objects
from gears providing campaign services. For example, the
`RecommendationConfiguration` class provides the user interface for users to
configure the use of calls to the recommendation service.

Configurable types have child properties that are rendered into the UI in the
order they display in the page. Property types define the inputs that are
rendered. The following example defines a single text input box with the Title
"Simple Property". Titles of form fields are automatically converted from
camel case to title case.

![c0661c0a-85f3-4036-8e7f-523b8f43b7df]

