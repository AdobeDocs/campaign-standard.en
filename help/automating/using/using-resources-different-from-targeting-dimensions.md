---
title: Using resources different from targeting dimensions
description: Learn how to use a resource that is different from the targeting dimension.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: query,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 5805bdfa-fb33-4a46-ba1e-7a10b067349b
TQID: https://experienceleague.adobe.com/tGVP20eQpo7EuB1xluX2AQHHMZ-IM-q6JmgFGp6Iwk4
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
---
# Using resources different from targeting dimensions {#using-resources-different-from-targeting-dimensions}

This use cases presents how to use a resource that is different from the targeting dimension, for example, to look up for a specific record in a distant table.

For more on targeting dimensions and resources, refer to [this section](../../automating/using/query.md#targeting-dimensions-and-resources)

**Example 1: identifying profiles targeted by the delivery with the label ”Welcome back !”**.

* In this case, we want to target profiles. We will set the targeting dimension to **[!UICONTROL Profiles (profile)]**.
* We want to filter the selected profiles according to the delivery label. We will therefore set the resource to **[!UICONTROL Delivery logs]**. This way, we are filtering directly in the delivery log table, which will offer better performance.

![](assets/targeting_dimension6.png)

![](assets/targeting_dimension7.png)

**Example 2: identifying profiles who were not targeted by the delivery with the label “Welcome back !”**

In the previous example, we used a resource different from the targeting dimension. This operation is only possible if you want to find a record that **is present** in the distant table (delivery logs in our example).

If we want to find a record that **is not present** in the distant table (for example, profiles who were not targeted by a specific delivery), you must use the same resource and targeting dimension, as the record will not be present in the distant table (delivery logs).

* In this case, we want to target profiles. We will set the targeting dimension to **[!UICONTROL Profiles (profile)]**.
* We want to filter the selected profiles according to the delivery label. It is not possible to filter directly on delivery logs as we are looking for a record not present in the delivery logs table. We will therefore set the resource to **[!UICONTROL Profile (profile)]** and build our query on the profiles table.

![](assets/targeting_dimension8.png)

![](assets/targeting_dimension9.png)
