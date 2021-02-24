---
description: Migration to Adobe Admin Console - Bizible - Product Documentation
title: Migration to Adobe Admin Console
---

# Migration to Adobe Admin Console {#migration-to-adobe-admin-console}

## Overview {#overview}

**Bizible Migration to Adobe Unified Provisioning Platform**

Starting in February 2021, all Bizible customers provisioned prior to 2021 will be migrated onto the Adobe Admin Console and Identity Management Service (IMS) platform via the Adobe Unified Provisioning Platform. All Bizible accounts and settings will remain the same outside of User Management, which will all occur via Adobe Admin Console and Adobe IMS after the migration.

**What is Adobe Admin Console & Identity Management Service (IMS)?**

Adobe Admin Console provides a central location for managing your Adobe entitlements across your entire organization. With this migration, Bizible becomes another entitlement that is managed centrally through Adobe Admin Console in your organization. Adobe Admin Console provides full product management, user management, role based access controls, and Identity Provider (IdP) integration.

Adobe Identity Management Service (IMS) is the service that provides all authentication between your users and your Adobe products (Bizible being one of those products after migration).

We encourage you to explore all of the details here:

* Adobe Admin Console Overview: [https://helpx.adobe.com/enterprise/using/admin-console.html](https://helpx.adobe.com/enterprise/using/admin-console.html)
* Adobe Admin Console Admin Guide: [https://helpx.adobe.com/enterprise/admin-guide.html](https://helpx.adobe.com/enterprise/admin-guide.html)
* Adobe Identity Management Services Overview: [https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeIdentityServices.pdf](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeIdentityServices.pdf)

**Why is my Bizible account being Migrated to Adobe Admin Console?**

Adobe Admin Console and IMS provide a full suite of functionality for User management, Single Sign On (SSO), and entitlement management. Migrating Bizible accounts into the Adobe platform offers several benefits:

* **Centralized Entitlement & User Management**: With Adobe Admin Console, all Adobe products, entitlements, and users are managed in a centralized location. With this migration, Bizible is now included in the list of your Adobe entitlements and all managed in one location.

* **Extended Functionality & Integrations for User Management**: Adobe Admin Console offers a number of direct integrations with various Identity Providers (IdP), such as Google G-Suite, Azure Active Directory, and Okta.

* **Future Bizible Product Enhancements**: Bizible has a number of product upgrades and new features on the product roadmap. Migrating onto Adobe Admin Console and IMS unlocks future Bizible integrations with various Adobe services and platforms.

**What do I need to do as a part of this Bizible Adobe Admin Console Migration Effort?**

Bizible will send an email to all Bizible administrators on your account when the migration begins. At this point, these administrators will receive an additional email from Adobe letting them know they are now system administrators in Adobe Admin Console, and that the Bizible entitlement has been added.

At this point, you will have a **Migration window of 30 days** to migrate user management from Bizible onto Adobe Admin Console.

>[!NOTE]
>
>During the migration window, all existing Bizible access stays the same. After your migration window is complete, users will be required to log in to Bizible using Adobe Id.

A full checklist and guide for this is [linked below](#adobe-ims-migration-checklist-and-action-items).

During the migration window, previous IdP user login and management functionality will remain active.

After your migration window is complete, all user management and login will occur via Adobe Admin Console and the **Login with Adobe Id** function in Bizible.

>[!NOTE]
>
>For any customers provisioned in September 2020 and beyond, you will already have Adobe Admin Console set up with your initial provisioning of Bizible. In this case, you already have user management set up through Adobe Admin Console.

This migration effort brings full parity for Bizible as an entitlement within your Adobe Admin Console. You will now see your Bizible instance(s) within the Product Context and have Product Profile functionality for managing users and admins in Bizible. At any time you may use the Product Card for User Management (rather than the specific 'BizibleAdmins' and 'BizibleUsers' groups you may have set up). These user groups will remain backward compatible.

![](assets/migration-1.png)

**When will my Bizible account be migrated to Adobe IMS?**

Bizible migrations are scheduled to begin in February 2021 and will take place on a rolling basis throughout the year.

Prior to starting migration for your Bizible accounts, your Bizible administrators will receive an email with additional information.

## Adobe IMS Migration Checklist and Action Items {#adobe-ims-migration-checklist-and-action-items}

Listed below is an overview of the changes that will occur as a result of migrating to Adobe Admin Console and the actions to take during the migration window:

**Before Migration**

| Action | Description | Additional Details |
|--- |--- |--- |
| Review User Management and any SSO Settings in Bizible | Bizible user management can be seen within apps.bizible.com on the 'Users.View/Add Account Users' tab.<br /> Any Bizible SSO setup can be seen within apps.bizible.com on the 'Security.Authentication' tab.<br /> When the migration starts, you will likely want to setup all Bizible users and settings present on these tabs within Adobe Admin Console to keep a consistent experience. | <a href="assets/migration-2.png"><img src="assets/migration-2.png" alt="Click to enlarge"></a>
| Review Your Organizations Identity Provider (IdP) | When transitioning User Management from Bizible (and your CRM) to Adobe Admin Console, many organizations take advantage of Federated Identities. This allows your organization to manage all user credentials. More details can be seen <a href="https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/identity.ug.html">here</a>.<br /> We recommend reviewing your Identity Provider and desired User Management strategies to help facilitate and accelerate your Bizible Adobe Admin Console migration. | [https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/identity.ug.html](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/identity.ug.html) |

**During Migration**

<table> 
 <colgroup> 
  <col> 
  <col>
  <col> 
 </colgroup> 
 <tbody> 
  <tr> 
   <td><b>Action</b></td> 
   <td><b>Description</b></td>
   <td><b>Additional Details</b></td>  
  </tr> 
  <tr> 
   <td>Log in to Your Adobe Admin Console</td> 
   <td>Once your account has started the migration process, all Bizible admins for your account will be added as System Administrators to your new Adobe Admin Console.  These person(s) will receive an automated email from Bizible.<br /> These person(s) will be able to log in to Adobe Admin Console and begin all setup like outlined <a href="https://experienceleague.adobe.com/docs/bizible/using/configuration-and-setup/bizible-and-salesforce/bizible-installation-guide.html?lang=en#set-up-your-adobe-admin-console-and-identity-provider">here</a>.<br /> Note that if your organization already has an Adobe IMS Organization, no new admins will be added by Adobe during the migration.<br /> Any system administrators will also receive an email alerting them to their new Bizible account setup.</td>
   <td> <a href="assets/migration-3.png"><img src="assets/migration-3.png" alt="Click to enlarge"></a><br /> <a href="https://experienceleague.adobe.com/docs/bizible/using/configuration-and-setup/bizible-and-salesforce/bizible-installation-guide.html?lang=en#set-up-your-adobe-admin-console-and-identity-provider">https://experienceleague.adobe.com/docs/bizible/using/configuration-and-setup/bizible-and-salesforce/bizible-installation-guide.html?lang=en#set-up-your-adobe-admin-console-and-identity-provider</a></td>  
  </tr>
  <tr> 
   <td>Review Adobe Admin Console and User Management Roles</td> 
   <td>Review the Adobe Admin Console Overview and User Management options available:

* [Adobe Admin Console Overview](https://helpx.adobe.com/enterprise/using/admin-console.html)

* [Adobe Admin Console Admin Guide](https://helpx.adobe.com/enterprise/admin-guide.html)</td>
   <td><a href="https://helpx.adobe.com/enterprise/using/admin-console.html">https://helpx.adobe.com/enterprise/using/admin-console.html</a><br /> <a href="https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html">https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html</a></td>  
  </tr> 
  <tr> 
   <td>Setup Identity Provider and SSO in Adobe Admin Console (optional)</td> 
   <td>When transitioning User Management from Bizible (and your CRM) to Adobe Admin Console, many organizations take advantage of Federated Identities.  This allows your organization to manage all user credentials. More details can be seen <a href="https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/identity.ug.html">here</a>.</td>
   <td><a href="https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/identity.ug.html">https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/identity.ug.html</a></td>  
  </tr> 
  <tr> 
   <td>Set up Bizible Users and Admins in Adobe Admin Console</td> 
   <td>Whatever Identity types you wish to use, you will need to add the list of Bizible Users and Admins to the Bizible product card within Adobe Admin Console.<br /> This will allow these users to login to apps.bizible.com using the 'Login with Adobe Id' option.<br /> More information can be seen <a href="https://experienceleague.adobe.com/docs/bizible/using/configuration-and-setup/bizible-and-salesforce/bizible-installation-guide.html?lang=en#set-up-your-adobe-admin-console-and-identity-provider">here</a>.</td>
   <td><img src="assets/migration-4.png"></td>  
  </tr> 
  <tr> 
   <td>Log in to Bizible using Adobe Id</td> 
   <td>During migration, all existing users can continue to login to Bizible using the CRM login during the 30 day migration.  After migration users will only be able to login to Bizible if they are setup in Adobe Admin Console and login with the Adobe ID option.</td>
   <td><img src="assets/migration-5.png"></td>  
  </tr> 
 </tbody> 
</table>

## FAQ {#faq}

**Will any aspects of my Bizible set up change as a part of my migration to Adobe Admin Console?**

Only User Management and any SSO configurations will change as a part of this migration. All other Bizible functionality remains the same.

**My organization already has Adobe Admin Console & IMS for other Adobe products. How will my migration be affected?**

If you already have Adobe Admin Console and IMS, your Bizible instance(s) will appear as additional products within your Adobe Admin Console after migration. Bizible will be managed the same as any other Adobe products.

**What type of security does Adobe Admin Console & Identity Management Service Offer?**

Please see full [details here](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeIdentityServices.pdf).

**How do I set up my company Identity Provider (IdP) within Adobe Admin Console?**

Azure: [https://helpx.adobe.com/enterprise/using/sso-setup-azure.ug.html](https://helpx.adobe.com/enterprise/using/sso-setup-azure.ug.html)
Google: [https://helpx.adobe.com/enterprise/using/setup-sso-google.ug.html](https://helpx.adobe.com/enterprise/using/setup-sso-google.ug.html)
Okta: [https://helpx.adobe.com/enterprise/kb/configure-okta-with-adobe-sso.html](https://helpx.adobe.com/enterprise/kb/configure-okta-with-adobe-sso.html)

**How do I set up Users and Admins within Adobe Admin Console for Bizible?**

In order to login to Bizible using Adobe ID, a must be added to the 'Users' tab in a Bizible product profile. If a user is also listed as an Admin on the Bizible product profile, they will receive admin access in Bizible.
More information can be [seen here](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html).

**How can I direct my questions or concerns?**

Please reach out to your Account Executive or Success Manager for all other inquires and we will be happy to talk through any questions, concerns, or best practices.
