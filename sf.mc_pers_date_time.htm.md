

# Dates and Times in Personalization

Learn how dates and time work in Marketing Cloud Personalization.

## Values Stored in UTC but Shown in Local Timezone

In Marketing Cloud Personalization, dates and times are displayed in the local
timezone. However, the underlying data values are stored in Coordinated
Universal Time (UTC). UTC, which is a standard and not a timezone, maps to
Greenwich Mean Time (GMT), which is a timezone.

## Date and Time Range

For some features (including segments, unified customer profile, and
campaigns), you can adjust the date and time range to reflect the time period
you’re interested in. Examples:

  * Event stream: local time
  * Campaign scheduling: local time
  * Segments: UTC

## Dates in Reports and Campaign Statistics

When analyzing data or selecting dates for reports or campaign statistics:

  * If a visitor enters or leaves daylight savings time (DST), the configured time can move by one hour.
  * Many activities in Marketing Cloud Personalization are aggregated at day or hour boundaries. Because these buckets are defined in terms of UTC, it’s possible to see a day bucket that begins and ends at 8PM EST, because that equates to midnight UTC.
  * When you select or enter a specific time, or when you see a displayed time, it is in your browser's timezone. If you specify a date range, it includes midnight GMT to midnight GMT and includes the start and end days.
  * Exported data formats times are in UTC.

