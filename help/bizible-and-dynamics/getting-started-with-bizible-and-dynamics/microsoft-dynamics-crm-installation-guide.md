---
unique-page-id: 18874763
description: Microsoft Dynamics CRM Installation Guide - Bizible - Product Documentation
title: Microsoft Dynamics CRM Installation Guide
---

# Microsoft Dynamics CRM Installation Guide {#microsoft-dynamics-crm-installation-guide}

## Supported Versions {#supported-versions}

Bizible supports the following Microsoft Dynamics CRM versions:

* Microsoft Dynamics 2016 (Online and On-Premise)
* Microsoft Dynamics 365 (Online and On-Premise)

For connection and authentication, Bizible supports the following Active Directory Federated Services (ADFS) versions:

* ADFS 4.0 - Windows Server 2016
* ADFS 5.0 - Windows Server 2019

## Install the Managed Solution {#install-the-managed-solution}

Install the zip file within Dynamics CRM. Your Solutions Engineer will provide you with the installation file via email.

Settings > Customizations > Solutions > Import (button) > Choose File

![](assets/1.png)

>[!NOTE]
>
>The following two screenshots may vary slightly from yours, as they were taken during a solution upgrade.

![](assets/2.png)

![](assets/3.png)

## Bizible User Permissions {#bizible-user-permissions}

We recommend creating a dedicated Bizible User within Dynamics for us to export and import data through to avoid any issues with other users in your CRM. Take note of the username and password as well as the endpoint URL as this will be used when creating the Bizible account.

## Security Roles {#security-roles}

If your organization uses Dynamics Security Roles, please make sure the connected user, or the dedicated Bizible User has sufficient read/write permissions to the required entities.

Security Roles are located here: Settings > Security > Security Roles

For Bizible custom entities, we will need full permissions across all of our entities.

>[!NOTE]
>
>Users who will be closing opportunities also will need the full permissions.

![](assets/4.png)

For Dynamics standard entities, please refer to Bizible’s Dynamics schema document. At a high level, Bizible just needs to read in certain entities in order to gather the appropriate data and write to custom fields that will get installed with the managed solution. We will not create new standard records, nor will we update any standard fields.

## Include Touchpoints on Page Layouts: {#include-touchpoints-on-page-layouts}

1. For each Entity, navigate to the Form Editor. You can either find this under Settings > Customizations > Customize the System > `[Entity]` > Forms. Or you can find it on the settings while you’re viewing a record.

   * The entities to configure: Account, Opportunity, Contact, Lead, and Campaign.

   ![](assets/5.png)

1. Page Layouts: first add a “One Column” tile in the section you want the Touchpoints to live. Within that new column, we will need a sub grid added to each form within your Account, Opportunity, Contact, and Lead entities.

   ![](assets/6.png)

   ![](assets/7.png)

1. Select the object (Bizible Attribution Touchpoints or Bizible Touchpoints) that should render in the subgrid, which depends on the object relationship. Optionally, change the columns that will display by clicking the Edit button. A default layout has been set by the managed solution.

   Bizible Attribution Touchpoint Subgrid - Accounts, Opportunities, and Contact  
   Bizible Touchpoint Subgrid - Leads and Contacts

   ![](assets/8.png)

1. Once you’re done updating the form, publish and save your changes.

## Schema-related Considerations {#schema-related-considerations}

**`Revenue`**

Bizible points to the standard Actual Revenue field by default. If you are not using this, please explain how you report on revenue to your Solutions Engineer or Success Manager as a custom workflow will be needed.

**`Close Date`**

Bizible points to the Actual Close Date field out of the box. If you are not using this or also use the Estimated Close Date field, please explain your process to your Solutions Engineer or Success Manager. A custom workflow may be need to account for both fields.

## Set up Your Adobe Admin Console and Identity Provider {#set-up-your-adobe-admin-console-and-identity-provider}

The first step to using Bizible is to create and sign-in to your provisioned Adobe Admin Console. If you haven't already received the email with log-in instructions, please contact your Bizible Account Representative.

As a product within the Adobe Suite, Bizible leverages the full functionality of Adobe Admin Console for Identity Management.  More resources can be found here: https://helpx.adobe.com/enterprise/using/admin-console.html

We recommend reviewing all of the resources, best practices, and options available to you for Identity Management: https://helpx.adobe.com/enterprise/using/set-up-identity.html

For guidance and review of setting up your Identity Management within the Adobe Admin Console, please reach out to your Bizible Account Representative.

