---
title: DataModel
description: Learn about the datamodel
uuid: 99277e46-e4f7-49a9-ba27-b878780f90da
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
discoiquuid: 6e21db35-daf9-4edb-977a-6ef606db0e4d
internal: n
snippet: y
---

# Delivery (nms:delivery)

## Object description

<table>
               <tr>
                  <th>Name</th>
                  <th>Label</th>
                  <th>Type (length)</th>
                  <th>Enumeration values</th>
               </tr>
               <tr>
                  <td>FCP</td>
                  <td>Proof</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>PKey</td>
                  <td>Main resource ID</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>abTesting</td>
                  <td>A/B Testing</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>advanced</td>
                  <td>Advanced delivery</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>advancedParameters</td>
                  <td>Advanced parameters</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>aemContents</td>
                  <td>Adobe Experience Manager contents</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>alertMessage</td>
                  <td>Warning message</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>alertMode</td>
                  <td>Warning type</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>attachment</td>
                  <td>Attached files</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>branding (brandingBase)</td>
                  <td>Brand</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>broadLogs</td>
                  <td>Delivery logs</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>builtIn</td>
                  <td>Built-in application object</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>campaign (campaignBase)</td>
                  <td>Campaign</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cmsAccount (extAccountAEMBase)</td>
                  <td>Adobe Experience Manager account</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>commands</td>
                  <td>Commands</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>content</td>
                  <td>Content</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>contentSource</td>
                  <td>Content source</td>
                  <td>enumeration (byte) </td>
                  <td>
                     <ul>
                        <li>Adobe Experience Manager - aem - 1</li>
                        <li>Adobe Campaign - campaign - 0</li>
                        <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>contextResourceType</td>
                  <td>Resource type</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>created</td>
                  <td>Created</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>createdBy (userBase)</td>
                  <td>Created by</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>deliveryMode</td>
                  <td>Delivery mode</td>
                  <td>enumeration (byte) </td>
                  <td>
                     <ul>
                        <li>Bulk delivery - bulk - 1</li>
                        <li>Mid-sourcing - midSourcing - 4</li>
                        <li>Description - descriptive - 2</li>
                        <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
                        <li>External - external - 0</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>deliveryProvider (extAccountBase)</td>
                  <td>Routing</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>desc</td>
                  <td>Description</td>
                  <td>string (512)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>emailPreview</td>
                  <td>Email preview</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>excludeLogs</td>
                  <td>Exclusion logs</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>exclusions</td>
                  <td>Exclusion causes</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>execution</td>
                  <td>Delivery execution parameters</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>executionType</td>
                  <td>Execution type</td>
                  <td>enumeration (byte) </td>
                  <td>
                     <ul>
                        <li>Unique - oneTime - 0</li>
                        <li>Continuous - continuous - 1</li>
                        <li>Message Center - messageCenter - 2</li>
                        <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>forecastLogs</td>
                  <td>ForecastLog</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>geoUnit (geoUnitBase)</td>
                  <td>Geographical unit</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>hasAttachments</td>
                  <td>Add attached files</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>icon</td>
                  <td>Icon</td>
                  <td>enumeration (byte) </td>
                  <td>
                     <ul>
                        <li>Transactional email - emailLightning - 60</li>
                        <li>Fax - fax - 4</li>
                        <li>Mobile (SMS) - sms - 1</li>
                        <li>Recurring email - emailRefresh - 30</li>
                        <li>Direct mail - paper - 3</li>
                        <li>Phone - phone - 2</li>
                        <li>Other - other - 120</li>
                        <li>Recurring SMS - smsRefresh - 31</li>
                        <li>Mobile application - pushNotification - 40</li>
                        <li>Transactional SMS - smsLightning - 61</li>
                        <li>Email - email - 0</li>
                        <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>isExternal</td>
                  <td>Is external resource</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isMaster</td>
                  <td>Master</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isTemplate</td>
                  <td>Template</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>iterations</td>
                  <td>Deliveries</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>job</td>
                  <td>Job</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>jobLogs</td>
                  <td>Logs</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>kpis</td>
                  <td>Indicators</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>label</td>
                  <td>Label</td>
                  <td>string (128)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>lastModified</td>
                  <td>Last modified</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>logicalStatus</td>
                  <td>Execution status</td>
                  <td>enumeration (string) (255)</td>
                  <td>
                     <ul>
                        <li>In progress - started - started</li>
                        <li>Editing - edition - edition</li>
                        <li>Finished - finished - finished</li>
                        <li>Warning - warning - warning</li>
                        <li>Erroneous - error - error</li>
                        <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>mailParameters</td>
                  <td>Email header parameters</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mainDate</td>
                  <td>Date</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mapping (deliveryMapping)</td>
                  <td>Target mapping</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>master (deliveryBase)</td>
                  <td>Master instance</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>masterKpis</td>
                  <td>Master indicators</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>messageType</td>
                  <td>Channel</td>
                  <td>enumeration (byte) </td>
                  <td>
                     <ul>
                        <li>Fax - fax - 4</li>
                        <li>Mobile (SMS) - sms - 1</li>
                        <li>Email - email - 0</li>
                        <li>Phone - phone - 2</li>
                        <li>Direct mail - paper - 3</li>
                        <li>Mobile application - pushNotification - 40</li>
                        <li>Other - other - 120</li>
                        <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>modifiedBy (userBase)</td>
                  <td>Modified by</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>name</td>
                  <td>ID</td>
                  <td>string (64)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>offerManagement</td>
                  <td>Offer Management</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>orgUnit (orgUnitBase)</td>
                  <td>Organizational unit</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>parent (deliveryBase)</td>
                  <td>Parent delivery</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>priority</td>
                  <td>Delivery priority</td>
                  <td>enumeration (byte) </td>
                  <td>
                     <ul>
                        <li>High - high - 20</li>
                        <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
                        <li>Normal - normal - 10</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>program (programBase)</td>
                  <td>Program</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>proofs</td>
                  <td>Proofs</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>pushNotificationPreview</td>
                  <td>Push notification preview</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>pushnotificationParameters</td>
                  <td>PushNotification parameters</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>realtimeReport</td>
                  <td>Realtime Reports</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>resourceVersion</td>
                  <td>Resource version</td>
                  <td>string (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>ribbonMessage</td>
                  <td>Ribbon message</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>scenario</td>
                  <td>Delivery template parameters</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>scheduling</td>
                  <td>Delivery scheduling</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>smsParameters</td>
                  <td>SMS parameters</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>smsPreview</td>
                  <td>SMS preview</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>state</td>
                  <td>Status</td>
                  <td>enumeration (byte) </td>
                  <td>
                     <ul>
                        <li>Start pending - startPending - 51</li>
                        <li>Ready to be delivered - ready - 45</li>
                        <li>Retry pending - retryPending - 61</li>
                        <li>Retry in progress - retryInProgress - 62</li>
                        <li>Failed - failed - 87</li>
                        <li>In progress - started - 55</li>
                        <li>Targeting pending - targetPrepPending - 11</li>
                        <li>Personalization pending - messagePrepPending - 21</li>
                        <li>Paused - paused - 75</li>
                        <li>Editing - edition - 0</li>
                        <li>Finished - finished - 95</li>
                        <li>Counting in progress - targetSelection - 12</li>
                        <li>Message finalized - messageReady - 25</li>
                        <li>Personalization or count failed - preparationError - 37</li>
                        <li>Stopped - cancelled - 85</li>
                        <li>Personalization in progress - messagePreparation - 22</li>
                        <li>Target ready - targetReady - 15</li>
                        <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
                        <li>Arbitration in progress - targetArbitration - 13</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>targets</td>
                  <td>Delivery target population</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>template (deliveryTemplateSummary)</td>
                  <td>Delivery template</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>thumbnail</td>
                  <td>Delivery thumbnail</td>
                  <td>string (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>title</td>
                  <td>Delivery</td>
                  <td>string (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>tracking</td>
                  <td>Tracking parameters</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>trackingLogs</td>
                  <td>Tracking logs</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>trackingUrls</td>
                  <td>Tracked URLs</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>triggerMessage</td>
                  <td>Parameters of the transactional message</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>typology (typologyBase)</td>
                  <td>Typology</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>workflow (workflowBase)</td>
                  <td>Targeting workflow</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>workflowStatus</td>
                  <td>Workflow status</td>
                  <td>enumeration (string) (255)</td>
                  <td>
                     <ul>
                        <li>In progress - started - started</li>
                        <li>Editing - edition - edition</li>
                        <li>Finished - finished - finished</li>
                        <li>Warning - warning - warning</li>
                        <li>Erroneous - error - error</li>
                        <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
            </table>

## Filters

By channel type (byChannel)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>channel</td>
    <td>enumeration</td>
    </tr>
</table>

By execution type (byExecutionType)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>executionType</td>
    <td>enumeration</td>
    </tr>
</table>

By logical status (byLogicalStatus)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>state</td>
    <td>enumeration</td>
    </tr>
</table>

By name or label (byText)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>text</td>
    <td>string</td>
    </tr>
    <tr>
    <td>mc</td>
    <td>string</td>
    </tr>
</table>

By period (byPeriod)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>timePeriod</td>
    <td>string</td>
    </tr>
</table>

By period (byStartPeriod)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>startDate</td>
    <td>date</td>
    </tr>
    <tr>
    <td>timePeriod</td>
    <td>string</td>
    </tr>
</table>

By publication status (byPublicationStatus)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>pStatus</td>
    <td>enumeration</td>
    </tr>
</table>

By status (byState)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>state</td>
    <td>enumeration</td>
    </tr>
</table>

Follow-up messages (showFollowup)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>followup</td>
    <td>boolean</td>
    </tr>
</table>

Include advanced deliveries (withAdvanced)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>advanced</td>
    <td>boolean</td>
    </tr>
</table>

Include continuous deliveries from a heterogeneous list (withContinuous)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>withContinuous</td>
    <td>boolean</td>
    </tr>
</table>

Include proofs (withFCP)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>withFCP</td>
    <td>boolean</td>
    </tr>
</table>

Planned during the given period (byPlanning)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>startDate</td>
    <td>date</td>
    </tr>
    <tr>
    <td>endDate</td>
    <td>date</td>
    </tr>
</table>

Present during given period (byCalendar)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>startDate</td>
    <td>date</td>
    </tr>
    <tr>
    <td>endDate</td>
    <td>date</td>
    </tr>
</table>

Show out-of-the-box (showOob)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>oob</td>
    <td>boolean</td>
    </tr>
</table>