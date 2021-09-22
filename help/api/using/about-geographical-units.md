---
title: About geographical units
description: Learn more about geographical units and APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

---

# About geographical units {#about-geographical-units}

>[!CAUTION]
>
>The Geographical unit feature has been deprecated with the Campaign Standard 18.7 release.
>
>As a result, new Campaign Standard instances, as well as existing instances with no geographical units created, cannot have this capability implemented starting the 18.7 release.
>
>For more on this, refer to the <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html">Deprecated features</a> page.

The **geoUnitBase** endpoint lets you interact with Geographical units, enabling you, for example, to update their attributes or update a profile's unit.

The **Geographical unit** field is added to a profile when extending the profile resource. As a result, remember to always use the **profileAndServicesExt** endpoint to interact with Geographical units. For more on the profile's resource extension, refer to the [Campaign documentation](https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles).
