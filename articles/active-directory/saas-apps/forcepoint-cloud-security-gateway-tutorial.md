---
title: 'Tutorial: Azure AD SSO integration with Forcepoint Cloud Security Gateway - User Authentication'
description: Learn how to configure single sign-on between Azure Active Directory and Forcepoint Cloud Security Gateway - User Authentication.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: CelesteDG
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 05/26/2022
ms.author: jeedes

---

# Tutorial: Azure AD SSO integration with Forcepoint Cloud Security Gateway - User Authentication

In this tutorial, you'll learn how to integrate Forcepoint Cloud Security Gateway - User Authentication with Azure Active Directory (Azure AD). When you integrate Forcepoint Cloud Security Gateway - User Authentication with Azure AD, you can:

* Control in Azure AD who has access to Forcepoint Cloud Security Gateway - User Authentication.
* Enable your users to be automatically signed-in to Forcepoint Cloud Security Gateway - User Authentication with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Forcepoint Cloud Security Gateway - User Authentication single sign-on (SSO) enabled subscription.
* Along with Cloud Application Administrator, Application Administrator can also add or manage applications in Azure AD.
For more information, see [Azure built-in roles](../roles/permissions-reference.md).

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment.

* Forcepoint Cloud Security Gateway - User Authentication supports **SP** initiated SSO.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Add Forcepoint Cloud Security Gateway - User Authentication from the gallery

To configure the integration of Forcepoint Cloud Security Gateway - User Authentication into Azure AD, you need to add Forcepoint Cloud Security Gateway - User Authentication from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **Forcepoint Cloud Security Gateway - User Authentication** in the search box.
1. Select **Forcepoint Cloud Security Gateway - User Authentication** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

## Configure and test Azure AD SSO for Forcepoint Cloud Security Gateway - User Authentication

Configure and test Azure AD SSO with Forcepoint Cloud Security Gateway - User Authentication using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in Forcepoint Cloud Security Gateway - User Authentication.

To configure and test Azure AD SSO with Forcepoint Cloud Security Gateway - User Authentication, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure Forcepoint Cloud Security Gateway - User Authentication SSO](#configure-forcepoint-cloud-security-gateway---user-authentication-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Forcepoint Cloud Security Gateway - User Authentication test user](#create-forcepoint-cloud-security-gateway---user-authentication-test-user)** - to have a counterpart of B.Simon in Forcepoint Cloud Security Gateway - User Authentication that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **Forcepoint Cloud Security Gateway - User Authentication** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

    ![Screenshot shows to edit Basic S A M L Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Identifier** text box, type the URL:
    `https://mailcontrol.com/sp_metadata.xml`

    b. In the **Reply URL** text box, type the URL:
    `https://proxy-login.blackspider.com/`

    c. In the **Sign-on URL** text box, type the URL:
    `https://mailcontrol.com`

1. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, click **Download** to download the **Federation Metadata XML** from the given options as per your requirement and save it on your computer.

    ![Screenshot shows the Certificate download link.](common/metadataxml.png "Certificate")

1. On the **Set up Forcepoint Cloud Security Gateway - User Authentication** section, copy the appropriate URL(s) based on your requirement.

   ![Screenshot shows to copy appropriate configuration U R L.](common/copy-configuration-urls.png "Authentication")

### Create an Azure AD test user

In this section, you'll create a test user in the Azure portal called B.Simon.

1. From the left pane in the Azure portal, select **Azure Active Directory**, select **Users**, and then select **All users**.
1. Select **New user** at the top of the screen.
1. In the **User** properties, follow these steps:
   1. In the **Name** field, enter `B.Simon`.  
   1. In the **User name** field, enter the username@companydomain.extension. For example, `B.Simon@contoso.com`.
   1. Select the **Show password** check box, and then write down the value that's displayed in the **Password** box.
   1. Click **Create**.

### Assign the Azure AD test user

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to Forcepoint Cloud Security Gateway - User Authentication.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **Forcepoint Cloud Security Gateway - User Authentication**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you are expecting a role to be assigned to the users, you can select it from the **Select a role** dropdown. If no role has been set up for this app, you see "Default Access" role selected.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure Forcepoint Cloud Security Gateway - User Authentication SSO

1. Log in to your Forcepoint Cloud Security Gateway - User Authentication company site as an administrator.

1. Go to **Web** > **SETTINGS** and click **Single Sign-On**.

1. In the **Single Sign-On** page, perform the following steps:
    
    ![Screenshot that shows the Single Sign-On Configuration.](./media/forcepoint-cloud-security-gateway-tutorial/general.png "Configuration")

    a. Enable **Use identity provider for single sign-on** checkbox.

    b. Select **Identity provider** from the dropdown.

    c. Upload the **Federation Metadata XML** file from the Azure portal into the **File upload** textbox by clicking **Browse** option.

    d. Click **Save**.

### Create Forcepoint Cloud Security Gateway - User Authentication test user

In this section, you create a user called Britta Simon in Forcepoint Cloud Security Gateway - User Authentication. Work with [Forcepoint Cloud Security Gateway - User Authentication support team](mailto:support@forcepoint.com) to add the users in the Forcepoint Cloud Security Gateway - User Authentication platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

* Click on **Test this application** in Azure portal. This will redirect to Forcepoint Cloud Security Gateway - User Authentication Sign-on URL where you can initiate the login flow. 

* Go to Forcepoint Cloud Security Gateway - User Authentication Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you click the Forcepoint Cloud Security Gateway - User Authentication tile in the My Apps, this will redirect to Forcepoint Cloud Security Gateway - User Authentication Sign-on URL. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Next steps

Once you configure Forcepoint Cloud Security Gateway - User Authentication you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).