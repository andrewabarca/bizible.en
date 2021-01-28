---
unique-page-id: 42762749
description: Marketo Engage Activities Integration - Bizible - Product Documentation
title: Marketo Engage Activities Integration
---

# Marketo Engage Activities Integration {#marketo-engage-activities-integration}

As part of the overall Bizible and Marketo Engage Integration, this effort to pull in Marketo Activities plays a huge role. Through Marketo Activities, the system tracks events such as Click Email, Change Score or Change Status in Progression - these activity types can be pared down and defined to select a subset that are eligible for touchpoints. Once touchpoints are created on these activities, they get tracked in the engagement journey and measured alongside your other marketing channels such as Paid Search or Partner Marketing.

## Requirements {#requirements}

* Production Marketo instance
* Production Salesforce or Microsoft Dynamics instance
* Any paid Bizible subscription
* Marketo People Sync Enabled (Bizible Settings)
* Marketo Programs Enabled (Bizible Settings)
* Marketo Activities Enabled (Bizible Settings)

## Setup {#setup}

1. To begin setting up Marketo Activities, navigate to **My Account** > **Settings** > **Activities**.

   ![](assets/one-1.png)

   ![](assets/two-1.png)

   The first thing required is to select the list of Activity Types that you plan to build rules on. There is no hard number of activity types required, but we also recommend that you don’t overload your touchpoints and dilute the importance of significant milestones. With that said, you may not need more than 5 activity types to track the relevant engagements.

1. Click the drop-down menu under Select Activities Types to begin choosing the various types.

   ![](assets/three-1.png)

1. Once all the activities you need are selected, you will also see them populated in your Selected Activities List as well as under Define Rules.

   ![](assets/four-1.png)

1. For each Activity Type, you’ll need to define one or more rules that determine which records are eligible for touchpoints. For our example, we will add a rule for the “Change Score” activity type so that the system will create a touchpoint when a Marketo Person reaches a score of 90 or greater.

1. First, depending on the Activity Type, you may need to set up a Bizible Campaign Name that can be used later on for channel mapping. Bizible Campaign Names can be re-used across multiple rules. This helps have broader names that can be used in a single channel rule. Not all Activity Types contain a Marketo Program, hence the need for a name as this first step.

   Here’s an example of what that extra step would look like:

   ![](assets/five-1.png)

1. In our “Change Score” example, we don’t need to enter a Campaign Name since we can pull that information from the Marketo Program. Now you can create the rule expression. Following our example, we want to select the field “New Value” with an operator of “is greater than” with a value of 90.

   You can expand on the rules and add additional filters or criteria by adding “and” or “or” statements to narrow down the results.

   ![](assets/six-1.png)

   ![](assets/seven-1.png)

1. Lastly, choose what we should use as the Touchpoint Date. All available date or date/time fields will appear here from Marketo. Unless you have custom date fields, you will see “Activity Date.”

   ![](assets/eight-1.png)

1. Be sure to click **Save As Draft** along the way so that you don’t lose your changes.

   ![](assets/nine-1.png)

1. Navigate to the **Attribute Mapping** tab.

   ![](assets/ten-1.png)

1. For each Activity Types that you selected, you have the option of mapping additional Marketo attributes to Touchpoint fields so that you can view and report off those values in Bizible Discover or in the CRM.

   Many of the fields have automatically been mapped and cannot be changed in order to be consistent with our other integrations. Reference the Field Mappings section below to find those values. For some activity types, Marketo includes attributes for a landing page, or referrer page, or browser that you can optionally map to a Touchpoint field. In the example below, we’ve made some additional suggestions that can be removed.

1. Select the Bizible Touchpoint field from the left column that you'd like to map to. Then, choose the Marketo Attribute that you want to populate in the Bizible Touchpoint field. Remember that these are optional, additional mapping on top of those that Bizible has already established.

   Mappable Fields:

    * City
    * Country
    * Region
    * Landing Page
    * Referrer Page
    * Form Page
    * Form Date
    * Platform
    * Browser

   >[!NOTE]
   >
   >Ad fields such as Ad Content or Keyword are not available in this list, as they reserved for our ad platform integrations.

## Activity Types {#activity-types}

Some activity types provide us with the Program Id and Program Name, so it’s easy to map that into the Campaign Id and Campaign Name on the Bizible Touchpoint. For others, there is no program association, so part of the rules definition will require you to create a Bizible Campaign Name. Below are lists of each category:

**Activity Types with Program Id**

Send Email (6)  
Email Delivered (7)  
Email Bounced (8)  
Unsubscribe Email (9)  
Open Email (10)  
Click Email (11)  
Change Data Value (13)  
Change Score (22)  
Add to List (24)  
Change Status in Progression (104)  
Add to Nurture (113)  
Change Nurture Cadence (115)

>[!NOTE]
>
>Of the Activity Types where we expect a Program Id, if an activity is detected without a program, Bizible will not accept that as an eligible touchpoint since we cannot have null Campaign values.

**Activity Types without Program Id**