In order to facilitate user authentication and authorization with your Bizible instance(s), the following steps are required within the Adobe Admin Console to setup the appropriate User Groups.

**Setting up User Groups in the Adobe Admin Console**

1. Navigate to https://adminconsole.adobe.com/overview.

1. In the Admin Console, click **Users**.

   ![](assets/microsoft-dynamics-crm-installation-guide-9.png)

1. Click **User Groups**.

   ![](assets/microsoft-dynamics-crm-installation-guide-10.png)

1. Click **New User Group**.

   ![](assets/microsoft-dynamics-crm-installation-guide-11.png)

1. Under User Group Name, enter "BizibleAdmins" and click **Save**.

   ![](assets/microsoft-dynamics-crm-installation-guide-12.png)

1. Click **New User Group** again.

   ![](assets/microsoft-dynamics-crm-installation-guide-13.png)

1. Under User Group Name, enter "BizibleUsers" and click **Save**.

   ![](assets/microsoft-dynamics-crm-installation-guide-14.png)

Now learn how to add people to these groups...

## Adding Users to the Admin Console User Groups {#adding-users-to-the-admin-console-user-groups}

After you've created User Groups, the next step is to grant access to the Bizible application by adding users.

|User Group | Description |
|--- | --- |
|**BizibleAdmins** |these are administrators and power users of the Bizible Application with full ability to update and manage Bizible-specific configuration options |
|**BizibleUsers** |these are standard users of the Bizible Application with read only permissions within the Bizible application |

When adding a user to their respective group, you'll see their [Identity Type listed](http://helpx.adobe.com/enterprise/using/set-up-identity.html).

After a user has been added to a group, they're able to access the Bizible instance by choosing the Sign in with Adobe ID option at https://apps.bizible.com.

   ![](assets/microsoft-dynamics-crm-installation-guide-15.png)

## Configuring your Connections and Data Providers {#configuring-your-connections-and-data-providers}

Once you've logged-in to the Bizible application as a user in the BizibleAdmins group within the Adobe Admin Console, it's time to set up your various data connections.

**CRM as a Data Provider**

1. In your Bizible account, click the **My Account** drop-down and select **Settings**.

   ![](assets/microsoft-dynamics-crm-installation-guide-16.png)

1. Under Integrations in the left nav, click **Connections**.

   ![](assets/microsoft-dynamics-crm-installation-guide-17.png)

1. Click the **Set Up New CRM Connection** button.

   ![](assets/microsoft-dynamics-crm-installation-guide-18.png)

1. Next to Microsoft Dynamics CRM, click the **Connect** button.

   ![](assets/microsoft-dynamics-crm-installation-guide-19.png)

1. Select Credentials or OAuth.

   ![](assets/microsoft-dynamics-crm-installation-guide-20.png)

   >[!NOTE]
   >
   >For more information on OAuth, please visit [this article](/help/bizible-and-dynamics/getting-started-with-bizible-and-dynamics/oauth-with-azure-active-directory-for-dynamics-crm.md). If you have any questions about the process, please contact your Bizible Account representative.

1. In this example, we've chosen Credentials. Enter your credentials and click **Next**.

After connecting, you'll see the details of your Dynamics connection in the CRM/MAP Connections list.

**Ad Account Connections**

To connect your Ad Accounts with Bizible, start by visiting the Connections tab within the Bizible application.

1. Follow Steps 1 & 2 from the above _CRM as a Data Provider_ section.

1. Click the **Set up New CRM Connection** button.

   ![](assets/microsoft-dynamics-crm-installation-guide-21.png)

1. Select your desired platform.

   ![](assets/microsoft-dynamics-crm-installation-guide-22.png)

**Bizible Javascript**

In order for Bizible to track your web activities, there are multiple steps for setup.

1. Click the **My Account** drop-down and select **Account Configuration**.

   ![](assets/microsoft-dynamics-crm-installation-guide-23.png)

1. Enter your phone number. For Website, enter your primary root domain that will be used for Bizible tracking on your website. Click **Save** when done.

   ![](assets/microsoft-dynamics-crm-installation-guide-24.png)

   >[!NOTE]
   >
   >To add multiple root domains, please contact your Bizible Account Representative.

1. The [Bizible JavaScript](/help/bizible-tracking/setting-up-tracking/adding-bizible-script.md) then needs to be placed across the entire site and landing pages. We recommend hardcoding the script within the head of your landing pages or adding through a Tag Management System such as [Google Tag Manager](/help\bizible-tracking\setting-up-tracking\adding-bizible-script-via-google-tag-manager.md).
