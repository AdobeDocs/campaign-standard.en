---
title: Configuring email channel
seo-title: Configuring email channel
description: Configuring email channel
seo-description: Learn how to configure the email channel.
uuid: 8cdec653-3436-4f93-8dd6-4118b0621a59
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/administration/using/configuring-email-channel
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 21.625-0400
cq-lastreplicated: 2018-07-23T05 53 33.903-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
cq-template: /apps/help/templates/article-3
discoiquuid: 18f3c034-ac81-42d7-a9cb-dbb82954d445
firstPublishExternalDate: 2018-07-23T05:53:33.788-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-02-16T08 03 38.506-0500
jcr-createdby: admin
jcr-description: Configuring email channel
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:53:33.788-0400
lochandoffdate: 2018-07-25T09 29 21.624-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Configuring email channel
publishexternaldate: 2018-07-23T05 53 33.788-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/administration/using/configuring-email-channel.html
sha1: 13feee24e1241d50f04383d0e1a548ed29725c11
topicBrowsingSortDate: 2018-07-23T05:53:33.788-0400
index: y
internal: n
snippet: y
---

# Configuring email channel

Configuring email channel

## Configuring the email channel

### List of email channel parameters

The email configuration screen allows you to define the parameters for the email messaging channel.

![](assets/channels_1.png)

**Header parameters of sent emails**

In this section, you can specify the **masks** authorized for the sender address and the error address. If necessary, these masks can be separated using commas. This configuration is optional. When these fields are entered, during the message preparation stage, Adobe Campaign checks that the addresses entered are valid. This operating mode ensures that no addresses are used that could trigger deliverability issues. Delivery addresses must be configured on the delivery server.

**Deliverability**

This ID is provided by support. It is necessary for deliverability reports to work correctly.

**Delivery parameters**

The following options are available:

* **Message delivery duration**: Adobe Campaign sends the messages beginning on the start date. This field allows you to specify the duration during which the messages can be sent.
* **Online resources validity duration**: this field is used for uploaded resources, mainly for the mirror page and images. The resources on this page are valid for a limited time (to save disk space).

**Retries**

Temporarily undelivered messages are subject to an automatic retry. See [Retries after a delivery failure](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-failure). This section indicates how many retries should be performed the day after the send is started (**Number of retries**) and the minimum delay between retries (**Retry period**).

By default, five retries are scheduled for the first day with a minimum interval of one hour, spread out over the 24 hours of the day. One retry per day is programmed after that and until the delivery deadline, which is defined in the **Delivery parameters** section.

**Email quarantine parameters**

Configuration options for quarantines are as follows:

* **Time between two significant errors**: enter a value ("1d" by default: 1 day) to define the time the application waits before incrementing the error counter in case of failure.
* **Maximum number of errors before quarantine**: when this value is reached, the email address is then quarantined (by default "5": the address will be quarantined on the sixth error). This means that the contact will be automatically excluded from subsequent deliveries.

**Related topic**:

[Understanding quarantine management](../../sending/using/understanding-quarantine-management.md)

### Email routing accounts

The **Integrated email routing** external account is provided by default. It contains the technical parameters that allow the application to send emails.

External account configuration should be done by expert users only.

![](assets/channels_2.png)

The account type must always be set to **Routing**, the channel to **Email** and the delivery mode set to **Bulk delivery**.

**Related topic**:

[External accounts](../../administration/using/external-accounts.md)

### Email processing rules

These rules contain the list of character strings which can be returned by remote servers and which let you qualify the error (**Hard**, **Soft** or **Ignored**).

The default rules are as follows:

**Bounce mails**

When an email fails, the remote message server returns a bounce error message to the address specified in the application settings. Adobe Campaign compares the content of each bounce mail to the strings in the list of rules, and then assigns it one of the three error types.

The user can create his own rules.

>[!CAUTION]
>
>When importing a package and when updating data via the **Update for deliverability** workflow, the user-created rules are overwritten.

**Managing email domains**

The domain management rules are used to regulate the flow of outgoing emails for a specific domain. They sample the bounce messages and block sending where appropriate. The Adobe Campaign messaging server applies rules specific to the domains, and then the rules for the general case represented by an asterisk in the list of rules. Rules for the Hotmail and MSN domains are available by default in Adobe Campaign.

To configure domain management rules, simply set a threshold and select certain SMTP parameters. A **threshold** is a limit calculated as an error percentage beyond which all messages towards a specific domain are blocked.

For example, in the general case, for a minimum of 300 messages, the sending of emails is blocked for three hours if the error rate reaches 90%.

The **SMTP parameters** act as filters applied for a blocking rule.

* You can choose whether or not to activate certain identification standards and encryption keys to check the domain name, such as **Sender ID**, **DomainKeys**, **DKIM**, and **S/MIME**.
* **SMTP relay**: lets you configure the IP address and the port of a relay server for a particular domain.

**MX Management**

Each rule defines an address mask for the MX. Any MX whose name matches this mask is therefore eligible. The mask can contain "&#42;" and "?" generic characters.

