---
title: Managing groups and users
seo-title: Managing groups and users
description: Managing groups and users
seo-description: Learn how to create security groups and manage users.
page-status-flag: never-activated
uuid: 7bb73033-3fb9-43a7-aa6d-4d176636544e
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: users-e-security
discoiquuid: a75b142d-54f3-40cd-8670-5c84fcf8fd1d
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# Managing groups and users{#managing-groups-and-users}

Managing groups and users

## About security groups {#about-security-groups}

Security groups are sets of users that share the same roles and rights within your organization.

Users must always be linked to a security group. This will allow you to assign them specific roles, organizational and geographical units.

For more information on roles, the tables in the following page present the different operations available according to a user's role(s): [Adobe Campaign Standard authorizations](https://docs.campaign.adobe.com/doc/standard/en/Technotes/AdobeCampaign-ACSRights.pdf).

If a user is not linked to any security group, he will not be able to access Adobe Campaign.

To restrict a user's access, do not add the user to the Campaign Standard users group as this is linked to **All** geographical and organizational units.

## Creating a security group and assigning users {#creating-a-security-group-and-assigning-users}

>[!NOTE]
>
>In the Admin console, security groups are referred as profiles and tenants as products.

You can create your own security groups if the out-of-the-box groups are not enough to manage your users. They can be managed by Administrators that have access to both Adobe Campaign administration menus and the Admin console. For more information on the Admin console, refer to this [documentation](https://helpx.adobe.com/enterprise/managing/user-guide.html).

Here, we first need to assign the two out-of-the-box groups Standard user and Administrator to our users. These security groups will restrict some functionalities of Adobe Campaign: the Standard User has basics access to Adobe Campaign whereas the Administrator can access the administration menus for example.

Note that any changes made to security groups on the admin console will be synchronized as soon as users log into Adobe Campaign.

Then, we want to create a set of security groups Europe and France that will restrict some products depending on the geographical units of our Standard user and Administrator.

![](assets/ootb_security_group_1.png)

You first need to assign one of the out-of-the-box security group to your users:

1. In the Admin console, select your tenant then the **Users** tab.

   ![](assets/manage_security_group_2.png)

1. Click the **Add user** button and enter your user's email address.
1. In the **Assign Products** tab, select your tenant then the Administrators out-of-the-box security group from the drop-down list. This will allow the user to have access to the administration menus and to create the next security groups.

   ![](assets/ootb_security_group_2.png)

1. Click **Save** and follow the same procedures to assign the Standard Users out-of-the-box security group to your new user.

   ![](assets/ootb_security_group_3.png)

Once your two users are attached to the Administrators and Standard users out-of-the-box security groups which assign roles to our users, the Administrator user can now create the two security groups France and Europe that will assign geographical units to our users in addition to the out-of-the-box security groups.

1. In the Admin console, select your tenant then the **Products** tab.
1. Click the **New Profile** button to create the Europe security group.

   ![](assets/create_security_1.png)

1. Type the **Profile name** by following this exact syntax: **Campaign Standard- tenantname - ID of the security group** and click **Done**.

   The ID chosen will then be used while creating the security group in Adobe Campaign.

   >[!NOTE]
   >
   >If the above syntax doesn't seem to work with an older instance, it needs to be replaced by **Campaign - tenantname - ID of the security group**.

   ![](assets/manage_security_group_1.png)

1. Then, follow the same procedures to create the France security group.
1. Assign your security group to your user by selecting the **Users** tab.

   ![](assets/manage_security_group_2.png)

1. Click your previously created user then the  ![](assets/managing_security_group_10.png) icon in the **Products** category.

   Select **Edit products assigned directly** to start assigning new security group to your user.

   ![](assets/manage_security_group_8.png)

1. In the **Assign Products** tab, select your tenant then your previously created security groups Europe from the drop-down list.

   Click **Save**.

   ![](assets/manage_security_group_3.png)

   If a user is in several groups:

    * The roles of the different groups are cumulated. Here, users are in two different groups: one that will act on roles the other on units.
    * It is the unit that is the highest in the hierarchy that will be used (see example in the [Organizational and geographical units](../../administration/using/organizational-and-geographical-units.md) section).
    * The user will no longer be able to connect if units have the same equivalent level and are in parallel branches in the hierarchy (such as Canada and the US).

1. Follow the same procedures to assign the France security group to your Standard user.

   ![](assets/manage_security_group_9.png)

The newly created security groups are now created in the Admin console. For them to be completely synced, you also need to create them in Adobe Campaign.

The Administrator user has to create the set of security groups that are used to assign geographical units: Europe and France. To learn how to create geographical or organizational units, see [Creating and managing units](../../administration/using/organizational-and-geographical-units.md#creating-and-managing-units) .

1. Click the **Adobe Campaign** logo, in the top left corner, then select **Administration > Users & Security > Security groups**.
1. Create your new security group and specify its **Label** and **ID**.

   The ID needs to be the same as the one chosen in the Admin console.

1. In the **User access** field, assign organizational and geographical units. Here, the Europe security group is assigned the All and Europe units.

   ![](assets/manage_security_group_6.png)

1. You can also assign roles to your security group. In our case, this step is not needed since the out-of-the-box security groups Administrators and Standard users are used to assign roles.
1. Follow the same procedures to create the last security France and assign the France geographical unit.

   ![](assets/manage_security_group_7.png)

Your users are now assigned to a security group and can connect to Adobe Campaign.

>[!CAUTION]
>
>If users are removed from a security group in the admin console, they will remain part of the Adobe Campaign security group and will no longer be able to log in Adobe Campaign. In this case, remove the users' email addresses in the admin console to prevent them from receiving sensitive information.

