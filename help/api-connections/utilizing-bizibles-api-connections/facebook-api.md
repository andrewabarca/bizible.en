---
unique-page-id: 18874680
description: Facebook API - Bizible - Product Documentation
title: Facebook API
---

# Facebook API {#facebook-api}

## Introduction {#introduction}

Similar to our AdWords & Bing Ads integrations, our Facebook integration does two fundamental actions:  

* Auto-tag all Facebook Ads with a Bizible parameter (_bf)
* Download ad cost information across all active Facebook ads

## How to Configure the Facebook Integration {#how-to-configure-the-facebook-integration}

As for setup, there are seven steps to be completed within Bizible's app.

1. Navigate to [apps.bizible.com](https://apps.bizible.com) and log-in.
1. Under My Account select **Settings**.
1. Under Integrations select **Connections**.
1. Select **Set Up New Ads Connection** and a pop-up will appear. Select **Facebook** and log-in using your Facebook credentials.

   >[!NOTE]
   >
   >The person connecting the Facebook Ads account needs to be an admin within the Facebook Ads account.

1. Once Bizible is connected to your Facebook account, click the pencil icon next to the account.
1. Within this view, move the 'Auto-tagging?' toggle to 'Yes.' Then select the check box found in the Learn More section to agree to the terms and conditions. Make sure the Auto-tagging toggle is still set to 'Yes'.

## Connecting the Account {#connecting-the-account}

![](assets/1.gif)

## Enabling Autotagging {#enabling-autotagging}

>[!NOTE]
>
>If you enable auto-tagging, we'll reset the conversion history and social proof of all of the ads that we tag. We highly recommend [exporting this data as a CSV](https://www.facebook.com/business/help/205067636197240) before you enable auto-tagging.

![](assets/2-2.png)

Once you've enabled the integration, Bizible will start downloading ad level cost into the Bizible Marketing ROI Dashboard.

For the integration to properly work, you'll need to enable auto-tagging on your Facebook account. This will allow our system to add a _bf parameter across all ad links. This process will add the new parameter on top of any other tracking parameters you've already added to your Facebook ads.

![](assets/3.gif)

## Field Mapping {#field-mapping}

<table> 
 <colgroup> 
  <col> 
  <col> 
 </colgroup> 
 <tbody> 
  <tr> 
   <th><p><strong>Touchpoint Field</strong></p></th> 
   <th><p><strong>Value</strong></p></th> 
  </tr> 
  <tr> 
   <td><p>Ad Campaign Id</p></td> 
   <td><p>[Facebook Campaign Id]</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad Campaign Name </p></td> 
   <td><p>[Facebook Campaign Name], or [utm_campaign] if provided</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad Group Id</p></td> 
   <td><p>[Facebook Ad Set Id]</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad Group Name</p></td> 
   <td><p>[Facebook Ad Set Name]</p></td> 
  </tr> 
  <tr> 
   <td><p>Touchpoint Source</p></td> 
   <td><p>???Facebook???, or [utm_source] if provided</p></td> 
  </tr> 
  <tr> 
   <td><p>Medium</p></td> 
   <td><p>???Social???, or [utm_medium] if provided</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad Id, or Creative_Unique_Id (Data Warehouse)</p></td> 
   <td><p>[custom Id generated from utm_content]</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad Content, or Creative_Name (Data Warehouse)</p></td> 
   <td><p>[utm_content] if provided</p></td> 
  </tr> 
  <tr> 
   <td><p>Keyword Text, or Keyword_Name (Data Warehouse)</p></td> 
   <td><p>[utm_term] if provided</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad_Unique_Id (Data Warehouse)</p></td> 
   <td><p>[Facebook Ad Id]</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad_Name (Data Warehouse)</p></td> 
   <td><p>[Facebook Ad Name]</p></td> 
  </tr> 
  <tr> 
   <td><p>Keyword_Unique_Id (Data Warehouse)</p></td> 
   <td><p>[custom Id generated from utm_term]</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad_Provider (Data Warehouse)</p></td> 
   <td><p>???Facebook???</p></td> 
  </tr> 
  <tr> 
   <td><p>Account_Unique_ID (Data Warehouse)</p></td> 
   <td><p>[Facebook Account #]</p></td> 
  </tr> 
  <tr> 
   <td><p>Account_Name (Data Warehouse)</p></td> 
   <td><p>[Facebook Account Name]</p></td> 
  </tr> 
 </tbody> 
</table>

## FAQ {#faq}

**Q: What Facebook Ads are supported by Bizible?**

A: Carousel, Single Image. Not Video, Slideshow or Collection at this time.

**Q: What is social proof?**

A: Social proof is visible engagement such as likes, clicks, comments, and shares.

**Q: What happens when Bizible tags the Ad?**

A: Facebook does not allow ads to be edited so Bizible needs to delete the creative, which contains the Destination URL, and then re-create the ad with the new parameters.

**Q: Why does Bizible update all Facebook Ads?**

A: Bizible's process is to tag all ads in case they are re-activated.

**Q: What permission does the connected user need?**

A: ads_management, email

**Q: How long can it take to import spend data?**

A: 1 hour

**Q: How long can it take to import ad data?**

A: 4 hours
