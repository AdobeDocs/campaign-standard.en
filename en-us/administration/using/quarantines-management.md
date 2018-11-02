---
title: Quarantines management
seo-title: Quarantines management
description: Quarantines management
seo-description: Learn how to optimize your deliverability with quarantine management.
page-status-flag: never-activated
uuid: 67e14663-499f-44e3-b46a-030d303a5652
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/administration/using/quarantines-management
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2017-11-28T11 04 03.869-0500
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
cq-template: /apps/help/templates/article-3
discoiquuid: 1e66d4f2-7677-4e98-a78d-842f97073315
firstPublishExternalDate: 2017-11-16T11:10:04.800-0500
herogradient: light
isreadyforlocalization: false
jcr-created: 2017-11-29T19 03 08.490-0500
jcr-createdby: admin
jcr-description: Quarantines management
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2017-11-16T11:10:04.800-0500
lochandoffdate: 2017-11-28T11 04 03.867-0500
lr-lastreplicatedby: wmyersta@adobe.com
navTitle: Quarantines management
publishexternaldate: 2017-11-16T11 10 04.800-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/administration/using/quarantines-management.html
sha1: 858328be11ae29025cd855aefb0b1b28173e28c0
topicBrowsingSortDate: 2017-11-16T11:10:04.800-0500
index: y
internal: n
snippet: y
---

# Quarantines management

Quarantines management

## About quarantines

Failed deliveries can result in email addresses being placed in quarantine. The recipients whose email address is in quarantine are automatically excluded during message preparation in order to speed up deliveries (the error rate has a significant effect on delivery speed) and avoid blacklisting by internet access providers.

>[!NOTE]
>
>Certain internet access providers automatically consider emails to be spam if the rate of invalid addresses is too high.

An email address can be quarantined, for example, when the mailbox is full or if the address does not exist. In any case, the quarantine procedure complies with specific rules described below.

Quarantine applies only to an email address, not the recipient himself. It means that, if two recipients have the same email address, they will both be affected if the address is quarantined.

Likewise, a recipient whose email address is quarantined could update his profile and enter a new address, and could then be targeted by delivery actions again.

Blacklisting, on the other hand, will result in the recipient concerned no longer being targeted by any delivery, e.g. after an unsubscription.

Administrators can see the list of addresses in quarantine from the **Administration > Channels > Quarantines > Addresses** menu.

![](assets/quarantines1.png)

Each email address has an error counter that is incremented when the sending of a message fails. In a default configuration, an address is quarantined after one "hard" or five consecutive "soft" errors at least 24 hours apart.

