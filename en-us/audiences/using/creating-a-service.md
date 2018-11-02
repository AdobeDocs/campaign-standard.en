---
title: Creating a service
seo-title: Creating a service
description: Creating a service
seo-description: Learn how to create your first service and configure it to send email confirmations to your subscribers.
uuid: 27bd5e54-8a96-47de-a3e4-f315e529b51f
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/audiences/using/creating-a-service
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 18.144-0400
cq-lastreplicated: 2018-07-23T05 55 28.958-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-subscriptions
cq-template: /apps/help/templates/article-3
discoiquuid: 9bb952eb-13be-4f90-8807-ea1604038cd8
firstPublishExternalDate: 2018-07-23T05:55:28.895-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 20.536-0400
jcr-createdby: admin
jcr-description: Creating a service
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:55:28.895-0400
lochandoffdate: 2018-07-25T09 29 18.144-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Creating a service
publishexternaldate: 2018-07-23T05 55 28.895-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/audiences/using/creating-a-service.html
sha1: 3dd54bf6adfdf1862160b98335b7c6e3642b0828
topicBrowsingSortDate: 2018-07-23T05:55:28.895-0400
index: y
internal: n
snippet: y
---

# Creating a service

Creating a service

In order to be able to manage subscriptions, you first need to create a service and configure it. Configuring a new service allows you to specify the email confirmations that the profiles will receive when they subscribe to or unsubscribe from the service. You will also define the subscription and unsubscription landing pages linked to the service. For example, a service subscription link inserted into an email will automatically direct the profile to the subscription landing page that is specified in the service.

To configure a service:

1. From the advanced menu **Profiles & audiences** > **Services** via the Adobe Campaign logo, add a new service or select an existing service. If you create a new service, simply follow the steps shown on the screen.

   A default service template is available. This template is pre-configured with default landing pages and confirmation emails. You can create other templates to define specific configurations. For more on this, refer to the [Managing templates](../../start/using/about-templates.md) section.

1. In the **Service properties** section, accessed via the  ![](assets/edit_darkgrey-24px.png)

   button in the service dashboard, configure the confirmation messages for subscriptions and unsubscriptions.

   ![](assets/lp_service_parameters.png)

1. Select a confirmation message template for subscriptions and unsubscriptions. Three modes are available:

    * **No message**: this mode allows you to create a service without a confirmation message.
    * **Default message**: this mode will use the default subscription or unsubscription confirmation transactional message. The default confirmation messages are generic and will be the same for all services that use the default mode.
    * **Custom message**: this mode allows you to handle custom confirmation messages, specific for each service. You then select the **Custom subscription event configuration** which is associated with a specific transactional message template. Refer to [Transactional messages](../../channels/using/about-transactional-messaging.md) for more information on transactional event and message configuration.

1. Save the service. It is now ready to be used.

Once a service has been created, you can start promoting it.

**Related topics:**

* [Managing a service and subscriptions](https://docs.campaign.adobe.com/doc/standard/en/Videos/service_creation.mp4) video
* [Promoting a service](../../audiences/using/promoting-a-service.md)
* [Creating an audience made of subscribers](../../audiences/using/creating-audiences.md#creating-list-audiences)
* [Linking a form to a service in a landing page](../../channels/using/designing-a-landing-page.md#linking-a-form-to-a-service)

