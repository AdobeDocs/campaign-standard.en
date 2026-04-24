---
title: Updates and maintenance operations
description: Information about update and maintenance operations for the Adobe Campaign server.
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 4da0b7b0-a854-4935-9f5f-04bfc764b18d
TQID: https://experienceleague.adobe.com/aWpRR9r5jK3vVHxO9-xFPrVSyTI9Cg2rIBJ6AzvEONQ
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
    internal-label: APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Updates and maintenance operations{#updates-and-maintenance-operations}

For maintenance purposes, the Adobe Campaign server is restarted every day at 6 AM (server time zone). Contact Adobe to know the server time. This operation is automatic and transparent. However, we recommend that you do not perform any data processing operations right before the restart. For example, avoid starting workflows before the restart, schedule them to start one minute after.

Adobe continuously improves its solutions by adding new capabilities, enhancements and fixes. All Adobe Campaign Standard instances are upgraded with every new release. No action is required to upgrade. Upgrades are deployed in two phases. First, Stage instances are upgraded to allow our customers to test new capabilities and adapt their configuration if needed. Production instances are then subsequently upgraded. Consult the [Release Planning](https://helpx.adobe.com/campaign/kb/acs-release-planning.html) to find out when the next release will happen. Also consult the list of [Deprecated and Removed Features](../../rn/using/deprecated-features.md).