* A "hard" error indicates an invalid address ("User unknown", for instance). 
* A "soft" error can be temporary (such as a full inbox).

  Refer to the "Fail types" sections ( [List of delivery failure types](../../administration/using/quarantines-management.md#list-of-delivery-failure-types)) and [Error management](../../administration/using/quarantines-management.md#error-management) for more information on error types.

>[!NOTE]
>
>The increase in number of quarantines is a normal effect, related to the "wear and tear" of the database. For example, if the lifetime of an email address is considered to be three years and the recipients table increases by 50% each year, the increase in quarantines can be calculated as follows: End of Year 1: (1&#42;0.33)/(1+0.5)=22%. End of Year 2: ((1.22&#42;0.33)+0.33)/(1.5+0.75)=32.5%.

## Error management

The application manages erroneous addresses according to the type of error.

1. When a **Hard** error occurs, the corresponding email address is immediately placed in quarantine. 
1. **Ignored** errors do not send an address to quarantine.
1. **Soft** errors therefore do not cause immediate placement in quarantine, but they increment an error counter. When the error counter reaches the limit threshold, the address goes into quarantine. In the default configuration, the threshold is set at five errors, where two errors are significant if they occur at least 24 hours apart. The address is placed in quarantine at the sixth error.

For **Soft** or **Ignored** synchronous errors, retries will be performed for the duration of validity of the delivery. The default configuration allows five retries at one-hour intervals, followed by one retry per day for four days. This configuration can be changed globally (by the Adobe technical administrator) or for each delivery action or delivery template.

* To modify the delivery limit at the level of a delivery, go to the advanced parameters of the delivery or delivery template and specify the desired duration in the corresponding field, as in the example below:

  ![](assets/quarantines3.png)

  >[!NOTE]
  >
  >The advanced delivery properties are presented in the [Email processing rules](../../administration/using/email-configuration.md) section.

* To modify the delivery limit for the entire platform, contact the Adobe technical administrator.

### Synchronous and asynchronous errors

A delivery can fail at either of two moments. Errors can thus be considered as synchronous or asynchronous:

1. Synchronous error: the remote mail server contacted by the Adobe Campaign delivery server returned an error message. Adobe Campaign qualifies each error in order to determine whether or not the email addresses concerned should be quarantined.

   When the delivery of an email fails, the Adobe Campaign delivery server receives an error message from the messaging server or the remote DNS server. The list of errors is made up of strings contained in the message returned by the remote server. Failure types and reasons are assigned to each error message. 

1. Asynchronous error: a bounce mail was resent later by the receiving server. This mail is loaded into a technical mailbox the application uses to label messages with an error. After an email sending failure, Adobe Campaign applies many rules to categorize the error message.

   The feedback loop operates like bounce emails. When a user qualifies an email as spam, you can configure email rules in Adobe Campaign to block all deliveries to this user. Messages sent to users who have qualified an email as spam are automatically redirected towards an email box specifically created for this purpose. The addresses of these users are blacklisted even though they did not click the unsubscription link. Addresses are blacklisted in the quarantine table and not the recipient table.

   >[!NOTE]
   >
   >The bounce mailbox as well as complaints are managed by the Adobe technical administrator.

   **Related topics**:

    * [List of delivery failure types](../../administration/using/quarantines-management.md#list-of-delivery-failure-types)
    * [List of delivery failure reasons](../../administration/using/quarantines-management.md#list-of-delivery-failure-reasons)
    * [Email processing rules](../../administration/using/quarantines-management.md#email-processing-rules)

### List of delivery failure types

Failures must be categorized for the return and quarantine mechanisms to function. There are three types of error, determining how the application behaves and manages an error:

* **Hard**: This involves an error message that explicitly states that the address is invalid, such as: "Unknown user".
* **Soft**: This might be a temporary error, or one that could not be categorized, such as: "Invalid domain" or "Mailbox full".
* **Ignored**: This is an error that is known to be temporary, such as "Out of office", or a technical error, e.g. if the sender type is "postmaster".

### List of delivery failure reasons

There are many possible reasons for **Failed** addresses. For example, in the list of quarantined addresses, the **Error reason** field indicates why the selected address was placed in quarantine.

![](assets/quarantines2.png)

* **User unknown** (Hard type): the address does not exist. There is no use sending deliveries to this address.
* **Unreachable** (Soft type): an error has occurred in the message delivery chain. Error in the message distribution chain (incident on SMTP relay, domain temporarily unreachable, etc.) The address in question may be removed from the list to make a new try.
* **Mailbox full** (Soft type): the recipient's mailbox contains too many messages. This address can be removed from the quarantine list to make another attempt. It is removed automatically after 30 days.

  In order for the address to be automatically removed from the list of quarantined addresses, the **Database cleanup** technical workflow must be started.

* **Refused** (Ignored type): the address was rejected following the application of a security rule (e.g. by an anti-spam program).
* **Undefined** (Soft type): the address is undergoing qualification pending increase of its error counter.

  This type of error occurs when a new error message is sent by the server: it can be an isolated error, but if it occurs again, the error counter increases, which will alert the technical teams. 

* **Error ignored**: the address is whitelisted and the message ignored.
* **Blacklisted address**: the address was blacklisted at the time of sending.
* **Account disabled**: the user uses a messaging service which is accessible from the web. When the Internet Access Provider (IAP) detects a lengthy period of inactivity, it can close the user's account. Deliveries to the user's address will then be impossible.
* **Not connected**: the recipient's mobile phone is switched off or not connected to the network when the message is sent.
* **Invalid domain**: the domain of the email address is incorrect or no longer exists.
* **Text too long**: the number of characters in the SMS message exceeds the limit. For more on this, see [SMS encoding, length and transliteration](../../administration/using/sms-configuration.md#sms-encoding--length-and-transliteration).
* **Character not supported by encoding**: the SMS message contains one or more characters that are not supported by the encoding. &For more on this, see [Table of characters - GSM Standard](../../administration/using/sms-configuration.md#table-of-characters---gsm-standard).

>[!NOTE]
>
>When a delivery is successful after a retry, the error counter of the address which was prior to that quarantined is reinitialized. The address status changes to **Valid** and it is deleted from the list of quarantines after two days by the **Database cleanup** workflow.

### Removing an address from quarantine

If you need to remove an address from quarantine, contact the Adobe technical administrator.

## About bounce mail qualification

Adobe Campaign allows you to manage email send failures via the bounce mails functionality. When an email cannot be delivered to a recipient, the remote mail server automatically sends an error message, known as a bounce mail, to a technical email inbox reserved for this use. Error messages are picked up by the Adobe Campaign platform and qualified by the inMail process to enrich the list of email management rules. To access these rules, click the **Adobe Campaign** logo, at the top left, then select **Administration** > **Channels** > **Email** > **Email processing rules** (refer to [Email processing rules](../../administration/using/quarantines-management.md#email-processing-rules)).

Bounces mails can have the following qualification statuses:

* **To qualify**: the bounce mail needs to be qualified. Qualification must be done by the Deliverability team to ensure that the platform deliverability functions correctly. As long as it is not qualified, the bounce mail is not used to complete the list of email processing rules.
* **Keep**: the bounce mail was qualified and will be used by the **Update for deliverability** workflow to be compared to existing email processing rules and enrich the list.
* **Ignore**: the bounce mail was qualified but will not be used by the **Update for deliverability** workflow. So it will not be sent to the client instances.

To view the statuses of the various bounce mails, click the **Adobe Campaign** logo, in the top left, then select **Administration > Channels > Quarantines > Message qualification**.

![](assets/qualification.png)

