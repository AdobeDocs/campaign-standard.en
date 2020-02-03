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

# Unsubscription Event (nms:rtEvent)

## Object description

<table>
               <tr>
                  <th>Name</th>
                  <th>Read Only</th>
                  <th>Type</th>
                  <th>Required</th>
               </tr>
               <tr>
                  <td>PKey</td>
                  <td>False</td>
                  <td>string</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>ctx</td>
                  <td>False</td>
                  <td>item</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>email</td>
                  <td>False</td>
                  <td>string</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>emailFormat</td>
                  <td>False</td>
                  <td>enumeration</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>mobilePhone</td>
                  <td>False</td>
                  <td>string</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>serverUrl</td>
                  <td>True</td>
                  <td>string</td>
                  <td>False</td>
               </tr>
            </table>

## Filters

byEmail

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

byStatusOrType

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