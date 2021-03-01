---
unique-page-id: 37357059
description: OAuth with Azure Active Directory for Dynamics CRM - Bizible - Product Documentation
title: OAuth with Azure Active Directory for Dynamics CRM
---

# OAuth with Azure Active Directory for Dynamics CRM {#oauth-with-azure-active-directory-for-dynamics-crm}

## Who’s Affected {#who-s-affected}

This setup is for new Bizible customers using Dynamics CRM with an Azure Active Directory (AAD) account, or for customers that want to migrate from their legacy username and password login to Azure Active Directory with OAuth.

>[!NOTE]
>
>For both of these scenarios, AAD is set up here to facilitate connecting your Dynamics instance in Bizible as a Data Provider.

## Set Up New Application {#set-up-new-application}

1. Sign-in to your [Azure Portal](https://portal.azure.com/#home).

1. Choose your Azure AD tenant by clicking on your account in the top-right corner of the page, followed by clicking on the Switch Directory navigation and then selecting the appropriate tenant (skip this step if you only have one Azure AD tenant under your account or if you've already selected the appropriate Azure AD tenant).

   ![](assets/setup-2.png)

1. Search for "Azure Active Directory" in the search bar and click the name to open.

   ![](assets/setup-3.png)

1. Click **App Registrations** in the left-hand menu.

   ![](assets/setup-4.png)

1. Click **New Registration** at the top.

   ![](assets/setup-5.png)

1. Follow the prompts and create a new application. It doesn't matter if it's a web application or a public client (mobile & desktop) application, but if you'd like specific examples for web applications or public client applications, check out our [quickstarts](https://docs.microsoft.com/en-us/azure/active-directory/develop/v1-overview).  
   a. Name is the application name and describes your application to end users.  
   b. Under Supported account types, select Accounts in any organizational directory and personal Microsoft accounts.  
   c. Provide the Redirect URI. For Web Applications, this is the base URL of your app where users can sign in. For example, `http://localhost:12345`. For public client (mobile & desktop), Azure AD uses it to return token responses. Enter a value specific to your application. For example, `http://MyFirstAADApp`.

1. Once you've completed registration, Azure AD will assign your application a unique client identifier (the Application ID). You need this value in the next section, so copy it from the application page.

1. To find your application in the Azure portal, click **App Registrations**, then click **All Applications**. Open your newly created application

1. Click **Authentication** in the left-hand menu.

   ![](assets/setup-9.png)

1. Add Bizible’s redirect URLs: `https://apps.bizible.com/OAuth2` and `https://apps.bizible.com/OAuth2?identityOnly=true` to the list of Redirect URLs.

   ![](assets/setup-10.png)

1. Navigate to the API Permissions tab and make sure the correct permissions are assigned to the application.

   ![](assets/setup-10a.png)

1. From here, enter “enterprise” in the search box and click on Enterprise Applications

   ![](assets/setup-11.png)

1. Again, find and open your new application from the list of applications

1. From the Permissions tab, click **Grant Admin Consent for (instance name)**.

   ![](assets/setup-13a.png)

1. Click **Accept**.

   ![](assets/setup-13b.png)

1. From the "Users and Groups" tab, make sure that the valid "Users and Groups" are assigned to the Application.
  
   ![](assets/setup-14.png)

## Creating an Application User {#creating-an-application-user}

Once the application registration is done, then an application user can be created.

1. Navigate to your Common Data Service environment (`https://[org].crm.dynamics.com`).

1. Navigate to **Settings** > **Security** > **Users**.

1. Choose **Application Users** in the view filter.

1. Select **+ New**.

1. In the Application User form, enter the required information.

   >[!NOTE]
   >
   >* The user name information must not match a user that exists in the Azure Active Directory.
   >
   >* In the Application ID field, enter the application ID of the app you registered earlier in the Azure AD.

1. If the setup is correct, then after selecting **Save**, the **Application ID URI** and **Azure AD Object Id** fields will auto-populate with correct values.

1. Before exiting the user form, choose **Manage Roles** and assign a security role to this application user so that the application user can access the desired organization data.

## Connecting your Dynamics Instance via OAuth {#connecting-your-dynamics-instance-via-oAuth}

1. When setting up your Dynamics connection for the first time, follow steps 1-5 of the "CRM as a Data Provider" section in [this article](/help/bizible-and-dynamics/getting-started-with-bizible-and-dynamics/microsoft-dynamics-crm-installation-guide.md).

1. When prompted for OAuth credentials, fill in the Client Id, Client Secret, and Application Id URI that were set up in the section above.

  a. Client Id is the Id from Step #7 in the section above. If you didn’t write it down, the Application Id is displayed in the Settings of the App registration.

  b. Client Secret is the application secret created in the Azure Portal for your application under Certificates & Secrets.

   ![](assets/creating-2e.png)
  
  c. Application ID URI is the URL of the target web API (secured resource). To find the App ID URL, in the Azure Portal, click Azure Active Directory, click Application registrations, open the application's Settings page, then click Properties. It may also be an external resource like `https://graph.microsoft.com`. This is normally the URL of the dynamics instance.

1. After you click **Submit**, you’ll be prompted to sign-in with Azure Active Directory. When the authentication is successful, your Dynamics account will be connected as a data provider within Bizible.

## Re-authenticating your Dynamics Account {#re-authenticating-your-dynamics-account}

1. When you’re in the Bizible application, go to **My Settings** > **Settings** > **Connections**.

1. Click on the key icon in the CRM section next to the Dynamics connection.

1. Once the key is clicked, a pop-up will appear and you’ll be prompted to enter the Client Id, Client Secret, and Application Id URI, similar to the signup flow.

   ![](assets/re-authenticating-3.png)

1. After you click **Submit**, you’ll be prompted to sign-in with Azure Active Directory. When the authentication is successful, your Dynamics account will be re-authorized within Bizible.
