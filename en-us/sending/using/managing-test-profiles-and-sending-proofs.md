---
title: Managing test profiles and sending proofs
seo-title: Managing test profiles and sending proofs
description: Managing test profiles and sending proofs
seo-description: Learn how to manage test profiles and proofs.
uuid: ad483de2-b9e2-46ae-8cf0-1d6b22a74627
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/managing-test-profiles-and-sending-proofs
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 53 47.852-0400
cq-lastreplicated: 2018-07-23T06 02 17.544-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
cq-template: /apps/help/templates/article-3
discoiquuid: e29ee5dd-4b5a-4e34-b575-ccf14ced9816
firstPublishExternalDate: 2018-07-23T06:02:17.439-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 29.708-0400
jcr-createdby: admin
jcr-description: Managing test profiles and sending proofs
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:17.439-0400
lochandoffdate: 2018-07-30T04 53 47.852-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Managing test profiles and sending proofs
publishexternaldate: 2018-07-23T06 02 17.439-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/managing-test-profiles-and-sending-proofs.html
sha1: 94512963c92f768a1c72ba021738292c0c4f5a30
topicBrowsingSortDate: 2018-07-23T06:02:17.439-0400
index: y
internal: n
snippet: y
---

# Managing test profiles and sending proofs

Managing test profiles and sending proofs

## <p>About test profiles</p>

The test profiles allow you to target additional recipients who do not match the defined targeting criteria. They are added to a message's audience to detect any fraudulent use of your recipient database or to ensure the emails arrive in the inboxes.

You can manage your test profiles from the advanced menu **Profiles & audiences > Test profiles**.

A test profile contains fictitious contact information, or contact information controlled by the sender, that can then be used in a message in the following contexts:

* For sending **Proofs**: the Proof is a specific message used to check the message before sending the finalized delivery to recipients. A Proof test profile is in charge of checking the delivery, with regard to its content and format. See [Sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs).
* For **Email rendering**: the Email rendering test profile is used to check the way in which a message is displayed according to the message inbox that receives it. For example, webmail, message service, mobile, etc. See [Email rendering](../../sending/using/email-rendering.md).

  The **Email rendering** use is read-only. Test profiles with this use are only available out-of-the-box in Adobe Campaign.

* As a **Trap**: the message is sent to the test profile just as it is sent to the main target, as a means to identify whether your client file is being used fraudulently.
* To **Preview** messages: a test profile can be selected when previewing a message to test the personalization elements.

![](assets/test_profile.png)

## <p>Managing test profiles</p>

### <p>Creating test profiles</p>

1. From the advanced menu, via the Adobe Campaign logo, select **Profiles & audiences > Test profiles** to access the list of test profiles. 

   ![](assets/test_profile_creation_1.png)

1. From the **Test profiles** dashboard, click **Create**.

   ![](assets/test_profile_creation_2.png)

1. Enter the data for this profile.

   ![](assets/test_profile_creation_3.png)

1. Select the use you intend for your test profile.

   ![](assets/test_profile_creation_4.png)

1. Enter the contact channels **Email, Telephone, Mobile, Mobile app**, as well as the test profile address if necessary.

   >[!NOTE]
   >
   >You can define a preferred email format: **Text** or **HTML**.

1. Specify an event type and the data for this event if you want to use this test profile for testing the personalization of a transactional message.
1. Click **Create** to save the test profile.

The test profile will then be added to the list of profiles.

**Related topic:**

[Creating a test profile](https://docs.campaign.adobe.com/doc/standard/en/Videos/test_profile_creation.mp4) video

### <p>Editing test profiles</p>

To edit a test profile and consult the data that is linked to it, or to modify it:

1. Select the test profile you would like to edit by clicking on its image.
1. Consult or modify the fields.

   ![](assets/test_profile_edit.png)

1. Click **Save** if you have entered your changes, or select the name of the test profile then **Test profiles** in the section at the top of the screen to go back to the test profiles dashboard.

## <p>Sending proofs</p>

A proof is a specific message that allows you to test a message before sending it to the main target.

Recipients of the proof are in charge of approving the message (its content and form). They are defined in the **Test profiles**. For more on this, see [Managing test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md#managing-test-profiles).

In order to send a proof, the test profiles must be included in your message's audience.

In a message:

1. Click the **Send a test** button.

   ![](assets/bat_select.png)

1. Select the type of proof you would like to use:

    * **Email rendering**: select this option to test the way your message is received according to the inboxes targeted. For more information, refer to [Email rendering](../../sending/using/email-rendering.md).
    * **Proof**: select this option to test the message before sending it to the main target. The proof recipients are in charge of approving the delivery, by checking both its content and its format.
    * **Proof + Email rendering**: this option combines the two previous options.

   ![](assets/bat_select1.png)

1. Confirm your choice.

   The proofs are sent to the test profiles.

   ![](assets/bat_select2.png)

1. You can view your proofs using the **Proofs** drop-down list.

   ![](assets/bat_view.png)

1. Select a proof to access its summary. For an email, if you have selected the **Email rendering** option as the proof type, the **Access email rendering** icon is displayed on the right of the proof label. See [Email rendering](../../sending/using/email-rendering.md).

   ![](assets/bat_view2.png)

Depending on the comments from the people who receive the proof, you may be asked to modify the delivery's content. Once the modifications have been carried out, you have to restart email preparation then re-send a proof. Each new proof can be accessed using the **Show proofs** button.

You have to send as many proofs as necessary until you have finalized the content of your delivery. Once this is done, you can send the delivery to the main target and close the approval cycle.

**Related topic:**

[Sending a test, preparing and sending an email](https://docs.campaign.adobe.com/doc/standard/en/Videos/test_preparing_sending_email.mp4) video
