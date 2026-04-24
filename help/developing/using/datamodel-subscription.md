---
title: DataModel Subscription Event
description: Learn about the datamodel
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: cf0fac4e-59fd-4d6e-a411-41361f45938d
TQID: https://experienceleague.adobe.com/XssYu0sntbeCRq1uNe6MhztLtISXoJiOefIOnjqIaoQ
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Subscription Event (nms:rtEvent)

## Object description

<table>
    <tr>
        <th>Name</th>
        <th>Label</th>
        <th>Type (length)</th>
        <th>Enumeration values</th>
    </tr>
    <tr>
        <td>PKey</td>
        <td>Main resource ID</td>
        <td>string </td>
        <td> </td>
    </tr>
    <tr>
        <td>ctx</td>
        <td>Event context</td>
        <td>item </td>
        <td> </td>
    </tr>
    <tr>
        <td>email</td>
        <td>Email</td>
        <td>string (128)</td>
        <td> </td>
    </tr>
    <tr>
        <td>emailFormat</td>
        <td>Email format</td>
        <td>enumeration (byte) </td>
        <td>
            <ul>
            <li>Text - text - 1</li>
            <li>HTML - html - 2</li>
            <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
            <li>Unknown - unknown - 0</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>eventHistoId</td>
        <td>Archived event ID</td>
        <td>integer </td>
        <td> </td>
    </tr>
    <tr>
        <td>mobilePhone</td>
        <td>Mobile number</td>
        <td>string (32)</td>
        <td> </td>
    </tr>
    <tr>
        <td>serverUrl</td>
        <td>ServerUrl</td>
        <td>string </td>
        <td> </td>
    </tr>
</table>

## Filters

By email (byEmail)

<table>
    <tr>
    <th>Name</th>
    <th>Type</th>
    </tr>
    <tr>
    <td>email</td>
    <td>string</td>
    </tr>
</table>

By status or type (byStatusOrType)

<table>
        <tr>
        <th>Name</th>
        <th>Type</th>
        </tr>
        <tr>
        <td>status</td>
        <td>enumeration</td>
        </tr>
        <tr>
        <td>type</td>
        <td>string</td>
        </tr>
    </table>
