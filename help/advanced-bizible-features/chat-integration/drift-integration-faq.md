---
unique-page-id: 27656441
description: Drift Integration FAQ - Bizible - Product Documentation
title: Drift Integration FAQ
---

# Drift Integration FAQ {#drift-integration-faq}

As a part of Bizible's integration with Drift, we've outlined some of the most frequently asked questions. If there are any questions not outlined below, please reach out to your Customer Success Manager or support@bizible.com.

**How is the integration enabled?**

Drift Chat tracking for Bizible is enabled by default. If for any reason you want to disable it (and not create Touchpoints from Drift Chats by default), we will need an additional attribute added to your Bizible Javascript implementation, bolded below:

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="" id="bizible-settings" data-chatEnabled="false"></script>`

For those using Google Tag Manager to load the Bizible Script, if you want to exclude your Drift Chats from being Touchpoint-eligible, you’ll need to add to following `<span>` right after your Bizible Script:

`<span id="bizible-settings" data-chatEnabled="false"></span>`

**What does the integration do?**

The integration now allows Bizible to track when an end-user provides their email address in a Drift chat. From there we create touchpoints from these interactions with a Touchpoint Type of "Web Chat." This integration allows marketers to understand the performance of their chat interactions, along with the channels/sub-channels/campaigns that drive people to interact with these chats.

**What if I track Drift via campaign sync rules?**

If there are any campaign sync rules in place to create touchpoints for Drift chat interactions, you'll need to ensure you stop adding those particular end-users into the corresponding CRM Campaign. Otherwise once the feature bit is enabled we will create a CRM Campaign touchpoint and digital touchpoint for one Drift chat interaction.

**What if I track Drift via CRM Campaigns?**

If there are CRM campaigns in place to create touchpoints for Drift chat interactions, a Touchpoint End Date will need to be set on those specific campaigns (the Touchpoint End Date should be the date the Web Chat Integration feature bit is enabled).

**What if I track Drift via Activities?**

If there are activity rules in place to create touchpoints for Drift chat interactions, an additional piece of logic will need to be added to the rules. You'll need to add logic using the Task Created Date field to prevent duplication of touchpoints from being created (IE CrmTask.CreatedDate is Less Than the date in which the feature bit was enabled). See screenshot below for example.

![](assets/activity-rule-drift.png)

