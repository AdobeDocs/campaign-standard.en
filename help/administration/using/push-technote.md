---
title: Push Notification Channel upcoming changes
description: Push Notification Channel upcoming changes
audience: channels
feature: Push
role: Admin
level: Experienced
hide: yes
hidefromtoc: yes
exl-id: e273b443-7c43-482b-8f86-60ada4b57cbf
---
# Push Notification Channel upcoming changes {#push-upgrade}

You can use Campaign to send push notifications on Android and iOS devices. To perform this, Campaign relies on specific subscription services. Some important changes to the Android Firebase Cloud Messaging (FCM) service will be released in 2024, and will impact your Adobe Campaign implementation. In addition, for iOS apps, Adobe is changing the way to allow Administrators to configure certificates.

## What changed? {#push-changes}

### Android {#push-android}

As part of Google's continual effort to improve its services, the legacy FCM APIs will be discontinued on **June 20, 2024**. Learn more about Firebase Cloud Messaging HTTP protocol in [Google Firebase documentation](https://firebase.google.com/docs/cloud-messaging/http-server-ref){target="_blank"}.

Currently Adobe Campaign Standard is using HTTP legacy APIs to send Android Push Notification Messages and will be making changes in the upcoming months to upgrade to the HTTP v1 APIs. 

### iOS {#push-ios}

Adobe will also be upgrading Adobe Campaign Standard for the iOS Push Notification Channel and changing the way we allow Administrators to configure certificates for their iOS applications. Administrators will now need to upload the iOS certificates through the Adobe Campaign Standard's user interface.   

## Are you impacted? {#push-impact}

As a Campaign Standard user, if you are sending push notification messages to your audiences, you are impacted.

## How to migrate? {#push-migration}

These updates require a Campaign Standard build upgrade, as they impact the mobile channel configuration and permission management.

Detailed instructions will be provided soon to facilitate a smooth transition process. 

Our Customer Support Team will be available to assist you throughout this transition. We may also host webinars and enablement sessions to cover the technical aspects and best practices for the transition. 

In the meantime, recommendation is to take this time to review your current configuration and customization in Adobe Campaign Standard so you are prepared to make any necessary changes, if required. 

If you have any immediate concerns or questions, please don't hesitate to reach out to our support team.
