---
unique-page-id: 37356027
description: Bizible Quick Start - Bizible - Product Documentation
title: Bizible Quick Start
---

# Bizible Quick Start {#bizible-quick-start}

We understand that not all Marketing teams want (or have access) to run marketing reporting out of the CRM, whether it’s because of limited access, CRM ownership, longer time to value, or legal implications. Going down the path of Bizible Quick Start gives you the ability to effectively implement and run Bizible with as little reliance on the CRM as possible.

## Standard Bizible Installation {#standard-bizible-installation}

Through the standard Bizible installation, you're required to install a Salesforce Package or a Microsoft Dynamics Managed Solution. The installation includes custom objects/entities and custom fields that are added to the CRM that Bizible can then write data to. This ultimately leads to a longer onboarding time due to tracking down the appropriate owner/administrator, creating new users and profiles, and getting through security clearances to install to a production instance—and sometimes creating a separate workstream to test out the installation in a sandbox instance.

Although having a package presents Bizible data in its full capacity inside the CRM, we find it’s not always necessary given the various use cases. If reporting can be conducted outside of the CRM (such as within Bizible Discover or an external Data Warehouse), Bizible Quick Start is a fast and easy way to get set up with Bizible without having to install the Bizible package.

## How It Works {#how-it-works}

* Robust JavaScript & Integrations

  * High quality data straight from the source
  * Bizible.js for on-site behavior, reading UTM parameters, referral sources, and more
  * Integrations with prominent ad networks and martech providers for for streamlined, granular data

* CRM Authorization

  * Still need authorization to read data from the CRM for lead, contact, and opp data

* Customization in apps.bizible.com

  * Customize configuration in apps.bizible.com instead of in the CRM

    * Channels and subchannels
    * Segments
    * Stages
    * Attribution model weighting

* CRM Campaign Sync

  * One of those customizations enables customers to connect CRM campaign data to the right fields through the Campaign Sync feature
  * Write rules in apps.bizible.com to determine which campaigns and conditions receive touchpoints
  * Far less effort required compared to CRM package installation

* Reporting in Discover & Data Warehouse

  * Report where you want:

    * Bizible Discover — couples unparalleled performance data with impactful visualizations
    * Data Warehouse — connect your attribution data with other datasets and report in your BI tool

## Permissions {#permissions}

Bizible requires access to standard Salesforce objects such as Leads and Contacts. We strongly recommend having an integration user or a dedicated Bizible Administrator Salesforce user serve as the connected user, as they will have the proper data access privileges.

In order to ensure that all data is properly pulling from Salesforce, we require the following security and accessibility settings: View All Data for the Profile of the dedicated user. This permission set gives Bizible the access needed to download data from standard objects. This permission set is at profile level.

## Setup up your Identity Provider and Data Connections {#setup-your-identity-provider-and-data-connections}

The guides below outline the steps to set up your Adobe Admin Console, configure your Identity Provider, and connect your CRM and Ad Accounts.

Salesforce customers, click [here](/help/configuration-and-setup/bizible-and-salesforce/bizible-installation-guide.md).

Microsoft Dynamics customers, click [here](/help/bizible-and-dynamics/getting-started-with-bizible-and-dynamics/microsoft-dynamics-crm-installation-guide.md).

Once you complete all of the above steps, you're good to go. If you run into any issues along the way, please don’t hesitate to reach out to your Bizible representative or support@bizible.com.

>[!NOTE]
>
>If you go through Bizible Quick Start then later decide to install the package into your CRM, that won't be an issue.
