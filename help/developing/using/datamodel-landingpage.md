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

# landingPage (nms:landingPage)

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
         <td>additionalData</td>
         <td>Additional data</td>
         <td>collection </td>
         <td> </td>
      </tr>
      <tr>
         <td>additionalLanguages</td>
         <td>Other languages</td>
         <td>item </td>
         <td> </td>
      </tr>
      <tr>
         <td>allowNonIdentifiedTarget</td>
         <td>Authorize unidentified visitors</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>branding (brandingBase)</td>
         <td>Brand</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>builtIn</td>
         <td>Built-in application object</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>cache</td>
         <td>Cache</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>campaign (campaignBase)</td>
         <td>Campaign</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>closedLog</td>
         <td>'Landing page closed' log</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>contextResourceType</td>
         <td>ContextResourceType</td>
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
         <td>cryptKey</td>
         <td>AES encryption key</td>
         <td>string (64)</td>
         <td> </td>
      </tr>
      <tr>
         <td>defaultLanguage</td>
         <td>Default language</td>
         <td>enumeration (string) (255)</td>
         <td>
            <ul>
               <li>Greek - el - el</li>
               <li>English - en - en</li>
               <li>Chinese - zh - zh</li>
               <li>French (France) - fr_FR - fr_FR</li>
               <li>Vietnamese - vi - vi</li>
               <li>Portuguese (Portugal) - pt_PT - pt_PT</li>
               <li>Italian (Italy) - it_IT - it_IT</li>
               <li>Italian - it - it</li>
               <li>Dutch (Belgium) - nl_BE - nl_BE</li>
               <li>Norwegian (Norway) - no_NO - no_NO</li>
               <li>Dutch (Netherlands) - nl_NL - nl_NL</li>
               <li>Arabic - ar - ar</li>
               <li>English (United States) - en_US - en_US</li>
               <li>Irish - ga - ga</li>
               <li>Czech - cs - cs</li>
               <li>Estonian - et - et</li>
               <li>Indonesian - id - id</li>
               <li>Spanish - es - es</li>
               <li>Russian - ru - ru</li>
               <li>Dutch - nl - nl</li>
               <li>Walloon - wa - wa</li>
               <li>Portuguese - pt - pt</li>
               <li>French (Belgium) - fr_BE - fr_BE</li>
               <li>Latvian - lv - lv</li>
               <li>Lithuanian - lt - lt</li>
               <li>Thai - th - th</li>
               <li>English (United Kingdom) - en_GB - en_GB</li>
               <li>French - fr - fr</li>
               <li>Portuguese (Brazil) - pt_BR - pt_BR</li>
               <li>German - de - de</li>
               <li>Danish - da - da</li>
               <li>Finnish - fi - fi</li>
               <li>Hungarian - hu - hu</li>
               <li>Swedish (Finland) - sv_FI - sv_FI</li>
               <li>Japanese - ja - ja</li>
               <li>Hebrew - he - he</li>
               <li>Korean - ko - ko</li>
               <li>Swedish - sv - sv</li>
               <li>Sweden (Swedish) - sv_SE - sv_SE</li>
               <li>Slovak - sk - sk</li>
               <li>Maltese - mt - mt</li>
               <li>Italian (Switzerland) - it_CH - it_CH</li>
               <li>Polish - pl - pl</li>
               <li>Slovene - sl - sl</li>
               <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>defaultOrigin (delivery)</td>
         <td>Traffic source</td>
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
         <td>designLanguage</td>
         <td>Design language</td>
         <td>enumeration (string) (255)</td>
         <td>
            <ul>
               <li>Greek - el - el</li>
               <li>English - en - en</li>
               <li>Chinese - zh - zh</li>
               <li>French (France) - fr_FR - fr_FR</li>
               <li>Vietnamese - vi - vi</li>
               <li>Portuguese (Portugal) - pt_PT - pt_PT</li>
               <li>Italian (Italy) - it_IT - it_IT</li>
               <li>Italian - it - it</li>
               <li>Dutch (Belgium) - nl_BE - nl_BE</li>
               <li>Norwegian (Norway) - no_NO - no_NO</li>
               <li>Dutch (Netherlands) - nl_NL - nl_NL</li>
               <li>Arabic - ar - ar</li>
               <li>English (United States) - en_US - en_US</li>
               <li>Irish - ga - ga</li>
               <li>Czech - cs - cs</li>
               <li>Estonian - et - et</li>
               <li>Indonesian - id - id</li>
               <li>Spanish - es - es</li>
               <li>Russian - ru - ru</li>
               <li>Dutch - nl - nl</li>
               <li>Walloon - wa - wa</li>
               <li>Portuguese - pt - pt</li>
               <li>French (Belgium) - fr_BE - fr_BE</li>
               <li>Latvian - lv - lv</li>
               <li>Lithuanian - lt - lt</li>
               <li>Thai - th - th</li>
               <li>English (United Kingdom) - en_GB - en_GB</li>
               <li>French - fr - fr</li>
               <li>Portuguese (Brazil) - pt_BR - pt_BR</li>
               <li>German - de - de</li>
               <li>Danish - da - da</li>
               <li>Finnish - fi - fi</li>
               <li>Hungarian - hu - hu</li>
               <li>Swedish (Finland) - sv_FI - sv_FI</li>
               <li>Japanese - ja - ja</li>
               <li>Hebrew - he - he</li>
               <li>Korean - ko - ko</li>
               <li>Swedish - sv - sv</li>
               <li>Sweden (Swedish) - sv_SE - sv_SE</li>
               <li>Slovak - sk - sk</li>
               <li>Maltese - mt - mt</li>
               <li>Italian (Switzerland) - it_CH - it_CH</li>
               <li>Polish - pl - pl</li>
               <li>Slovene - sl - sl</li>
               <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>dynamicService</td>
         <td>Dynamic service</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>end</td>
         <td>Expiration date</td>
         <td>date </td>
         <td> </td>
      </tr>
      <tr>
         <td>errorContextResourceType</td>
         <td>ErrorContextResourceType</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>errorPage</td>
         <td>Error page</td>
         <td>item </td>
         <td> </td>
      </tr>
      <tr>
         <td>geoUnit (geoUnitBase)</td>
         <td>Geographical unit</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>htmlPage</td>
         <td>Pages</td>
         <td>collection </td>
         <td> </td>
      </tr>
      <tr>
         <td>identificationByUrlParam</td>
         <td>Identification by URL parameters</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>inactiveUrlRedirection</td>
         <td>Redirection URL</td>
         <td>string (4096)</td>
         <td> </td>
      </tr>
      <tr>
         <td>isExternal</td>
         <td>Is external resource</td>
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
         <td>loadingFilter (queryFilterBase)</td>
         <td>Loading key</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>loadingFilterMapping</td>
         <td>Parameters of the loading key</td>
         <td>collection </td>
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
         <td>messageAction</td>
         <td>Start sending message</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>messageActionDelivery (deliveryMCTemplateBase)</td>
         <td>Transactional message</td>
         <td>link </td>
         <td> </td>
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
         <td>orgUnit (orgUnitBase)</td>
         <td>Organizational unit</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>prefill</td>
         <td>Preload visitor data</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>program (programBase)</td>
         <td>Program</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>publicUrl</td>
         <td>Public URL</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>publicationDate</td>
         <td>Publication date</td>
         <td>date </td>
         <td> </td>
      </tr>
      <tr>
         <td>reconciliationFilter (queryFilterBase)</td>
         <td>Reconciliation key</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>reconciliationFilterMapping</td>
         <td>Reconciliation key parameters</td>
         <td>collection </td>
         <td> </td>
      </tr>
      <tr>
         <td>reconciliationUpdateStrategy</td>
         <td>Update strategy</td>
         <td>enumeration (byte) </td>
         <td>
            <ul>
               <li>Update - updateTarget - 1</li>
               <li>Unauthorized - unauthorized - 0</li>
               <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>service (serviceBase)</td>
         <td>Subscription service</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>specificAction</td>
         <td>Specific action</td>
         <td>enumeration (byte) </td>
         <td>
            <ul>
               <li>Blacklist - blackList - 3</li>
               <li>No specific action - none - 0</li>
               <li>Unsubscription - unsubscription - 2</li>
               <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
               <li>Subscription - subscription - 1</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>start</td>
         <td>Deployment date</td>
         <td>date </td>
         <td> </td>
      </tr>
      <tr>
         <td>state</td>
         <td>Status</td>
         <td>enumeration (byte) </td>
         <td>
            <ul>
               <li>Editing - edit - 0</li>
               <li>Publishing failed - failed - 99</li>
               <li>Closed - closed - 20</li>
               <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
               <li>Online - opened - 10</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>targetResource</td>
         <td>Targeting dimension</td>
         <td>string (255)</td>
         <td> </td>
      </tr>
      <tr>
         <td>template (landingPage)</td>
         <td>Landing page template</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>testUrl</td>
         <td>Test URL</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>thumbnail</td>
         <td>Thumbnail</td>
         <td>string (255)</td>
         <td> </td>
      </tr>
      <tr>
         <td>timezone</td>
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
               <li>Server time zone - _server_ - _server_</li>
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
               <li>Default - _inherit_ - _inherit_</li>
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
               <li>Time zone of the database - _wdbc_ - _wdbc_</li>
               <li>(GMT+06:30) Rangoon - Asia_Rangoon - Asia/Rangoon</li>
               <li>(GMT+11:00) Magadan, The Solomon Islands, New Caledonia - Pacific_Guadalcanal - Pacific/Guadalcanal</li>
               <li>(GMT+02:00) Cairo - Africa_Cairo - Africa/Cairo</li>
               <li>(GMT+05:00) Iekaterinburg - Asia_Yekaterinburg - Asia/Yekaterinburg</li>
               <li>(GMT+08:00) Irkoutsk - Asia_Irkutsk - Asia/Irkutsk</li>
               <li>(GMT+10:00) Guam, Port Moresby - Pacific_Guam - Pacific/Guam</li>
               <li>(GMT-04:00) Atlantic Standard Time (Canada) - America_Halifax - America/Halifax</li>
               <li>(GMT) Greenwich mean time - GMT - GMT</li>
               <li>(GMT-04:00) La Paz - America_La_Paz - America/La_Paz</li>
               <li>Operator time zone - _login_ - _login_</li>
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
         <td>Landing page</td>
         <td>string (255)</td>
         <td> </td>
      </tr>
      <tr>
         <td>trackingEnabled</td>
         <td>Log responses</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>trackingUrlName</td>
         <td>Tracking URL name</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>type</td>
         <td>Type</td>
         <td>enumeration (byte) </td>
         <td>
            <ul>
               <li>Generic - generic - 0</li>
               <li>Unsubscription from a service - unsubscription - 3</li>
               <li>Blacklist - blackList - 4</li>
               <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
               <li>Acquisition - acquisition - 1</li>
               <li>Subscription to a service - subscription - 2</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>uuid</td>
         <td>Security ID</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>webTrackingEnabled</td>
         <td>Enable web tracking</td>
         <td>boolean </td>
         <td> </td>
      </tr>
   </table>

## Filters

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

By targeting resource (byTargetResource)

<table>
<tr>
<th>Name</th>
<th>Type</th>
</tr>
<tr>
<td>targetResource</td>
<td>string</td>
</tr>
</table>

Include advanced landing pages (withAdvanced)

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

Published during given period (byPlanning)

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