Click Link (3)  
New Lead (12)  
Sync Lead to SFDC (19)  
Convert Lead (21)  
Change Owner (23)  
Remove from List (25)  
SFDC Activity (26)  
Email Bounced Soft (27)  
Delete Lead from SFDC (29)  
Merge Leads (32)  
Add to Opportunity (34)  
Remove from Opportunity (35)  
Update Opportunity (36)  
Delete Lead (37)  
Send Alert (38)  
Send Sales Email (39)  
Open Sales Email (40)  
Click Sales Email (41)  
Add to SFDC Campaign (42)  
Remove from SFDC Campaign (43)  
Change Status in SFDC Campaign (44)  
Receive Sales Email (45)  
Request Campaign (47)  
Sales Email Bounced (48)  
Change Revenue Stage (101)  
Change Revenue Stage Manually (102)  
Change Segment (108)  
Call Webhook (110)  
Sent Forward to Friend Email (111)  
Received Forward to Friend Email (112)  
Change Nurture Track (114)  
Push Lead to Marketo (145)  
Sync Lead to Microsoft (300)  
Share Content (400)  
Custom Activity (xxx)

## Channel Mapping {#channel-mapping}

For any of the rules from an Activity Type with a Program Id, the Marketo Program Channel is determined from the Program. We use the Program Channel to map to your custom Offline Channels, so you’ll need to make sure your channels are configured properly [as instructed here](/help/bizible-and-marketo/bizible-integrations-with-marketo/marketo-engage-programs-integration.md#channel-mapping).
  
And for any of the rules from an Activity Type without a Program Id, your first step was to create a Campaign Name. Use this Campaign Name to set up your custom Online Channels [laid out here](/help/channel-tracking-and-setup/online-channels/online-custom-channel-setup.md).
  
If Channels for your Marketo Activities aren’t properly configured, it’s likely your new touchpoints will fall under the “Other” channel.

## Program Costs {#program-costs}

Through the data import of Marketo Programs, costs are automatically downloaded from Period Costs and the reported cost in Marketo is distributed throughout the assigned month. For example, if $1000 is reported for January 2021, the $1000 is split across 31 days. The costs can be found in Bizible Discover.

## Cookie Mapping {#cookie-mapping}

As a result of Bizible’s integration with Marketo, the Bizible Cookie Id is also now mapped and synced with the Marketo Munchkin Id. This helps close the gap to attribute the anonymous first touch to a web session rather than attributing both the FT and LC touches to a Marketo Activity. Imagine this scenario:

Mark clicks on a Facebook ad and lands on wayneenterprises.com where he gets cookied with Bizible Id 123 and Marketo Munchkin Id 456. No form fill takes place.
  
The Wayne Enterprises Marketing team sends out an email blast to specific targeted leads, one of them being `mark@email.com`.  
  
`mark@email.com` receives the email and clicks through and lands on `wayneenterprises.com`. This becomes `mark@email.com's` second visit to `wayneenterprise.com` with the same cookie Ids, but there was no form fill, so to Bizible, they are still an anonymous visitor.  
  
The Wayne Enterprises Marketing team creates a Marketo Activity rule to generate touchpoints for a "Click Email" activity type.  
  
Today's implementation would create a single FT and LC touchpoint for `mark@email.com` from the Marketo Activity from the "Click Email" activity type.  
  
With this cookie mapping enhancement, the FT would go back and get credited to the Facebook ad and the LC would get credited to the Email.

## FAQ {#faq}

**How do I know whether to create a Marketo Programs rule or a Marketo Activities rule?**

The Marketo Engage Programs Integration is a simple way to generate touchpoints based on whether or not a Person is a program member of a program. If you’re interested in defining a rule based on the time a Person changes to a particular Program status, the Marketo Engage Activities Integration will be the setup you’ll want, specifically the “Change Status in Progression” activity type so that your Touchpoint Date can be mapped to the system generated Activity Date.

**Why is the name of my Touchpoint Type truncated?**

The Touchpoint Type field was created in the Bizible package with 16 characters. Unfortunately, changing the character limit of the field would require deprecating the existing field and creating a new one. The value of the Touchpoint Type is the Activity Type, which is also set in the Medium field.

**Why does my Custom Activity Type not appear in the list of available activities?**

We only show “Approved” custom activity types and not Draft or Approved with Draft.

**How do I determine which Activity Types I want to generate a touchpoint for?**

Although there is no limit on the number of Activity Types you can create, we generally recommend no more than 5 activity types. It takes time to determine which marketing activities are relevant enough to be part of the touchpoint journey. For example, “Unsubscribe Email” may not be a significant touchpoint to track, but “Click Email” with additional filters might be a good one. This varies by each organization and each team, so we suggest you work with your teams to brainstorm on the best approach here.

**Why is my Browser Name cut off?**

Bizible’s Browser Name has a hard limit of 20 characters, although the User Agent value we get from Marketo tends to be a longer string.

BrowserInfo.Name  
BrowserInfo.Version  
PlatformInfo.Name  
PlatformInfo.Version
