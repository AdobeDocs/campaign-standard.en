---
title: CNIL guidance on email tracking pixels
description: Learn about CNIL's updated guidance on email tracking pixels and the Adobe Campaign Standard controls that can support your compliance efforts.
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
hide: true
---

# Understanding CNIL's updated guidance on email tracking pixels {#cnil-pixel-tracking}

>[!BEGINSHADEBOX]

**On this page:** Learn about CNIL's April 2026 recommendation on email tracking pixels and discover the Adobe Campaign Standard controls—tracking activation, link-level tracking, consent data model, opt-out mechanisms, and reporting—that can support your compliance efforts.

>[!ENDSHADEBOX]

This post is for informational purposes only. It is not legal advice and does not warrant your compliance with applicable law. The Adobe Campaign Standard product capabilities described below are building blocks that, configured and operated appropriately, may support a compliant implementation. Each customer is responsible for determining and complying with its obligations under applicable law.

## Overview {#overview}

On April 14, 2026, the *Commission nationale de l'informatique et des libertés* (CNIL), France's data protection authority, published a [recommendation on the use of tracking pixels within emails](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf). The guidance clarifies when consent is required and highlights the importance of proper consent practices for email pixel tracking. This policy could impact sending practices for any entity delivering emails to subscribers based in France.

CNIL provided a three-month period from the date of the recommendation for companies to inform their email recipients ("users") of the presence of the tracking pixels, their purpose, and users' right to opt-out. During this transition period, customers are expected to notify users about pixel tracking and provide an opt-out if necessary. CNIL is expected to begin enforcement activities after July 14, 2026.

As the CNIL and other regulators clarify guidance on tracking pixels and related issues, Adobe will continue to monitor updates and inform customers of the technical capabilities of Adobe products that support email marketing, including Adobe Campaign Standard.

Adobe email marketing execution applications, including Adobe Journey Optimizer, Journey Optimizer B2B, Adobe Campaign, and Marketo Engage, provide controls that can help customers manage open tracking at the delivery or email level. Customers are responsible for determining their own compliance obligations under applicable CNIL guidance and other laws, but these capabilities may support customer compliance efforts.

### What is an email tracking pixel {#tracking-pixel}

An email tracking pixel is a 1x1 transparent image embedded in the HTML of an email. When the recipient's email client loads that image, the pixel pings a server that records data such as a timestamp, device type, email client and sometimes an IP address for approximate location. That log is then tied to a recipient's record, allowing marketers to see whether an email is opened.

### Customer support {#support}

Customers seeking assistance implementing the changes described above may engage with their existing Adobe ecosystem. For technical questions about the Adobe capabilities referenced, contact your Customer Success Manager or technical account manager.

## Adobe Campaign Standard functionality related to email tracking {#acs-functionality}

Customers may use Adobe Campaign Standard's native tracking, schema, and personalization mechanisms to address certain elements when configuring architecture.

### Email classification {#email-classification}

Extend the delivery template with a custom field indicating the type of the email (authentication, deliverability-only, transactional, marketing with consent, B2B prospecting). In Campaign Standard, delivery templates can carry custom fields that flow into reporting and workflow logic. This classification drives which tracking is appropriate for each send.

[Learn how to create and use delivery templates](../../channels/using/creating-an-email.md)

### Consent data model {#consent-data-model}

Extend the Profile resource via the Campaign Standard custom resource mechanism (**Administration > Development > Custom Resources**) to carry per-purpose consent flags, consent timestamps, and the date of the most recent open (date only — no time component). A separate custom resource linked to the Profile captures the append-only consent event log that supports individual proof of consent. Since Campaign Standard landing pages can write directly to Profile fields, the current consent state is manageable natively; the consent log is written via the Adobe Campaign Standard REST API (`/profileAndServicesExt`) once a preference is submitted.

[Learn how to create or extend a resource](../../developing/using/creating-or-extending-the-resource.md)

[Learn how to interact with custom resources via API](../../api/using/interacting-with-custom-resources.md)

### Pixel emission {#pixel-emission}

Adobe Campaign Standard controls tracking at the delivery level via the **[!UICONTROL Activate tracking]** toggle in the delivery or template properties. For deliveries where open tracking is not lawful (authentication-only, re-solicitation emails), this toggle is disabled. For deliveries where per-purpose pixel emission is appropriate, one approach is to disable the standard auto-inserted pixel and use content blocks containing conditional 1×1 tracked image elements — one per purpose — where each image is assigned a URL category (`PIX_DELIV`, `PIX_PERF`, `PIX_PROFILE`, `PIX_FRAUD`) and is shown only when the recipient's corresponding consent flag is true.

[Learn how to configure email tracking parameters](configuring-email-channel.md#tracking-parameters)

[Learn how to manage tracked URLs in the Email Designer](../../designing/using/links.md#about-tracked-urls)

[Learn how to add content blocks](../../designing/using/personalization.md#adding-a-content-block)

### Withdrawal {#withdrawal}

Add a **Manage tracker preferences** link to every email footer, distinct from the unsubscribe link. The link points to a Campaign Standard landing page authenticated via the `recipientId` or `urlSubscription` mechanism; the recipient toggles their per-purpose consent flags and submits. On confirmation, a small call to the Campaign Standard REST API writes the withdrawal event to the consent log. The recommendation indicates that this link is itself security-exempt from the tracking requirement.

[Learn how to set up opt-in and opt-out landing pages](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#setting-up-opt-in-and-opt-out-landing-pages)

[Learn how to get started with landing pages](../../channels/using/getting-started-with-landing-pages.md)

### Proof of consent {#consent-proof}

Each consent change — capture at sign-up, update from the preferences page, expiry — creates a row in the consent log custom resource, carrying the wording version code, capture timestamp, capture source, and the scope. This log is queryable through the Campaign Standard explorer, exposable via the REST API, and exportable for DPO review via a scheduled workflow.

[Learn how to interact with custom resources via API](../../api/using/interacting-with-custom-resources.md)

### Re-solicitation governance {#re-solicitation}

A custom `cusLastPixelRefusalDate` field on the Profile, combined with a typology filtering rule that excludes profiles where that field is within a chosen period of time, prevents re-solicitation of recipients who have declined in that time. A scheduled workflow manages customers' consent expiry timeframes by flagging stale records and writing expiry events to the consent log.

[Learn how to work with typology rules](../../sending/using/about-typology-rules.md)

[Learn how to manage typology rules](../../sending/using/managing-typology-rules.md)

### Reporting {#reporting}

Campaign Standard Dynamic Reports are built on URL categories and profile dimensions. The per-purpose URL categories introduced above surface in Dynamic Reports as new dimensions, allowing operators to slice open and click data by purpose. The distinction between consented and non-consented tracking is visible natively once the URL categories are in place.

[Learn how to get started with Dynamic Reports](../../reporting/using/about-dynamic-reports.md)

[Learn about tracking indicators](../../reporting/using/tracking-indicators.md)
