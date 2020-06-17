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

# Profile (nms:recipient)

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
                  <td>age</td>
                  <td>Age</td>
                  <td>integer </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>appSubscription</td>
                  <td>Subscriptions to an application</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>birthDate</td>
                  <td>Date of birth</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blockList</td>
                  <td>No longer contact (by any channel)</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blockListEmail</td>
                  <td>No longer contact by email</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blockListFax</td>
                  <td>No longer contact by fax</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blockListMobile</td>
                  <td>No longer contact by SMS</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blockListPhone</td>
                  <td>No longer contact by phone</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blockListPostalMail</td>
                  <td>No longer contact by direct mail</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blockListPushnotification</td>
                  <td>No longer contact by push notification</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>country (countries)</td>
                  <td>Country</td>
                  <td>link </td>
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
                  <td>cryptedId</td>
                  <td>Encrypted ID</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cusHobbieslink (cusHobbies)</td>
                  <td>CusHobbieslink</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cusLastTransactionDate</td>
                  <td>Last Transaction Date</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cusTransactionslink</td>
                  <td>Transactions</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>domain</td>
                  <td>Email domain</td>
                  <td>string (255)</td>
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
                  <td>emailStatus (addressStatus)</td>
                  <td>Info about the email</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>excludeLogs</td>
                  <td>Exclusion logs</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>externalId</td>
                  <td>External Resource ID</td>
                  <td>string(100) </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>fax</td>
                  <td>Fax</td>
                  <td>string (32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>firstName</td>
                  <td>First name</td>
                  <td>string (30)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>gender</td>
                  <td>Gender</td>
                  <td>enumeration (byte) </td>
                  <td>
                     <ul>
                        <li>Unspecified - unknown - 0</li>
                        <li>Male - male - 1</li>
                        <li>Female - female - 2</li>
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
                  <td>lastModified</td>
                  <td>Last modified</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>lastName</td>
                  <td>Last name</td>
                  <td>string (50)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>location</td>
                  <td>Location</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>logs</td>
                  <td>Delivery logs</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>middleName</td>
                  <td>Middle name</td>
                  <td>string (30)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mobilePhone</td>
                  <td>Mobile</td>
                  <td>string (32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>modifiedBy (userBase)</td>
                  <td>Modified by</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>phone</td>
                  <td>Phone</td>
                  <td>string (32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>places</td>
                  <td>Locations</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>postalAddress</td>
                  <td>Postal address</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>salutation</td>
                  <td>Title</td>
                  <td>string (20)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>stateLink (state)</td>
                  <td>State</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subHisto</td>
                  <td>Subscription history</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subscriptions</td>
                  <td>Subscriptions</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>thumbnail</td>
                  <td>Thumbnail</td>
                  <td>string (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>timeZone</td>
                  <td>Time zone</td>
                  <td>enumeration (string) (64)</td>
                  <td>
                     <ul>
                        <li>(GMT-02:00) Central-Atlantic - Atlantic_South_Georgia - Atlantic/South_Georgia</li>
                        <li>(GMT+02:00) Amman - Asia_Amman - Asia/Amman</li>
                        <li>(GMT-03:00) Brasi - America_Sao_Paulo - America/Sao_Paulo</li>
                        <li>(GMT+06:00) Astana, Dhaka - Asia_Dhaka - Asia/Dhaka</li>
                        <li>(GMT+06:00) Novossibirsk - Asia_Novosibirsk - Asia/Novosibirsk</li>
                        <li>(GMT+02:00) Windhoek - Africa_Windhoek - Africa/Windhoek</li>
                        <li>(GMT+04:00) Caucasus, Erevan - Asia_Yerevan - Asia/Yerevan</li>
                        <li>(GMT-04:00) Manaus - America_Manaus - America/Manaus</li>
                        <li>(GMT+03:30) Teheran - Asia_Tehran - Asia/Tehran</li>
                        <li>(GMT+12:00) Auckland, Wellington - Pacific_Auckland - Pacific/Auckland</li>
                        <li>(GMT+02:00) Jerusalem - Asia_Jerusalem - Asia/Jerusalem</li>
                        <li>(GMT+03:00) Moscow, St. Petersburg, Volgograd - Europe_Moscow - Europe/Moscow</li>
                        <li>(GMT+09:30) Adelaïde - Australia_Adelaide - Australia/Adelaide</li>
                        <li>(GMT+10:00) Canberra, Melbourne, Sydney - Australia_Canberra - Australia/Canberra</li>
                        <li>(GMT+08:00) Perth - Australia_Perth - Australia/Perth</li>
                        <li>(GMT+09:00) Yakoutsk - Asia_Yakutsk - Asia/Yakutsk</li>
                        <li>(GMT-10:00) Hawai - Pacific_Honolulu - Pacific/Honolulu</li>
                        <li>(GMT+04:00) Baku - Asia_Baku - Asia/Baku</li>
                        <li>(GMT+10:00) Vladivostok - Asia_Vladivostok - Asia/Vladivostok</li>
                        <li>(GMT+09:00) Seoul - Asia_Seoul - Asia/Seoul</li>
                        <li>(GMT+01:00) Sarajevo, Skoplje, Sofia, Warsaw, Zagreb - Europe_Sarajevo - Europe/Sarajevo</li>
                        <li>(GMT+04:00) Abu Dhabi, Muscat - Asia_Muscat - Asia/Muscat</li>
                        <li>(GMT+08:00) Kuala Lumpur, Singapore - Asia_Kuala_Lumpur - Asia/Kuala_Lumpur</li>
                        <li>(GMT+09:00) Osaka, Sapporo, Tokyo - Asia_Tokyo - Asia/Tokyo</li>
                        <li>(GMT+10:00) Brisbane - Australia_Brisbane - Australia/Brisbane</li>
                        <li>(GMT+05:30) Sri Jayawardenepura - Asia_Colombo - Asia/Colombo</li>
                        <li>(GMT+02:00) Harare, Pretoria - Africa_Harare - Africa/Harare</li>
                        <li>(GMT+08:00) Oulan-Bator - Asia_Ulan_Bator - Asia/Ulan_Bator</li>
                        <li>(GMT-02:00) Greenwich Mean Time minus 2 hours - Gmt_m2 - Etc/GMT+2</li>
                        <li>(GMT-03:00) Greenwich Mean Time minus 3 hours - Gmt_m3 - Etc/GMT+3</li>
                        <li>(GMT-01:00) Greenwich Mean Time minus 1 hour - Gmt_m1 - Etc/GMT+1</li>
                        <li>(GMT-06:00) Greenwich Mean Time minus 6 hours - Gmt_m6 - Etc/GMT+6</li>
                        <li>(GMT-07:00) Greenwich Mean Time minus 7 hours - Gmt_m7 - Etc/GMT+7</li>
                        <li>(GMT-04:00) Greenwich Mean Time minus 4 hours - Gmt_m4 - Etc/GMT+4</li>
                        <li>(GMT) Casablanca - Africa_Casablanca - Africa/Casablanca</li>
                        <li>(GMT+05:30) Kolkata, Chennai, Mumbai, New Delhi - Asia_Kolkata - Asia/Kolkata</li>
                        <li>(GMT-11:00) Greenwich Mean Time minus 11 hours - Gmt_m11 - Etc/GMT+11</li>
                        <li>(GMT-09:00) Greenwich Mean Time minus 9 hours - Gmt_m9 - Etc/GMT+9</li>
                        <li>(GMT-03:30) Newfoundland - America_St_Johns - America/St_Johns</li>
                        <li>(GMT+03:00) Greenwich Mean Time plus 3 hours - Gmt_p3 - Etc/GMT-3</li>
                        <li>(GMT-04:30) Caracas - America_Caracas - America/Caracas</li>
                        <li>(GMT+01:00) Amsterdam, Berlin, Berne, Rome, Stockholm, Vienna - Europe_Berlin - Europe/Berlin</li>
                        <li>(GMT-07:00) Chihuahua, La Paz, Mazatlan - America_Chihuahua - America/Chihuahua</li>
                        <li>(GMT+03:00) Nairobi - Africa_Nairobi - Africa/Nairobi</li>
                        <li>(GMT-04:00) Asunción - America_Asuncion - America/Asuncion</li>
                        <li>(GMT+03:00) Bagdad - Asia_Baghdad - Asia/Baghdad</li>
                        <li>(GMT-10:00) Greenwich Mean Time minus 10 hours - Gmt_m10 - Etc/GMT+10</li>
                        <li>(GMT-03:00) Greenland - America_Godthab - America/Godthab</li>
                        <li>(GMT+02:00) Damas - Asia_Damascus - Asia/Damascus</li>
                        <li>(GMT-11:00) Samoa - Pacific_Samoa - Pacific/Samoa</li>
                        <li>(GMT-05:00) Bogota, Lima, Quito - America_Bogota - America/Bogota</li>
                        <li>(GMT+01:00) Brussels, Copenhagen, Madrid, Paris - Europe_Paris - Europe/Paris</li>
                        <li>(GMT+08:00) Beijing, Chongqing, Hong Kong, Urumqi - Asia_Shanghai - Asia/Shanghai</li>
                        <li>(GMT+12:00) Fidji - Pacific_Fiji - Pacific/Fiji</li>
                        <li>(GMT+02:00) Athens, Istanbul, Minsk - Europe_Athens - Europe/Athens</li>
                        <li>(GMT+04:00) Tbilissi - Asia_Tbilisi - Asia/Tbilisi</li>
                        <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
                        <li>(GMT+05:45) Katmandu - Asia_Katmandu - Asia/Katmandu</li>
                        <li>(GMT-05:00) Indiana (East) - America_Indianapolis - America/Indianapolis</li>
                        <li>(GMT-01:00) Cape Verde islands - Atlantic_Cape_Verde - Atlantic/Cape_Verde</li>
                        <li>(GMT+04:00) Port Louis - Indian_Mauritius - Indian/Mauritius</li>
                        <li>(GMT+08:00) Taipei - Asia_Taipei - Asia/Taipei</li>
                        <li>(GMT+06:30) Rangoon - Asia_Rangoon - Asia/Rangoon</li>
                        <li>(GMT+11:00) Magadan, The Solomon Islands, New Caledonia - Pacific_Guadalcanal - Pacific/Guadalcanal</li>
                        <li>(GMT+02:00) Cairo - Africa_Cairo - Africa/Cairo</li>
                        <li>(GMT+05:00) Iekaterinburg - Asia_Yekaterinburg - Asia/Yekaterinburg</li>
                        <li>(GMT+08:00) Irkoutsk - Asia_Irkutsk - Asia/Irkutsk</li>
                        <li>(GMT+10:00) Guam, Port Moresby - Pacific_Guam - Pacific/Guam</li>
                        <li>(GMT-04:00) Atlantic Standard Time (Canada) - America_Halifax - America/Halifax</li>
                        <li>(GMT) Greenwich mean time - GMT - GMT</li>
                        <li>Default - none - none</li>
                        <li>(GMT-04:00) La Paz - America_La_Paz - America/La_Paz</li>
                        <li>(GMT-06:00) Guadalajara, Mexico, Monterrey - America_Mexico_City - America/Mexico_City</li>
                        <li>(GMT+09:30) Darwin - Australia_Darwin - Australia/Darwin</li>
                        <li>(GMT-05:00) Est (United States and Canada) - America_New_York - America/New_York</li>
                        <li>(GMT-05:00) Greenwich Mean Time minus 5 hours - Gmt_m5 - Etc/GMT+5</li>
                        <li>(GMT+05:00) Islamabad, Karachi, Tachkent - Asia_Karachi - Asia/Karachi</li>
                        <li>(GMT+03:00) Koweït, Riyad - Asia_Riyadh - Asia/Riyadh</li>
                        <li>(GMT-08:00) Greenwich Mean Time minus 8 hours - Gmt_m8 - Etc/GMT+8</li>
                        <li>(GMT-01:00) The Azores - Atlantic_Azores - Atlantic/Azores</li>
                        <li>(GMT+07:00) Bangkok, Hanoi, Djakarta - Asia_Bangkok - Asia/Bangkok</li>
                        <li>(GMT) Monrovia - Africa_Monrovia - Africa/Monrovia</li>
                        <li>(GMT-09:00) Alaska - America_Anchorage - America/Anchorage</li>
                        <li>(GMT+01:00) Belgrade, Bratislava, Budapest, Ljubljana, Prague - Europe_Belgrade - Europe/Belgrade</li>
                        <li>(GMT) Reykjavik - Atlantic_Reykjavik - Atlantic/Reykjavik</li>
                        <li>(GMT+02:00) Bucarest - Europe_Bucharest - Europe/Bucharest</li>
                        <li>(GMT+05:00) Greenwich Mean Time plus 5 hours - Gmt_p5 - Etc/GMT-5</li>
                        <li>(GMT+04:00) Greenwich Mean Time plus 4 hours - Gmt_p4 - Etc/GMT-4</li>
                        <li>(GMT+07:00) Greenwich Mean Time plus 7 hours - Gmt_p7 - Etc/GMT-7</li>
                        <li>(GMT+06:00) Greenwich Mean Time plus 6 hours - Gmt_p6 - Etc/GMT-6</li>
                        <li>(GMT+01:00) Greenwich Mean Time plus 1 hour - Gmt_p1 - Etc/GMT-1</li>
                        <li>(GMT-08:00) Pacific (United States and Canada) - America_Los_Angeles - America/Los_Angeles</li>
                        <li>(GMT+02:00) Greenwich Mean Time plus 2 hours - Gmt_p2 - Etc/GMT-2</li>
                        <li>(GMT+07:00) Krasnoïarsk - Asia_Krasnoyarsk - Asia/Krasnoyarsk</li>
                        <li>(GMT+09:00) Greenwich Mean Time plus 9 hours - Gmt_p9 - Etc/GMT-9</li>
                        <li>(GMT+08:00) Greenwich Mean Time plus 8 hours - Gmt_p8 - Etc/GMT-8</li>
                        <li>(GMT+10:00) Hobart - Australia_Hobart - Australia/Hobart</li>
                        <li>(GMT+13:00) Nuku'alofa - Pacific_Tongatapu - Pacific/Tongatapu</li>
                        <li>(GMT-06:00) Central America - America_Regina - America/Regina</li>
                        <li>(GMT-03:00) Buenos Aires, Cayenne, Fortaleza - America_Buenos_Aires - America/Buenos_Aires</li>
                        <li>(GMT-07:00) Rocky Mountains (United States and Canada) - America_Denver - America/Denver</li>
                        <li>(GMT+01:00) Central Africa - West - Africa_Luanda - Africa/Luanda</li>
                        <li>(GMT+02:00) Helsinki, Kiev, Riga, Sofia, Tallinn, Vilnius - Europe_Helsinki - Europe/Helsinki</li>
                        <li>(GMT) Greenwich Mean Time: Dublin, Edinburgh, Lisbon, London - Europe_London - Europe/London</li>
                        <li>(GMT-07:00) Arizona - America_Phoenix - America/Phoenix</li>
                        <li>(GMT+02:00) Beirut - Asia_Beirut - Asia/Beirut</li>
                        <li>(GMT+04:30) Kabul - Asia_Kabul - Asia/Kabul</li>
                        <li>(GMT-06:00) Center (United States and Canada) - America_Chicago - America/Chicago</li>
                        <li>(GMT+11:00) Greenwich Mean Time plus 11 hours - Gmt_p11 - Etc/GMT-11</li>
                        <li>(GMT+10:00) Greenwich Mean Time plus 10 hours - Gmt_p10 - Etc/GMT-10</li>
                        <li>(GMT+13:00) Greenwich Mean Time plus 13 hours - Gmt_p13 - Etc/GMT-13</li>
                        <li>(GMT+12:00) Greenwich Mean Time plus 12 hours - Gmt_p12 - Etc/GMT-12</li>
                        <li>(GMT-04:00) Santiago - America_Santiago - America/Santiago</li>
                        <li>(GMT-03:00) Montevideo - America_Montevideo - America/Montevideo</li>
                        <li>(GMT-04:00) Cuiaba - America_Cuiaba - America/Cuiaba</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>title</td>
                  <td>Profile</td>
                  <td>string (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>tracking</td>
                  <td>Tracking logs</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
            </table>


## Filters


Birthday (birthday)

<table>
<tr>
<th>Name</th>
<th>Type</th>
</tr>
<tr>
<td>includeStart</td>
<td>boolean</td>
</tr>
<tr>
<td>previousUnitsValue</td>
<td>integer</td>
</tr>
<tr>
<td>nextUnitsValue</td>
<td>integer</td>
</tr>
<tr>
<td>endDay</td>
<td>date</td>
</tr>
<tr>
<td>precision</td>
<td>enumeration</td>
</tr>
<tr>
<td>relativeValue</td>
<td>string</td>
</tr>
<tr>
<td>month</td>
<td>date</td>
</tr>
<tr>
<td>operator</td>
<td>enumeration</td>
</tr>
<tr>
<td>includeEnd</td>
<td>boolean</td>
</tr>
<tr>
<td>endMonth</td>
<td>date</td>
</tr>
<tr>
<td>type</td>
<td>enumeration</td>
</tr>
<tr>
<td>day</td>
<td>date</td>
</tr>
</table>

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

By keys (byKeysProfile)

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

By name or email (byText)

<table>
<tr>
<th>Name</th>
<th>Type</th>
</tr>
<tr>
<td>text</td>
<td>string</td>
</tr>
</table>

By static audience (byStaticAudience)

<table>
<tr>
<th>Name</th>
<th>Type</th>
</tr>
<tr>
<td>audience</td>
<td>link</td>
</tr>
</table>

Clicked (hasClickedDelivery)

<table>
<tr>
<th>Name</th>
<th>Type</th>
</tr>
<tr>
<td>delivery</td>
<td>link</td>
</tr>
</table>

Opened (hasOpenedDelivery)

<table>
<tr>
<th>Name</th>
<th>Type</th>
</tr>
<tr>
<td>delivery</td>
<td>link</td>
</tr>
</table>

Profile (profile)

<table>
<tr>
<th>Name</th>
<th>Type</th>
</tr>
<tr>
<td>profile</td>
<td>link</td>
</tr>
</table>

Received (hasReceivedDelivery)

<table>
<tr>
<th>Name</th>
<th>Type</th>
</tr>
<tr>
<td>delivery</td>
<td>link</td>
</tr>
</table>

Subscribers (subscribers)

<table>
<tr>
<th>Name</th>
<th>Type</th>
</tr>
<tr>
<td>service</td>
<td>link</td>
</tr>
</table>