For example, the following addresses:

* a.mx.yahoo.com 
* b.mx.yahoo.com 
* c.mx.yahoo.com

are compatible with the following masks:

* &#42;.yahoo.com
* ?.mx.yahoo.com

These rules are applied in sequence: the first rule whose MX mask is compatible with the targeted MX is applied.

The following parameters are available for each rule:

* **Range of IDs**: this option lets you indicate the ranges of identifiers (publicId) for which the rule applies. You can specify:

    * A number: the rule will only apply to this publicId.
    * A range of numbers (number1-number2): the rule will apply to all publicIds between these two numbers.

  If the field is empty, the rule applies to all IDs.

* **Shared**: this option indicates that the highest number of messages per hour and of connections applies to all MXs linked to this rule. 
* **Maximum number of connections**: maximum number of simultaneous connections to an MX from a given address. 
* **Maximum number of messages**: maximum number of messages that can be sent by one connection. After this amount, the connection is closed and a new one is reopened. 
* **Messages per hour**: maximum number of messages that can be sent in one hour for an MX via a given address.

>[!CAUTION]
>
>* The delivery server (MTA) must be restarted if the parameters have been changed. 
>* The modification or creation of management rules is for expert users only. 
>

## List of email properties

This section details the list of parameters available in the properties screen of an email or email template. Managing templates is detailed in the [Managing templates](../../start/using/about-templates.md) section.

>[!NOTE]
>
>Certain parameters are only available in templates. The parameters available vary according to the rights you have as a user.

To edit the properties of an email or an email template, use the **Edit properties** button.

![](assets/delivery_options_1.png)

### List of email general parameters

The general parameters are:

![](assets/delivery_options_2.png)

Identify the email using the **Label** and **ID** fields. This information appears in the interface but is not visible to the message recipients.

>[!CAUTION]
>
>The ID must be unique.

The **Brand** field allows you to select the brand linked to the delivery. For more information on using and configuring brands, refer to the [Branding](../../administration/using/branding.md) section.

The **Campaign** field allows you to enter the campaign linked to the email.

You can also add a **Description** in the corresponding field and edit the image displayed on the email thumbnail in the lists.

### List of email sending parameters

The **Send** section contains the following parameters:

#### Retries parameters

Temporarily undelivered messages are subject to an automatic retry. See [Retries after a delivery failure](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-failure). This section indicates how many retries should be performed the day after the send is started (**Max. number of retries**) and the minimum delay between retries (**Retry period**).

