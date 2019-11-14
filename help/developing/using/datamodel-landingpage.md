---
title: About SMS and push content design
description: Learn about the editor used to modify the content of your SMS messages and push notifications in Adobe Campaign.
page-status-flag: never-activated
uuid: 99277e46-e4f7-49a9-ba27-b878780f90da
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-sms-and-push-content
discoiquuid: 6e21db35-daf9-4edb-977a-6ef606db0e4d
context-tags: delivery,smsContent,back
internal: n
snippet: y
---

# Lanfinng

<table cellpadding="4" cellspacing="0" summary="" class="simpletable">
<tr class="sthead"><th valign="bottom" id="d5439e17" class="stentry">Name</th>
<th valign="bottom" id="d5439e19" class="stentry">Label</th>
<th valign="bottom" id="d5439e21" class="stentry">Type (length)</th>
<th valign="bottom" id="d5439e23" class="stentry">Enumeration values</th>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">PKey</td>
<td valign="top" headers="d5439e19" class="stentry">Main resource ID</td>
<td valign="top" headers="d5439e21" class="stentry">string </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">additionalData</td>
<td valign="top" headers="d5439e19" class="stentry">Additional data</td>
<td valign="top" headers="d5439e21" class="stentry">collection </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">additionalLanguages</td>
<td valign="top" headers="d5439e19" class="stentry">Other languages</td>
<td valign="top" headers="d5439e21" class="stentry">item </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">allowNonIdentifiedTarget</td>
<td valign="top" headers="d5439e19" class="stentry">Authorize unidentified visitors</td>
<td valign="top" headers="d5439e21" class="stentry">boolean </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">branding (brandingBase)</td>
<td valign="top" headers="d5439e19" class="stentry">Brand</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">builtIn</td>
<td valign="top" headers="d5439e19" class="stentry">Built-in application object</td>
<td valign="top" headers="d5439e21" class="stentry">boolean </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">cache</td>
<td valign="top" headers="d5439e19" class="stentry">Cache</td>
<td valign="top" headers="d5439e21" class="stentry">string </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">campaign (campaignBase)</td>
<td valign="top" headers="d5439e19" class="stentry">Campaign</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">closedLog</td>
<td valign="top" headers="d5439e19" class="stentry">'Landing page closed' log</td>
<td valign="top" headers="d5439e21" class="stentry">string </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">contextResourceType</td>
<td valign="top" headers="d5439e19" class="stentry">ContextResourceType</td>
<td valign="top" headers="d5439e21" class="stentry">string </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">created</td>
<td valign="top" headers="d5439e19" class="stentry">Created</td>
<td valign="top" headers="d5439e21" class="stentry">date </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">createdBy (userBase)</td>
<td valign="top" headers="d5439e19" class="stentry">Created by</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">cryptKey</td>
<td valign="top" headers="d5439e19" class="stentry">AES encryption key</td>
<td valign="top" headers="d5439e21" class="stentry">string (64)</td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">defaultLanguage</td>
<td valign="top" headers="d5439e19" class="stentry">Default language</td>
<td valign="top" headers="d5439e21" class="stentry">enumeration (string) (255)</td>
<td valign="top" headers="d5439e23" class="stentry"><ul class="ul"><li class="li">Greek - el - el</li>
<li class="li">English - en - en</li>
<li class="li">Chinese - zh - zh</li>
<li class="li">French (France) - fr_FR - fr_FR</li>
<li class="li">Vietnamese - vi - vi</li>
<li class="li">Portuguese (Portugal) - pt_PT - pt_PT</li>
<li class="li">Italian (Italy) - it_IT - it_IT</li>
<li class="li">Italian - it - it</li>
<li class="li">Dutch (Belgium) - nl_BE - nl_BE</li>
<li class="li">Norwegian (Norway) - no_NO - no_NO</li>
<li class="li">Dutch (Netherlands) - nl_NL - nl_NL</li>
<li class="li">Arabic - ar - ar</li>
<li class="li">English (United States) - en_US - en_US</li>
<li class="li">Irish - ga - ga</li>
<li class="li">Czech - cs - cs</li>
<li class="li">Estonian - et - et</li>
<li class="li">Indonesian - id - id</li>
<li class="li">Spanish - es - es</li>
<li class="li">Russian - ru - ru</li>
<li class="li">Dutch - nl - nl</li>
<li class="li">Walloon - wa - wa</li>
<li class="li">Portuguese - pt - pt</li>
<li class="li">French (Belgium) - fr_BE - fr_BE</li>
<li class="li">Latvian - lv - lv</li>
<li class="li">Lithuanian - lt - lt</li>
<li class="li">Thai - th - th</li>
<li class="li">English (United Kingdom) - en_GB - en_GB</li>
<li class="li">French - fr - fr</li>
<li class="li">Portuguese (Brazil) - pt_BR - pt_BR</li>
<li class="li">German - de - de</li>
<li class="li">Danish - da - da</li>
<li class="li">Finnish - fi - fi</li>
<li class="li">Hungarian - hu - hu</li>
<li class="li">Swedish (Finland) - sv_FI - sv_FI</li>
<li class="li">Japanese - ja - ja</li>
<li class="li">Hebrew - he - he</li>
<li class="li">Korean - ko - ko</li>
<li class="li">Swedish - sv - sv</li>
<li class="li">Sweden (Swedish) - sv_SE - sv_SE</li>
<li class="li">Slovak - sk - sk</li>
<li class="li">Maltese - mt - mt</li>
<li class="li">Italian (Switzerland) - it_CH - it_CH</li>
<li class="li">Polish - pl - pl</li>
<li class="li">Slovene - sl - sl</li>
<li class="li">INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
</ul>
</td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">defaultOrigin (delivery)</td>
<td valign="top" headers="d5439e19" class="stentry">Traffic source</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">desc</td>
<td valign="top" headers="d5439e19" class="stentry">Description</td>
<td valign="top" headers="d5439e21" class="stentry">string (512)</td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">designLanguage</td>
<td valign="top" headers="d5439e19" class="stentry">Design language</td>
<td valign="top" headers="d5439e21" class="stentry">enumeration (string) (255)</td>
<td valign="top" headers="d5439e23" class="stentry"><ul class="ul"><li class="li">Greek - el - el</li>
<li class="li">English - en - en</li>
<li class="li">Chinese - zh - zh</li>
<li class="li">French (France) - fr_FR - fr_FR</li>
<li class="li">Vietnamese - vi - vi</li>
<li class="li">Portuguese (Portugal) - pt_PT - pt_PT</li>
<li class="li">Italian (Italy) - it_IT - it_IT</li>
<li class="li">Italian - it - it</li>
<li class="li">Dutch (Belgium) - nl_BE - nl_BE</li>
<li class="li">Norwegian (Norway) - no_NO - no_NO</li>
<li class="li">Dutch (Netherlands) - nl_NL - nl_NL</li>
<li class="li">Arabic - ar - ar</li>
<li class="li">English (United States) - en_US - en_US</li>
<li class="li">Irish - ga - ga</li>
<li class="li">Czech - cs - cs</li>
<li class="li">Estonian - et - et</li>
<li class="li">Indonesian - id - id</li>
<li class="li">Spanish - es - es</li>
<li class="li">Russian - ru - ru</li>
<li class="li">Dutch - nl - nl</li>
<li class="li">Walloon - wa - wa</li>
<li class="li">Portuguese - pt - pt</li>
<li class="li">French (Belgium) - fr_BE - fr_BE</li>
<li class="li">Latvian - lv - lv</li>
<li class="li">Lithuanian - lt - lt</li>
<li class="li">Thai - th - th</li>
<li class="li">English (United Kingdom) - en_GB - en_GB</li>
<li class="li">French - fr - fr</li>
<li class="li">Portuguese (Brazil) - pt_BR - pt_BR</li>
<li class="li">German - de - de</li>
<li class="li">Danish - da - da</li>
<li class="li">Finnish - fi - fi</li>
<li class="li">Hungarian - hu - hu</li>
<li class="li">Swedish (Finland) - sv_FI - sv_FI</li>
<li class="li">Japanese - ja - ja</li>
<li class="li">Hebrew - he - he</li>
<li class="li">Korean - ko - ko</li>
<li class="li">Swedish - sv - sv</li>
<li class="li">Sweden (Swedish) - sv_SE - sv_SE</li>
<li class="li">Slovak - sk - sk</li>
<li class="li">Maltese - mt - mt</li>
<li class="li">Italian (Switzerland) - it_CH - it_CH</li>
<li class="li">Polish - pl - pl</li>
<li class="li">Slovene - sl - sl</li>
<li class="li">INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
</ul>
</td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">dynamicService</td>
<td valign="top" headers="d5439e19" class="stentry">Dynamic service</td>
<td valign="top" headers="d5439e21" class="stentry">boolean </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">end</td>
<td valign="top" headers="d5439e19" class="stentry">Expiration date</td>
<td valign="top" headers="d5439e21" class="stentry">date </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">errorContextResourceType</td>
<td valign="top" headers="d5439e19" class="stentry">ErrorContextResourceType</td>
<td valign="top" headers="d5439e21" class="stentry">string </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">errorPage</td>
<td valign="top" headers="d5439e19" class="stentry">Error page</td>
<td valign="top" headers="d5439e21" class="stentry">item </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">geoUnit (geoUnitBase)</td>
<td valign="top" headers="d5439e19" class="stentry">Geographical unit</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">htmlPage</td>
<td valign="top" headers="d5439e19" class="stentry">Pages</td>
<td valign="top" headers="d5439e21" class="stentry">collection </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">identificationByUrlParam</td>
<td valign="top" headers="d5439e19" class="stentry">Identification by URL parameters</td>
<td valign="top" headers="d5439e21" class="stentry">boolean </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">inactiveUrlRedirection</td>
<td valign="top" headers="d5439e19" class="stentry">Redirection URL</td>
<td valign="top" headers="d5439e21" class="stentry">string (4096)</td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">isExternal</td>
<td valign="top" headers="d5439e19" class="stentry">Is external resource</td>
<td valign="top" headers="d5439e21" class="stentry">boolean </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">isTemplate</td>
<td valign="top" headers="d5439e19" class="stentry">Template</td>
<td valign="top" headers="d5439e21" class="stentry">boolean </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">job</td>
<td valign="top" headers="d5439e19" class="stentry">Job</td>
<td valign="top" headers="d5439e21" class="stentry">collection </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">jobLogs</td>
<td valign="top" headers="d5439e19" class="stentry">Logs</td>
<td valign="top" headers="d5439e21" class="stentry">collection </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">label</td>
<td valign="top" headers="d5439e19" class="stentry">Label</td>
<td valign="top" headers="d5439e21" class="stentry">string (128)</td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">lastModified</td>
<td valign="top" headers="d5439e19" class="stentry">Last modified</td>
<td valign="top" headers="d5439e21" class="stentry">date </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">loadingFilter (queryFilterBase)</td>
<td valign="top" headers="d5439e19" class="stentry">Loading key</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">loadingFilterMapping</td>
<td valign="top" headers="d5439e19" class="stentry">Parameters of the loading key</td>
<td valign="top" headers="d5439e21" class="stentry">collection </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">logicalStatus</td>
<td valign="top" headers="d5439e19" class="stentry">Execution status</td>
<td valign="top" headers="d5439e21" class="stentry">enumeration (string) (255)</td>
<td valign="top" headers="d5439e23" class="stentry"><ul class="ul"><li class="li">In progress - started - started</li>
<li class="li">Editing - edition - edition</li>
<li class="li">Finished - finished - finished</li>
<li class="li">Warning - warning - warning</li>
<li class="li">Erroneous - error - error</li>
<li class="li">INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
</ul>
</td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">messageAction</td>
<td valign="top" headers="d5439e19" class="stentry">Start sending message</td>
<td valign="top" headers="d5439e21" class="stentry">boolean </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">messageActionDelivery (deliveryMCTemplateBase)</td>
<td valign="top" headers="d5439e19" class="stentry">Transactional message</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">modifiedBy (userBase)</td>
<td valign="top" headers="d5439e19" class="stentry">Modified by</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">name</td>
<td valign="top" headers="d5439e19" class="stentry">ID</td>
<td valign="top" headers="d5439e21" class="stentry">string (64)</td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">orgUnit (orgUnitBase)</td>
<td valign="top" headers="d5439e19" class="stentry">Organizational unit</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">prefill</td>
<td valign="top" headers="d5439e19" class="stentry">Preload visitor data</td>
<td valign="top" headers="d5439e21" class="stentry">boolean </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">program (programBase)</td>
<td valign="top" headers="d5439e19" class="stentry">Program</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">publicUrl</td>
<td valign="top" headers="d5439e19" class="stentry">Public URL</td>
<td valign="top" headers="d5439e21" class="stentry">string </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">publicationDate</td>
<td valign="top" headers="d5439e19" class="stentry">Publication date</td>
<td valign="top" headers="d5439e21" class="stentry">date </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">reconciliationFilter (queryFilterBase)</td>
<td valign="top" headers="d5439e19" class="stentry">Reconciliation key</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">reconciliationFilterMapping</td>
<td valign="top" headers="d5439e19" class="stentry">Reconciliation key parameters</td>
<td valign="top" headers="d5439e21" class="stentry">collection </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">reconciliationUpdateStrategy</td>
<td valign="top" headers="d5439e19" class="stentry">Update strategy</td>
<td valign="top" headers="d5439e21" class="stentry">enumeration (byte) </td>
<td valign="top" headers="d5439e23" class="stentry"><ul class="ul"><li class="li">Update - updateTarget - 1</li>
<li class="li">Unauthorized - unauthorized - 0</li>
<li class="li">INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
</ul>
</td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">service (serviceBase)</td>
<td valign="top" headers="d5439e19" class="stentry">Subscription service</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">specificAction</td>
<td valign="top" headers="d5439e19" class="stentry">Specific action</td>
<td valign="top" headers="d5439e21" class="stentry">enumeration (byte) </td>
<td valign="top" headers="d5439e23" class="stentry"><ul class="ul"><li class="li">Blacklist - blackList - 3</li>
<li class="li">No specific action - none - 0</li>
<li class="li">Unsubscription - unsubscription - 2</li>
<li class="li">INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
<li class="li">Subscription - subscription - 1</li>
</ul>
</td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">start</td>
<td valign="top" headers="d5439e19" class="stentry">Deployment date</td>
<td valign="top" headers="d5439e21" class="stentry">date </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">state</td>
<td valign="top" headers="d5439e19" class="stentry">Status</td>
<td valign="top" headers="d5439e21" class="stentry">enumeration (byte) </td>
<td valign="top" headers="d5439e23" class="stentry"><ul class="ul"><li class="li">Editing - edit - 0</li>
<li class="li">Publishing failed - failed - 99</li>
<li class="li">Closed - closed - 20</li>
<li class="li">INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
<li class="li">Online - opened - 10</li>
</ul>
</td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">targetResource</td>
<td valign="top" headers="d5439e19" class="stentry">Targeting dimension</td>
<td valign="top" headers="d5439e21" class="stentry">string (255)</td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">template (landingPage)</td>
<td valign="top" headers="d5439e19" class="stentry">Landing page template</td>
<td valign="top" headers="d5439e21" class="stentry">link </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">testUrl</td>
<td valign="top" headers="d5439e19" class="stentry">Test URL</td>
<td valign="top" headers="d5439e21" class="stentry">string </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">thumbnail</td>
<td valign="top" headers="d5439e19" class="stentry">Thumbnail</td>
<td valign="top" headers="d5439e21" class="stentry">string (255)</td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">timezone</td>
<td valign="top" headers="d5439e19" class="stentry">Time zone</td>
<td valign="top" headers="d5439e21" class="stentry">enumeration (string) (64)</td>
<td valign="top" headers="d5439e23" class="stentry"><ul class="ul"><li class="li">(GMT-02:00) Central-Atlantic - Atlantic_South_Georgia - Atlantic/South_Georgia</li>
<li class="li">(GMT+02:00) Amman - Asia_Amman - Asia/Amman</li>
<li class="li">(GMT-03:00) Brasi - America_Sao_Paulo - America/Sao_Paulo</li>
<li class="li">(GMT+06:00) Astana, Dhaka - Asia_Dhaka - Asia/Dhaka</li>
<li class="li">(GMT+06:00) Novossibirsk - Asia_Novosibirsk - Asia/Novosibirsk</li>
<li class="li">(GMT+02:00) Windhoek - Africa_Windhoek - Africa/Windhoek</li>
<li class="li">(GMT+04:00) Caucasus, Erevan - Asia_Yerevan - Asia/Yerevan</li>
<li class="li">(GMT-04:00) Manaus - America_Manaus - America/Manaus</li>
<li class="li">(GMT+03:30) Teheran - Asia_Tehran - Asia/Tehran</li>
<li class="li">(GMT+12:00) Auckland, Wellington - Pacific_Auckland - Pacific/Auckland</li>
<li class="li">(GMT+02:00) Jerusalem - Asia_Jerusalem - Asia/Jerusalem</li>
<li class="li">(GMT+03:00) Moscow, St. Petersburg, Volgograd - Europe_Moscow - Europe/Moscow</li>
<li class="li">(GMT+09:30) Adelaïde - Australia_Adelaide - Australia/Adelaide</li>
<li class="li">(GMT+10:00) Canberra, Melbourne, Sydney - Australia_Canberra - Australia/Canberra</li>
<li class="li">(GMT+08:00) Perth - Australia_Perth - Australia/Perth</li>
<li class="li">(GMT+09:00) Yakoutsk - Asia_Yakutsk - Asia/Yakutsk</li>
<li class="li">(GMT-10:00) Hawai - Pacific_Honolulu - Pacific/Honolulu</li>
<li class="li">(GMT+04:00) Baku - Asia_Baku - Asia/Baku</li>
<li class="li">(GMT+10:00) Vladivostok - Asia_Vladivostok - Asia/Vladivostok</li>
<li class="li">(GMT+09:00) Seoul - Asia_Seoul - Asia/Seoul</li>
<li class="li">(GMT+01:00) Sarajevo, Skoplje, Sofia, Warsaw, Zagreb - Europe_Sarajevo - Europe/Sarajevo</li>
<li class="li">Server time zone - _server_ - _server_</li>
<li class="li">(GMT+04:00) Abu Dhabi, Muscat - Asia_Muscat - Asia/Muscat</li>
<li class="li">(GMT+08:00) Kuala Lumpur, Singapore - Asia_Kuala_Lumpur - Asia/Kuala_Lumpur</li>
<li class="li">(GMT+09:00) Osaka, Sapporo, Tokyo - Asia_Tokyo - Asia/Tokyo</li>
<li class="li">(GMT+10:00) Brisbane - Australia_Brisbane - Australia/Brisbane</li>
<li class="li">(GMT+05:30) Sri Jayawardenepura - Asia_Colombo - Asia/Colombo</li>
<li class="li">(GMT+02:00) Harare, Pretoria - Africa_Harare - Africa/Harare</li>
<li class="li">(GMT+08:00) Oulan-Bator - Asia_Ulan_Bator - Asia/Ulan_Bator</li>
<li class="li">(GMT-02:00) Greenwich Mean Time minus 2 hours - Gmt_m2 - Etc/GMT+2</li>
<li class="li">(GMT-03:00) Greenwich Mean Time minus 3 hours - Gmt_m3 - Etc/GMT+3</li>
<li class="li">(GMT-01:00) Greenwich Mean Time minus 1 hour - Gmt_m1 - Etc/GMT+1</li>
<li class="li">(GMT-06:00) Greenwich Mean Time minus 6 hours - Gmt_m6 - Etc/GMT+6</li>
<li class="li">(GMT-07:00) Greenwich Mean Time minus 7 hours - Gmt_m7 - Etc/GMT+7</li>
<li class="li">(GMT-04:00) Greenwich Mean Time minus 4 hours - Gmt_m4 - Etc/GMT+4</li>
<li class="li">(GMT) Casablanca - Africa_Casablanca - Africa/Casablanca</li>
<li class="li">(GMT+05:30) Kolkata, Chennai, Mumbai, New Delhi - Asia_Kolkata - Asia/Kolkata</li>
<li class="li">(GMT-11:00) Greenwich Mean Time minus 11 hours - Gmt_m11 - Etc/GMT+11</li>
<li class="li">(GMT-09:00) Greenwich Mean Time minus 9 hours - Gmt_m9 - Etc/GMT+9</li>
<li class="li">(GMT-03:30) Newfoundland - America_St_Johns - America/St_Johns</li>
<li class="li">Default - _inherit_ - _inherit_</li>
<li class="li">(GMT+03:00) Greenwich Mean Time plus 3 hours - Gmt_p3 - Etc/GMT-3</li>
<li class="li">(GMT-04:30) Caracas - America_Caracas - America/Caracas</li>
<li class="li">(GMT+01:00) Amsterdam, Berlin, Berne, Rome, Stockholm, Vienna - Europe_Berlin - Europe/Berlin</li>
<li class="li">(GMT-07:00) Chihuahua, La Paz, Mazatlan - America_Chihuahua - America/Chihuahua</li>
<li class="li">(GMT+03:00) Nairobi - Africa_Nairobi - Africa/Nairobi</li>
<li class="li">(GMT-04:00) Asunción - America_Asuncion - America/Asuncion</li>
<li class="li">(GMT+03:00) Bagdad - Asia_Baghdad - Asia/Baghdad</li>
<li class="li">(GMT-10:00) Greenwich Mean Time minus 10 hours - Gmt_m10 - Etc/GMT+10</li>
<li class="li">(GMT-03:00) Greenland - America_Godthab - America/Godthab</li>
<li class="li">(GMT+02:00) Damas - Asia_Damascus - Asia/Damascus</li>
<li class="li">(GMT-11:00) Samoa - Pacific_Samoa - Pacific/Samoa</li>
<li class="li">(GMT-05:00) Bogota, Lima, Quito - America_Bogota - America/Bogota</li>
<li class="li">(GMT+01:00) Brussels, Copenhagen, Madrid, Paris - Europe_Paris - Europe/Paris</li>
<li class="li">(GMT+08:00) Beijing, Chongqing, Hong Kong, Urumqi - Asia_Shanghai - Asia/Shanghai</li>
<li class="li">(GMT+12:00) Fidji - Pacific_Fiji - Pacific/Fiji</li>
<li class="li">(GMT+02:00) Athens, Istanbul, Minsk - Europe_Athens - Europe/Athens</li>
<li class="li">(GMT+04:00) Tbilissi - Asia_Tbilisi - Asia/Tbilisi</li>
<li class="li">INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
<li class="li">(GMT+05:45) Katmandu - Asia_Katmandu - Asia/Katmandu</li>
<li class="li">(GMT-05:00) Indiana (East) - America_Indianapolis - America/Indianapolis</li>
<li class="li">(GMT-01:00) Cape Verde islands - Atlantic_Cape_Verde - Atlantic/Cape_Verde</li>
<li class="li">(GMT+04:00) Port Louis - Indian_Mauritius - Indian/Mauritius</li>
<li class="li">(GMT+08:00) Taipei - Asia_Taipei - Asia/Taipei</li>
<li class="li">Time zone of the database - _wdbc_ - _wdbc_</li>
<li class="li">(GMT+06:30) Rangoon - Asia_Rangoon - Asia/Rangoon</li>
<li class="li">(GMT+11:00) Magadan, The Solomon Islands, New Caledonia - Pacific_Guadalcanal - Pacific/Guadalcanal</li>
<li class="li">(GMT+02:00) Cairo - Africa_Cairo - Africa/Cairo</li>
<li class="li">(GMT+05:00) Iekaterinburg - Asia_Yekaterinburg - Asia/Yekaterinburg</li>
<li class="li">(GMT+08:00) Irkoutsk - Asia_Irkutsk - Asia/Irkutsk</li>
<li class="li">(GMT+10:00) Guam, Port Moresby - Pacific_Guam - Pacific/Guam</li>
<li class="li">(GMT-04:00) Atlantic Standard Time (Canada) - America_Halifax - America/Halifax</li>
<li class="li">(GMT) Greenwich mean time - GMT - GMT</li>
<li class="li">(GMT-04:00) La Paz - America_La_Paz - America/La_Paz</li>
<li class="li">Operator time zone - _login_ - _login_</li>
<li class="li">(GMT-06:00) Guadalajara, Mexico, Monterrey - America_Mexico_City - America/Mexico_City</li>
<li class="li">(GMT+09:30) Darwin - Australia_Darwin - Australia/Darwin</li>
<li class="li">(GMT-05:00) Est (United States and Canada) - America_New_York - America/New_York</li>
<li class="li">(GMT-05:00) Greenwich Mean Time minus 5 hours - Gmt_m5 - Etc/GMT+5</li>
<li class="li">(GMT+05:00) Islamabad, Karachi, Tachkent - Asia_Karachi - Asia/Karachi</li>
<li class="li">(GMT+03:00) Koweït, Riyad - Asia_Riyadh - Asia/Riyadh</li>
<li class="li">(GMT-08:00) Greenwich Mean Time minus 8 hours - Gmt_m8 - Etc/GMT+8</li>
<li class="li">(GMT-01:00) The Azores - Atlantic_Azores - Atlantic/Azores</li>
<li class="li">(GMT+07:00) Bangkok, Hanoi, Djakarta - Asia_Bangkok - Asia/Bangkok</li>
<li class="li">(GMT) Monrovia - Africa_Monrovia - Africa/Monrovia</li>
<li class="li">(GMT-09:00) Alaska - America_Anchorage - America/Anchorage</li>
<li class="li">(GMT+01:00) Belgrade, Bratislava, Budapest, Ljubljana, Prague - Europe_Belgrade - Europe/Belgrade</li>
<li class="li">(GMT) Reykjavik - Atlantic_Reykjavik - Atlantic/Reykjavik</li>
<li class="li">(GMT+02:00) Bucarest - Europe_Bucharest - Europe/Bucharest</li>
<li class="li">(GMT+05:00) Greenwich Mean Time plus 5 hours - Gmt_p5 - Etc/GMT-5</li>
<li class="li">(GMT+04:00) Greenwich Mean Time plus 4 hours - Gmt_p4 - Etc/GMT-4</li>
<li class="li">(GMT+07:00) Greenwich Mean Time plus 7 hours - Gmt_p7 - Etc/GMT-7</li>
<li class="li">(GMT+06:00) Greenwich Mean Time plus 6 hours - Gmt_p6 - Etc/GMT-6</li>
<li class="li">(GMT+01:00) Greenwich Mean Time plus 1 hour - Gmt_p1 - Etc/GMT-1</li>
<li class="li">(GMT-08:00) Pacific (United States and Canada) - America_Los_Angeles - America/Los_Angeles</li>
<li class="li">(GMT+02:00) Greenwich Mean Time plus 2 hours - Gmt_p2 - Etc/GMT-2</li>
<li class="li">(GMT+07:00) Krasnoïarsk - Asia_Krasnoyarsk - Asia/Krasnoyarsk</li>
<li class="li">(GMT+09:00) Greenwich Mean Time plus 9 hours - Gmt_p9 - Etc/GMT-9</li>
<li class="li">(GMT+08:00) Greenwich Mean Time plus 8 hours - Gmt_p8 - Etc/GMT-8</li>
<li class="li">(GMT+10:00) Hobart - Australia_Hobart - Australia/Hobart</li>
<li class="li">(GMT+13:00) Nuku'alofa - Pacific_Tongatapu - Pacific/Tongatapu</li>
<li class="li">(GMT-06:00) Central America - America_Regina - America/Regina</li>
<li class="li">(GMT-03:00) Buenos Aires, Cayenne, Fortaleza - America_Buenos_Aires - America/Buenos_Aires</li>
<li class="li">(GMT-07:00) Rocky Mountains (United States and Canada) - America_Denver - America/Denver</li>
<li class="li">(GMT+01:00) Central Africa - West - Africa_Luanda - Africa/Luanda</li>
<li class="li">(GMT+02:00) Helsinki, Kiev, Riga, Sofia, Tallinn, Vilnius - Europe_Helsinki - Europe/Helsinki</li>
<li class="li">(GMT) Greenwich Mean Time: Dublin, Edinburgh, Lisbon, London - Europe_London - Europe/London</li>
<li class="li">(GMT-07:00) Arizona - America_Phoenix - America/Phoenix</li>
<li class="li">(GMT+02:00) Beirut - Asia_Beirut - Asia/Beirut</li>
<li class="li">(GMT+04:30) Kabul - Asia_Kabul - Asia/Kabul</li>
<li class="li">(GMT-06:00) Center (United States and Canada) - America_Chicago - America/Chicago</li>
<li class="li">(GMT+11:00) Greenwich Mean Time plus 11 hours - Gmt_p11 - Etc/GMT-11</li>
<li class="li">(GMT+10:00) Greenwich Mean Time plus 10 hours - Gmt_p10 - Etc/GMT-10</li>
<li class="li">(GMT+13:00) Greenwich Mean Time plus 13 hours - Gmt_p13 - Etc/GMT-13</li>
<li class="li">(GMT+12:00) Greenwich Mean Time plus 12 hours - Gmt_p12 - Etc/GMT-12</li>
<li class="li">(GMT-04:00) Santiago - America_Santiago - America/Santiago</li>
<li class="li">(GMT-03:00) Montevideo - America_Montevideo - America/Montevideo</li>
<li class="li">(GMT-04:00) Cuiaba - America_Cuiaba - America/Cuiaba</li>
</ul>
</td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">title</td>
<td valign="top" headers="d5439e19" class="stentry">Landing page</td>
<td valign="top" headers="d5439e21" class="stentry">string (255)</td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">trackingEnabled</td>
<td valign="top" headers="d5439e19" class="stentry">Log responses</td>
<td valign="top" headers="d5439e21" class="stentry">boolean </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">trackingUrlName</td>
<td valign="top" headers="d5439e19" class="stentry">Tracking URL name</td>
<td valign="top" headers="d5439e21" class="stentry">string </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">type</td>
<td valign="top" headers="d5439e19" class="stentry">Type</td>
<td valign="top" headers="d5439e21" class="stentry">enumeration (byte) </td>
<td valign="top" headers="d5439e23" class="stentry"><ul class="ul"><li class="li">Generic - generic - 0</li>
<li class="li">Unsubscription from a service - unsubscription - 3</li>
<li class="li">Blacklist - blackList - 4</li>
<li class="li">INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
<li class="li">Acquisition - acquisition - 1</li>
<li class="li">Subscription to a service - subscription - 2</li>
</ul>
</td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">uuid</td>
<td valign="top" headers="d5439e19" class="stentry">Security ID</td>
<td valign="top" headers="d5439e21" class="stentry">string </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e17" class="stentry">webTrackingEnabled</td>
<td valign="top" headers="d5439e19" class="stentry">Enable web tracking</td>
<td valign="top" headers="d5439e21" class="stentry">boolean </td>
<td valign="top" headers="d5439e23" class="stentry"> </td>
</tr>
</table>