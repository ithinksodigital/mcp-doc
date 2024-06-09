

# Create an A/B Test Segment

Create an A/B test segment to ensure a user falls into a specific segment
across multiple campaigns. For example, you can also use an A/B test segment
to split campaign traffic into intervals, such as halves, thirds, or quarters.

### Required User Permissions

Permissions Needed  
---  
To create a segment: | A role with Segments Create/Edit permissions  
  
  1. In the **Audiences** section of the main navigation, select **User Segments** | **User Segments**.
  2. Click **New Segment**.
  3. Enter a **Segment Name** that describes its purpose.
  4. Select **Campaigns** from the **Select Category** dropdown. 
  5. Select **A/B Test Segment** from the **Select Campaigns Rule** dropdown.
  6. Enter the percentages for the **Total population** range fields. See [A/B Test Intervals](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_a_b_test_interval.htm&language=en_US&type=5 "Learn how A/B test segments can split campaign traffic into intervals, such as halves, thirds, and quarters.") for more information.

![0aee5174-8e5c-49ff-9b8b-fd542c5543cb]

Note The upper limit for the segment’s range isn’t inclusive. So, a segment
with a range of 0–25% includes only users that are grouped between 0% and 25%,
and not the users in the 25% group.

  7. Click **Save**.