By default, five retries are scheduled for the first day with a minimum interval of one hour, spread out over the 24 hours of the day. One retry per day is programmed after that and until the delivery deadline, which is defined in the [List of email validity period parameters](../../administration/using/configuring-email-channel.md#list-of-email-validity-period-parameters) section.

The **Test SMTP delivery** option allows you to test sending messages via SMTP. The messages are processed up until connection with the SMTP server is achieved, but they are not sent. For more information on configuring SMTP, refer to the [List of email SMTP parameters](../../administration/using/configuring-email-channel.md#list-of-email-smtp-parameters) section.

#### Email format parameters

You can configure the format of emails to be sent. There are three options available:

* **Use recipient preferences** (default mode): the message format is defined according to the data stored in the recipient profile and stored by default in the **Email format** field (@emailFormat). If a recipient wishes to receive messages in a certain format, this is the format sent. If the field is not completed, a multipart-alternative message is sent (see below).
* **Let recipient mail client choose the most appropriate format (multipart-alternative)**: the message contains both formats: text and HTML. The format displayed upon reception depends on the configuration of the recipient's mail software (multipart-alternative).

  >[!CAUTION]
  >
  >This option includes both versions of the message. It therefore impacts the delivery throughput, because the message size is greater.

* **Send all messages in text format**: the message is sent in text format. HTML format will not be sent, but used for the mirror page only when the recipient clicks the link in the message.

### List of email validity period parameters

The **Validity** section contains the following parameters:

* **Explicitly set validity dates**: when this box is unchecked, you must enter a duration in the **Delivery duration** and **Resource validity limit** fields. Check this box if you would like to define specific times and dates.
* **Delivery duration**: Adobe Campaign sends the messages beginning on the start date. This field allows you to specify the duration during which the messages can be sent.
* **Resource validity duration**: this field is used for uploaded resources, mainly for the mirror page and images. The resources on this page are valid for a limited time (to save disk space).
* **Mirror page management**: the mirror page is an HTML page accessible online via a web browser. Its content is identical to the email content. By default, the mirror page is generated if the link is inserted in the mail content. This field allows you to modify the way in which this page is generated:

  >[!CAUTION]
  >
  >An HTML content must have been defined for the email for the mirror page to be created.

    * **Generate the mirror page if a mirror link appears in the email content** (default mode): the mirror page is generated if the link is inserted in the mail content. 
    * **Force the generation of the mirror page**: even if no link to the mirror page is inserted into the messages, the mirror page will be created. 
    * **Do not generate the mirror page**: no mirror page is generated, even if the link is in the messages. 
    * **Generate a mirror page accessible using only the message ID**: this option lets you access the content of the mirror page, with personalization information, in the delivery log window.

### List of email tracking parameters

The **Tracking** section contains the following parameters:

* **Activate tracking**: allows you to activate/deactivate message URL tracking. To manage tracking for each message URL, use the **Links** or **Tracked URLs** button in the content editor action bar. See [About tracked URLs](../../designing/using/about-tracked-urls.md).
* **Tracking validity limit**: allows you to define the duration for which the tracking will be activated on the URLs.
* **Substitution URL for expired URLs**: you can enter a URL to a web page that will be displayed once the tracking has expired.

### List of email advanced parameters

The **Advanced parameters** section contains multiple parameters.

The first two fields allow you to enter information necessary to elaborate email message headers (reply address and reply address text). This information can be personalized. To do this, click the button to the right of the field that is going to be changed, then add the personalization fields. Inserting and using the personalization fields is detailed in the [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md) section.

#### Target context

The targeting context allows you to define a set of tables that will be used for email targeting (in the audience definition screen) and personalization (defining personalization fields in the HTML content editor).

#### Routing

This field indicates the routing mode used. It references an external account. For example, this can be used if you would like to use an external account containing specific branding configurations.

>[!NOTE]
>
>External accounts are accessible via the **Administration** > **Application settings** > **External accounts** menu.

#### Preparation

Preparing messages is detailed in the [Approving messages](../../sending/using/preparing-the-send.md) section.

* **Typology**: before any send, messages must be prepared in order to validate the content and configuration. The verification rules applied during the preparation phase are defined in a **typology**. For example, for emails, preparation involves checking the subject, URLs and images, etc. Select the typology to apply in this field.

  >[!NOTE]
  >
  >Typologies, which can be accessed via the **Administration** > **Channels** > **Typologies** menu, are presented in the [Typologies](../../administration/using/about-typology-rules.md) section.

* **Compute the label during delivery analysis**: allows you to calculate the label value of the email during the message preparation phase. 
* **Save SQL queries in the log**: this option allows you to add SQL query logs in the journal during the preparation phase.

### List of email SMTP parameters

The **SMTP** section contains the following parameters:

* **Character encoding**: check the **Force encoding** box if you would like to force message encoding, then select the encoding you want to use.
* **Bounce mails**: by default, bounce mails are received in the platform's error inbox (defined in the **Administration** > **Channels** > **Email** > **Configuration** screen). To define a specific error address for an email, enter the address in the **Error address** field.
* **Additional SMTP headers**: this option allows for additional SMTP headers to be added to your messages. The script entered in the **Headers** field must reference one header per line, in the form of **name:value**. Values are encoded automatically if necessary.

  >[!CAUTION]
  >
  >Adding a script for inserting additional SMTP headers is reserved for advanced users. The syntax of this script must comply with the requirements of this content type: no unused space, no empty line, etc.

### List of access authorization parameters

The **Access authorization** section contains the following parameters:

* The **Organizational unit** and **Geographical unit** fields allow you to restrict access to this email to certain users. The users associated with the specified unit or parent units will have read and write access to this email. Users associated with child units will only have read access to this email.

  >[!NOTE]
  >
  >You can configure organizational and geographical units via the **Administration** > **Users & Security** menu.

* The **Created by**, **Created**, **Modified by** and **Last modified** fields are automatically completed.

## Email BCC

Emails sent by Adobe Campaign can be stored on an external system through BCC. When activated in the delivery template, this feature allows you to send an exact copy of the corresponding sent messages to a BCC email address.

This action is most of the time performed for legal reasons. It has to be managed by the customer. Adobe Campaign does not manage stored messages: they are sent to a dedicated address from where they can be processed and archived on an external system.

>[!NOTE]
>
>This feature is optional. Please check your license agreement and contact your account executive to activate it.

Note that you can only use one BCC email address.

Only successfully sent emails are taken in account. Bounces are not.

>[!CAUTION]
>
>For privacy reasons, BCC emails must be processed by an archiving system capable of storing securely personally identifiable information (PII).

Email BCC is activated in the [email template](../../start/using/about-templates.md), through a dedicated option:

1. Go to **Resources** > **Templates** > **Delivery templates**.
1. Duplicate the out-of-the-box **Send via email** template.
1. Select the duplicated template.
1. Click the **Edit properties** button to edit the template's properties.
1. Expand the **Send** section.
1. Check the **Archive emails** box to keep a copy of all sent messages for each delivery based on this template.

   ![](assets/email_archiving.png)

If the emails sent to the BCC address are opened and clicked through, it will be taken into account in the **Total opens** and **Clicks** from the send analysis which could cause some miscalculations.

>[!NOTE]
>
>When creating a new delivery template, Email BCC is not enabled by default, even if the option has been purchased. You must enable it manually in each delivery template where you want to use it.

