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


# Landing Page - Datamodel


## Object Description

+-----------------+-----------------+-----------------+-----------------+
| Name            | Label           | Type (length)   | Enumeration     |
|                 |                 |                 | values          |
+=================+=================+=================+=================+
| PKey            | Main resource   | string          |                 |
|                 | ID              |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| additionalData  | Additional data | collection      |                 |
+-----------------+-----------------+-----------------+-----------------+
| additionalLangu | Other languages | item            |                 |
| ages            |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| allowNonIdentif | Authorize       | boolean         |                 |
| iedTarget       | unidentified    |                 |                 |
|                 | visitors        |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| branding        | Brand           | link            |                 |
| (brandingBase)  |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| builtIn         | Built-in        | boolean         |                 |
|                 | application     |                 |                 |
|                 | object          |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| cache           | Cache           | string          |                 |
+-----------------+-----------------+-----------------+-----------------+
| campaign        | Campaign        | link            |                 |
| (campaignBase)  |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| closedLog       | \'Landing page  | string          |                 |
|                 | closed\' log    |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| contextResource | ContextResource | string          |                 |
| Type            | Type            |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| created         | Created         | date            |                 |
+-----------------+-----------------+-----------------+-----------------+
| createdBy       | Created by      | link            |                 |
| (userBase)      |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| cryptKey        | AES encryption  | string (64)     |                 |
|                 | key             |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| defaultLanguage | Default         | enumeration     | -   Greek -     |
|                 | language        | (string) (255)  |     el - el     |
|                 |                 |                 | -   English -   |
|                 |                 |                 |     en - en     |
|                 |                 |                 | -   Chinese -   |
|                 |                 |                 |     zh - zh     |
|                 |                 |                 | -   French      |
|                 |                 |                 |     (France) -  |
|                 |                 |                 |     fr\_FR -    |
|                 |                 |                 |     fr\_FR      |
|                 |                 |                 | -   Vietnamese  |
|                 |                 |                 | -               |
|                 |                 |                 |     vi - vi     |
|                 |                 |                 | -   Portuguese  |
|                 |                 |                 |     (Portugal)  |
|                 |                 |                 | -               |
|                 |                 |                 |     pt\_PT -    |
|                 |                 |                 |     pt\_PT      |
|                 |                 |                 | -   Italian     |
|                 |                 |                 |     (Italy) -   |
|                 |                 |                 |     it\_IT -    |
|                 |                 |                 |     it\_IT      |
|                 |                 |                 | -   Italian -   |
|                 |                 |                 |     it - it     |
|                 |                 |                 | -   Dutch       |
|                 |                 |                 |     (Belgium) - |
|                 |                 |                 |     nl\_BE -    |
|                 |                 |                 |     nl\_BE      |
|                 |                 |                 | -   Norwegian   |
|                 |                 |                 |     (Norway) -  |
|                 |                 |                 |     no\_NO -    |
|                 |                 |                 |     no\_NO      |
|                 |                 |                 | -   Dutch       |
|                 |                 |                 |     (Netherland |
|                 |                 |                 | s) -            |
|                 |                 |                 |     nl\_NL -    |
|                 |                 |                 |     nl\_NL      |
|                 |                 |                 | -   Arabic -    |
|                 |                 |                 |     ar - ar     |
|                 |                 |                 | -   English     |
|                 |                 |                 |     (United     |
|                 |                 |                 |     States) -   |
|                 |                 |                 |     en\_US -    |
|                 |                 |                 |     en\_US      |
|                 |                 |                 | -   Irish -     |
|                 |                 |                 |     ga - ga     |
|                 |                 |                 | -   Czech -     |
|                 |                 |                 |     cs - cs     |
|                 |                 |                 | -   Estonian -  |
|                 |                 |                 |     et - et     |
|                 |                 |                 | -   Indonesian  |
|                 |                 |                 | -               |
|                 |                 |                 |     id - id     |
|                 |                 |                 | -   Spanish -   |
|                 |                 |                 |     es - es     |
|                 |                 |                 | -   Russian -   |
|                 |                 |                 |     ru - ru     |
|                 |                 |                 | -   Dutch -     |
|                 |                 |                 |     nl - nl     |
|                 |                 |                 | -   Walloon -   |
|                 |                 |                 |     wa - wa     |
|                 |                 |                 | -   Portuguese  |
|                 |                 |                 | -               |
|                 |                 |                 |     pt - pt     |
|                 |                 |                 | -   French      |
|                 |                 |                 |     (Belgium) - |
|                 |                 |                 |     fr\_BE -    |
|                 |                 |                 |     fr\_BE      |
|                 |                 |                 | -   Latvian -   |
|                 |                 |                 |     lv - lv     |
|                 |                 |                 | -   Lithuanian  |
|                 |                 |                 | -               |
|                 |                 |                 |     lt - lt     |
|                 |                 |                 | -   Thai - th - |
|                 |                 |                 |     th          |
|                 |                 |                 | -   English     |
|                 |                 |                 |     (United     |
|                 |                 |                 |     Kingdom) -  |
|                 |                 |                 |     en\_GB -    |
|                 |                 |                 |     en\_GB      |
|                 |                 |                 | -   French -    |
|                 |                 |                 |     fr - fr     |
|                 |                 |                 | -   Portuguese  |
|                 |                 |                 |     (Brazil) -  |
|                 |                 |                 |     pt\_BR -    |
|                 |                 |                 |     pt\_BR      |
|                 |                 |                 | -   German -    |
|                 |                 |                 |     de - de     |
|                 |                 |                 | -   Danish -    |
|                 |                 |                 |     da - da     |
|                 |                 |                 | -   Finnish -   |
|                 |                 |                 |     fi - fi     |
|                 |                 |                 | -   Hungarian - |
|                 |                 |                 |     hu - hu     |
|                 |                 |                 | -   Swedish     |
|                 |                 |                 |     (Finland) - |
|                 |                 |                 |     sv\_FI -    |
|                 |                 |                 |     sv\_FI      |
|                 |                 |                 | -   Japanese -  |
|                 |                 |                 |     ja - ja     |
|                 |                 |                 | -   Hebrew -    |
|                 |                 |                 |     he - he     |
|                 |                 |                 | -   Korean -    |
|                 |                 |                 |     ko - ko     |
|                 |                 |                 | -   Swedish -   |
|                 |                 |                 |     sv - sv     |
|                 |                 |                 | -   Sweden      |
|                 |                 |                 |     (Swedish) - |
|                 |                 |                 |     sv\_SE -    |
|                 |                 |                 |     sv\_SE      |
|                 |                 |                 | -   Slovak -    |
|                 |                 |                 |     sk - sk     |
|                 |                 |                 | -   Maltese -   |
|                 |                 |                 |     mt - mt     |
|                 |                 |                 | -   Italian     |
|                 |                 |                 |     (Switzerlan |
|                 |                 |                 | d) -            |
|                 |                 |                 |     it\_CH -    |
|                 |                 |                 |     it\_CH      |
|                 |                 |                 | -   Polish -    |
|                 |                 |                 |     pl - pl     |
|                 |                 |                 | -   Slovene -   |
|                 |                 |                 |     sl - sl     |
|                 |                 |                 | -   INVALID     |
|                 |                 |                 |     VALUE -     |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_ -   |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_     |
+-----------------+-----------------+-----------------+-----------------+
| defaultOrigin   | Traffic source  | link            |                 |
| (delivery)      |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| desc            | Description     | string (512)    |                 |
+-----------------+-----------------+-----------------+-----------------+
| designLanguage  | Design language | enumeration     | -   Greek -     |
|                 |                 | (string) (255)  |     el - el     |
|                 |                 |                 | -   English -   |
|                 |                 |                 |     en - en     |
|                 |                 |                 | -   Chinese -   |
|                 |                 |                 |     zh - zh     |
|                 |                 |                 | -   French      |
|                 |                 |                 |     (France) -  |
|                 |                 |                 |     fr\_FR -    |
|                 |                 |                 |     fr\_FR      |
|                 |                 |                 | -   Vietnamese  |
|                 |                 |                 | -               |
|                 |                 |                 |     vi - vi     |
|                 |                 |                 | -   Portuguese  |
|                 |                 |                 |     (Portugal)  |
|                 |                 |                 | -               |
|                 |                 |                 |     pt\_PT -    |
|                 |                 |                 |     pt\_PT      |
|                 |                 |                 | -   Italian     |
|                 |                 |                 |     (Italy) -   |
|                 |                 |                 |     it\_IT -    |
|                 |                 |                 |     it\_IT      |
|                 |                 |                 | -   Italian -   |
|                 |                 |                 |     it - it     |
|                 |                 |                 | -   Dutch       |
|                 |                 |                 |     (Belgium) - |
|                 |                 |                 |     nl\_BE -    |
|                 |                 |                 |     nl\_BE      |
|                 |                 |                 | -   Norwegian   |
|                 |                 |                 |     (Norway) -  |
|                 |                 |                 |     no\_NO -    |
|                 |                 |                 |     no\_NO      |
|                 |                 |                 | -   Dutch       |
|                 |                 |                 |     (Netherland |
|                 |                 |                 | s) -            |
|                 |                 |                 |     nl\_NL -    |
|                 |                 |                 |     nl\_NL      |
|                 |                 |                 | -   Arabic -    |
|                 |                 |                 |     ar - ar     |
|                 |                 |                 | -   English     |
|                 |                 |                 |     (United     |
|                 |                 |                 |     States) -   |
|                 |                 |                 |     en\_US -    |
|                 |                 |                 |     en\_US      |
|                 |                 |                 | -   Irish -     |
|                 |                 |                 |     ga - ga     |
|                 |                 |                 | -   Czech -     |
|                 |                 |                 |     cs - cs     |
|                 |                 |                 | -   Estonian -  |
|                 |                 |                 |     et - et     |
|                 |                 |                 | -   Indonesian  |
|                 |                 |                 | -               |
|                 |                 |                 |     id - id     |
|                 |                 |                 | -   Spanish -   |
|                 |                 |                 |     es - es     |
|                 |                 |                 | -   Russian -   |
|                 |                 |                 |     ru - ru     |
|                 |                 |                 | -   Dutch -     |
|                 |                 |                 |     nl - nl     |
|                 |                 |                 | -   Walloon -   |
|                 |                 |                 |     wa - wa     |
|                 |                 |                 | -   Portuguese  |
|                 |                 |                 | -               |
|                 |                 |                 |     pt - pt     |
|                 |                 |                 | -   French      |
|                 |                 |                 |     (Belgium) - |
|                 |                 |                 |     fr\_BE -    |
|                 |                 |                 |     fr\_BE      |
|                 |                 |                 | -   Latvian -   |
|                 |                 |                 |     lv - lv     |
|                 |                 |                 | -   Lithuanian  |
|                 |                 |                 | -               |
|                 |                 |                 |     lt - lt     |
|                 |                 |                 | -   Thai - th - |
|                 |                 |                 |     th          |
|                 |                 |                 | -   English     |
|                 |                 |                 |     (United     |
|                 |                 |                 |     Kingdom) -  |
|                 |                 |                 |     en\_GB -    |
|                 |                 |                 |     en\_GB      |
|                 |                 |                 | -   French -    |
|                 |                 |                 |     fr - fr     |
|                 |                 |                 | -   Portuguese  |
|                 |                 |                 |     (Brazil) -  |
|                 |                 |                 |     pt\_BR -    |
|                 |                 |                 |     pt\_BR      |
|                 |                 |                 | -   German -    |
|                 |                 |                 |     de - de     |
|                 |                 |                 | -   Danish -    |
|                 |                 |                 |     da - da     |
|                 |                 |                 | -   Finnish -   |
|                 |                 |                 |     fi - fi     |
|                 |                 |                 | -   Hungarian - |
|                 |                 |                 |     hu - hu     |
|                 |                 |                 | -   Swedish     |
|                 |                 |                 |     (Finland) - |
|                 |                 |                 |     sv\_FI -    |
|                 |                 |                 |     sv\_FI      |
|                 |                 |                 | -   Japanese -  |
|                 |                 |                 |     ja - ja     |
|                 |                 |                 | -   Hebrew -    |
|                 |                 |                 |     he - he     |
|                 |                 |                 | -   Korean -    |
|                 |                 |                 |     ko - ko     |
|                 |                 |                 | -   Swedish -   |
|                 |                 |                 |     sv - sv     |
|                 |                 |                 | -   Sweden      |
|                 |                 |                 |     (Swedish) - |
|                 |                 |                 |     sv\_SE -    |
|                 |                 |                 |     sv\_SE      |
|                 |                 |                 | -   Slovak -    |
|                 |                 |                 |     sk - sk     |
|                 |                 |                 | -   Maltese -   |
|                 |                 |                 |     mt - mt     |
|                 |                 |                 | -   Italian     |
|                 |                 |                 |     (Switzerlan |
|                 |                 |                 | d) -            |
|                 |                 |                 |     it\_CH -    |
|                 |                 |                 |     it\_CH      |
|                 |                 |                 | -   Polish -    |
|                 |                 |                 |     pl - pl     |
|                 |                 |                 | -   Slovene -   |
|                 |                 |                 |     sl - sl     |
|                 |                 |                 | -   INVALID     |
|                 |                 |                 |     VALUE -     |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_ -   |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_     |
+-----------------+-----------------+-----------------+-----------------+
| dynamicService  | Dynamic service | boolean         |                 |
+-----------------+-----------------+-----------------+-----------------+
| end             | Expiration date | date            |                 |
+-----------------+-----------------+-----------------+-----------------+
| errorContextRes | ErrorContextRes | string          |                 |
| ourceType       | ourceType       |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| errorPage       | Error page      | item            |                 |
+-----------------+-----------------+-----------------+-----------------+
| geoUnit         | Geographical    | link            |                 |
| (geoUnitBase)   | unit            |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| htmlPage        | Pages           | collection      |                 |
+-----------------+-----------------+-----------------+-----------------+
| identificationB | Identification  | boolean         |                 |
| yUrlParam       | by URL          |                 |                 |
|                 | parameters      |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| inactiveUrlRedi | Redirection URL | string (4096)   |                 |
| rection         |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| isExternal      | Is external     | boolean         |                 |
|                 | resource        |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| isTemplate      | Template        | boolean         |                 |
+-----------------+-----------------+-----------------+-----------------+
| job             | Job             | collection      |                 |
+-----------------+-----------------+-----------------+-----------------+
| jobLogs         | Logs            | collection      |                 |
+-----------------+-----------------+-----------------+-----------------+
| label           | Label           | string (128)    |                 |
+-----------------+-----------------+-----------------+-----------------+
| lastModified    | Last modified   | date            |                 |
+-----------------+-----------------+-----------------+-----------------+
| loadingFilter   | Loading key     | link            |                 |
| (queryFilterBas |                 |                 |                 |
| e)              |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| loadingFilterMa | Parameters of   | collection      |                 |
| pping           | the loading key |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| logicalStatus   | Execution       | enumeration     | -   In          |
|                 | status          | (string) (255)  |     progress -  |
|                 |                 |                 |     started -   |
|                 |                 |                 |     started     |
|                 |                 |                 | -   Editing -   |
|                 |                 |                 |     edition -   |
|                 |                 |                 |     edition     |
|                 |                 |                 | -   Finished -  |
|                 |                 |                 |     finished -  |
|                 |                 |                 |     finished    |
|                 |                 |                 | -   Warning -   |
|                 |                 |                 |     warning -   |
|                 |                 |                 |     warning     |
|                 |                 |                 | -   Erroneous - |
|                 |                 |                 |     error -     |
|                 |                 |                 |     error       |
|                 |                 |                 | -   INVALID     |
|                 |                 |                 |     VALUE -     |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_ -   |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_     |
+-----------------+-----------------+-----------------+-----------------+
| messageAction   | Start sending   | boolean         |                 |
|                 | message         |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| messageActionDe | Transactional   | link            |                 |
| livery          | message         |                 |                 |
| (deliveryMCTemp |                 |                 |                 |
| lateBase)       |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| modifiedBy      | Modified by     | link            |                 |
| (userBase)      |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| name            | ID              | string (64)     |                 |
+-----------------+-----------------+-----------------+-----------------+
| orgUnit         | Organizational  | link            |                 |
| (orgUnitBase)   | unit            |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| prefill         | Preload visitor | boolean         |                 |
|                 | data            |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| program         | Program         | link            |                 |
| (programBase)   |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| publicUrl       | Public URL      | string          |                 |
+-----------------+-----------------+-----------------+-----------------+
| publicationDate | Publication     | date            |                 |
|                 | date            |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| reconciliationF | Reconciliation  | link            |                 |
| ilter           | key             |                 |                 |
| (queryFilterBas |                 |                 |                 |
| e)              |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| reconciliationF | Reconciliation  | collection      |                 |
| ilterMapping    | key parameters  |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| reconciliationU | Update strategy | enumeration     | -   Update -    |
| pdateStrategy   |                 | (byte)          |     updateTarge |
|                 |                 |                 | t -             |
|                 |                 |                 |     1           |
|                 |                 |                 | -   Unauthorize |
|                 |                 |                 | d -             |
|                 |                 |                 |     unauthorize |
|                 |                 |                 | d -             |
|                 |                 |                 |     0           |
|                 |                 |                 | -   INVALID     |
|                 |                 |                 |     VALUE -     |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_ -   |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_     |
+-----------------+-----------------+-----------------+-----------------+
| service         | Subscription    | link            |                 |
| (serviceBase)   | service         |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| specificAction  | Specific action | enumeration     | -   Blacklist - |
|                 |                 | (byte)          |     blackList - |
|                 |                 |                 |     3           |
|                 |                 |                 | -   No specific |
|                 |                 |                 |     action -    |
|                 |                 |                 |     none - 0    |
|                 |                 |                 | -   Unsubscript |
|                 |                 |                 | ion -           |
|                 |                 |                 |     unsubscript |
|                 |                 |                 | ion -           |
|                 |                 |                 |     2           |
|                 |                 |                 | -   INVALID     |
|                 |                 |                 |     VALUE -     |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_ -   |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_     |
|                 |                 |                 | -   Subscriptio |
|                 |                 |                 | n -             |
|                 |                 |                 |     subscriptio |
|                 |                 |                 | n -             |
|                 |                 |                 |     1           |
+-----------------+-----------------+-----------------+-----------------+
| start           | Deployment date | date            |                 |
+-----------------+-----------------+-----------------+-----------------+
| state           | Status          | enumeration     | -   Editing -   |
|                 |                 | (byte)          |     edit - 0    |
|                 |                 |                 | -   Publishing  |
|                 |                 |                 |     failed -    |
|                 |                 |                 |     failed - 99 |
|                 |                 |                 | -   Closed -    |
|                 |                 |                 |     closed - 20 |
|                 |                 |                 | -   INVALID     |
|                 |                 |                 |     VALUE -     |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_ -   |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_     |
|                 |                 |                 | -   Online -    |
|                 |                 |                 |     opened - 10 |
+-----------------+-----------------+-----------------+-----------------+
| targetResource  | Targeting       | string (255)    |                 |
|                 | dimension       |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| template        | Landing page    | link            |                 |
| (landingPage)   | template        |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| testUrl         | Test URL        | string          |                 |
+-----------------+-----------------+-----------------+-----------------+
| thumbnail       | Thumbnail       | string (255)    |                 |
+-----------------+-----------------+-----------------+-----------------+
| timezone        | Time zone       | enumeration     | -   (GMT-02:00) |
|                 |                 | (string) (64)   |     Central-Atl |
|                 |                 |                 | antic -         |
|                 |                 |                 |     Atlantic\_S |
|                 |                 |                 | outh\_Georgia - |
|                 |                 |                 |     Atlantic/So |
|                 |                 |                 | uth\_Georgia    |
|                 |                 |                 | -   (GMT+02:00) |
|                 |                 |                 |     Amman -     |
|                 |                 |                 |     Asia\_Amman |
|                 |                 |                 |  -              |
|                 |                 |                 |     Asia/Amman  |
|                 |                 |                 | -   (GMT-03:00) |
|                 |                 |                 |     Brasi -     |
|                 |                 |                 |     America\_Sa |
|                 |                 |                 | o\_Paulo -      |
|                 |                 |                 |     America/Sao |
|                 |                 |                 | \_Paulo         |
|                 |                 |                 | -   (GMT+06:00) |
|                 |                 |                 |     Astana,     |
|                 |                 |                 |     Dhaka -     |
|                 |                 |                 |     Asia\_Dhaka |
|                 |                 |                 |  -              |
|                 |                 |                 |     Asia/Dhaka  |
|                 |                 |                 | -   (GMT+06:00) |
|                 |                 |                 |     Novossibirs |
|                 |                 |                 | k -             |
|                 |                 |                 |     Asia\_Novos |
|                 |                 |                 | ibirsk -        |
|                 |                 |                 |     Asia/Novosi |
|                 |                 |                 | birsk           |
|                 |                 |                 | -   (GMT+02:00) |
|                 |                 |                 |     Windhoek -  |
|                 |                 |                 |     Africa\_Win |
|                 |                 |                 | dhoek -         |
|                 |                 |                 |     Africa/Wind |
|                 |                 |                 | hoek            |
|                 |                 |                 | -   (GMT+04:00) |
|                 |                 |                 |     Caucasus,   |
|                 |                 |                 |     Erevan -    |
|                 |                 |                 |     Asia\_Yerev |
|                 |                 |                 | an -            |
|                 |                 |                 |     Asia/Yereva |
|                 |                 |                 | n               |
|                 |                 |                 | -   (GMT-04:00) |
|                 |                 |                 |     Manaus -    |
|                 |                 |                 |     America\_Ma |
|                 |                 |                 | naus -          |
|                 |                 |                 |     America/Man |
|                 |                 |                 | aus             |
|                 |                 |                 | -   (GMT+03:30) |
|                 |                 |                 |     Teheran -   |
|                 |                 |                 |     Asia\_Tehra |
|                 |                 |                 | n -             |
|                 |                 |                 |     Asia/Tehran |
|                 |                 |                 | -   (GMT+12:00) |
|                 |                 |                 |     Auckland,   |
|                 |                 |                 |     Wellington  |
|                 |                 |                 | -               |
|                 |                 |                 |     Pacific\_Au |
|                 |                 |                 | ckland -        |
|                 |                 |                 |     Pacific/Auc |
|                 |                 |                 | kland           |
|                 |                 |                 | -   (GMT+02:00) |
|                 |                 |                 |     Jerusalem - |
|                 |                 |                 |     Asia\_Jerus |
|                 |                 |                 | alem -          |
|                 |                 |                 |     Asia/Jerusa |
|                 |                 |                 | lem             |
|                 |                 |                 | -   (GMT+03:00) |
|                 |                 |                 |     Moscow, St. |
|                 |                 |                 |     Petersburg, |
|                 |                 |                 |     Volgograd - |
|                 |                 |                 |     Europe\_Mos |
|                 |                 |                 | cow -           |
|                 |                 |                 |     Europe/Mosc |
|                 |                 |                 | ow              |
|                 |                 |                 | -   (GMT+09:30) |
|                 |                 |                 |     Adelaïde -  |
|                 |                 |                 |     Australia\_ |
|                 |                 |                 | Adelaide -      |
|                 |                 |                 |     Australia/A |
|                 |                 |                 | delaide         |
|                 |                 |                 | -   (GMT+10:00) |
|                 |                 |                 |     Canberra,   |
|                 |                 |                 |     Melbourne,  |
|                 |                 |                 |     Sydney -    |
|                 |                 |                 |     Australia\_ |
|                 |                 |                 | Canberra -      |
|                 |                 |                 |     Australia/C |
|                 |                 |                 | anberra         |
|                 |                 |                 | -   (GMT+08:00) |
|                 |                 |                 |     Perth -     |
|                 |                 |                 |     Australia\_ |
|                 |                 |                 | Perth -         |
|                 |                 |                 |     Australia/P |
|                 |                 |                 | erth            |
|                 |                 |                 | -   (GMT+09:00) |
|                 |                 |                 |     Yakoutsk -  |
|                 |                 |                 |     Asia\_Yakut |
|                 |                 |                 | sk -            |
|                 |                 |                 |     Asia/Yakuts |
|                 |                 |                 | k               |
|                 |                 |                 | -   (GMT-10:00) |
|                 |                 |                 |     Hawai -     |
|                 |                 |                 |     Pacific\_Ho |
|                 |                 |                 | nolulu -        |
|                 |                 |                 |     Pacific/Hon |
|                 |                 |                 | olulu           |
|                 |                 |                 | -   (GMT+04:00) |
|                 |                 |                 |     Baku -      |
|                 |                 |                 |     Asia\_Baku  |
|                 |                 |                 | -               |
|                 |                 |                 |     Asia/Baku   |
|                 |                 |                 | -   (GMT+10:00) |
|                 |                 |                 |     Vladivostok |
|                 |                 |                 |  -              |
|                 |                 |                 |     Asia\_Vladi |
|                 |                 |                 | vostok -        |
|                 |                 |                 |     Asia/Vladiv |
|                 |                 |                 | ostok           |
|                 |                 |                 | -   (GMT+09:00) |
|                 |                 |                 |     Seoul -     |
|                 |                 |                 |     Asia\_Seoul |
|                 |                 |                 |  -              |
|                 |                 |                 |     Asia/Seoul  |
|                 |                 |                 | -   (GMT+01:00) |
|                 |                 |                 |     Sarajevo,   |
|                 |                 |                 |     Skoplje,    |
|                 |                 |                 |     Sofia,      |
|                 |                 |                 |     Warsaw,     |
|                 |                 |                 |     Zagreb -    |
|                 |                 |                 |     Europe\_Sar |
|                 |                 |                 | ajevo -         |
|                 |                 |                 |     Europe/Sara |
|                 |                 |                 | jevo            |
|                 |                 |                 | -   Server time |
|                 |                 |                 |     zone -      |
|                 |                 |                 |     \_server\_  |
|                 |                 |                 | -               |
|                 |                 |                 |     \_server\_  |
|                 |                 |                 | -   (GMT+04:00) |
|                 |                 |                 |     Abu Dhabi,  |
|                 |                 |                 |     Muscat -    |
|                 |                 |                 |     Asia\_Musca |
|                 |                 |                 | t -             |
|                 |                 |                 |     Asia/Muscat |
|                 |                 |                 | -   (GMT+08:00) |
|                 |                 |                 |     Kuala       |
|                 |                 |                 |     Lumpur,     |
|                 |                 |                 |     Singapore - |
|                 |                 |                 |     Asia\_Kuala |
|                 |                 |                 | \_Lumpur -      |
|                 |                 |                 |     Asia/Kuala\ |
|                 |                 |                 | _Lumpur         |
|                 |                 |                 | -   (GMT+09:00) |
|                 |                 |                 |     Osaka,      |
|                 |                 |                 |     Sapporo,    |
|                 |                 |                 |     Tokyo -     |
|                 |                 |                 |     Asia\_Tokyo |
|                 |                 |                 |  -              |
|                 |                 |                 |     Asia/Tokyo  |
|                 |                 |                 | -   (GMT+10:00) |
|                 |                 |                 |     Brisbane -  |
|                 |                 |                 |     Australia\_ |
|                 |                 |                 | Brisbane -      |
|                 |                 |                 |     Australia/B |
|                 |                 |                 | risbane         |
|                 |                 |                 | -   (GMT+05:30) |
|                 |                 |                 |     Sri         |
|                 |                 |                 |     Jayawardene |
|                 |                 |                 | pura -          |
|                 |                 |                 |     Asia\_Colom |
|                 |                 |                 | bo -            |
|                 |                 |                 |     Asia/Colomb |
|                 |                 |                 | o               |
|                 |                 |                 | -   (GMT+02:00) |
|                 |                 |                 |     Harare,     |
|                 |                 |                 |     Pretoria -  |
|                 |                 |                 |     Africa\_Har |
|                 |                 |                 | are -           |
|                 |                 |                 |     Africa/Hara |
|                 |                 |                 | re              |
|                 |                 |                 | -   (GMT+08:00) |
|                 |                 |                 |     Oulan-Bator |
|                 |                 |                 |  -              |
|                 |                 |                 |     Asia\_Ulan\ |
|                 |                 |                 | _Bator -        |
|                 |                 |                 |     Asia/Ulan\_ |
|                 |                 |                 | Bator           |
|                 |                 |                 | -   (GMT-02:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     minus 2     |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_m2 -   |
|                 |                 |                 |     Etc/GMT+2   |
|                 |                 |                 | -   (GMT-03:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     minus 3     |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_m3 -   |
|                 |                 |                 |     Etc/GMT+3   |
|                 |                 |                 | -   (GMT-01:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     minus 1     |
|                 |                 |                 |     hour -      |
|                 |                 |                 |     Gmt\_m1 -   |
|                 |                 |                 |     Etc/GMT+1   |
|                 |                 |                 | -   (GMT-06:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     minus 6     |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_m6 -   |
|                 |                 |                 |     Etc/GMT+6   |
|                 |                 |                 | -   (GMT-07:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     minus 7     |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_m7 -   |
|                 |                 |                 |     Etc/GMT+7   |
|                 |                 |                 | -   (GMT-04:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     minus 4     |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_m4 -   |
|                 |                 |                 |     Etc/GMT+4   |
|                 |                 |                 | -   (GMT)       |
|                 |                 |                 |     Casablanca  |
|                 |                 |                 | -               |
|                 |                 |                 |     Africa\_Cas |
|                 |                 |                 | ablanca -       |
|                 |                 |                 |     Africa/Casa |
|                 |                 |                 | blanca          |
|                 |                 |                 | -   (GMT+05:30) |
|                 |                 |                 |     Kolkata,    |
|                 |                 |                 |     Chennai,    |
|                 |                 |                 |     Mumbai, New |
|                 |                 |                 |     Delhi -     |
|                 |                 |                 |     Asia\_Kolka |
|                 |                 |                 | ta -            |
|                 |                 |                 |     Asia/Kolkat |
|                 |                 |                 | a               |
|                 |                 |                 | -   (GMT-11:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     minus 11    |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_m11 -  |
|                 |                 |                 |     Etc/GMT+11  |
|                 |                 |                 | -   (GMT-09:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     minus 9     |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_m9 -   |
|                 |                 |                 |     Etc/GMT+9   |
|                 |                 |                 | -   (GMT-03:30) |
|                 |                 |                 |     Newfoundlan |
|                 |                 |                 | d -             |
|                 |                 |                 |     America\_St |
|                 |                 |                 | \_Johns -       |
|                 |                 |                 |     America/St\ |
|                 |                 |                 | _Johns          |
|                 |                 |                 | -   Default -   |
|                 |                 |                 |     \_inherit\_ |
|                 |                 |                 |  -              |
|                 |                 |                 |     \_inherit\_ |
|                 |                 |                 | -   (GMT+03:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 3      |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_p3 -   |
|                 |                 |                 |     Etc/GMT-3   |
|                 |                 |                 | -   (GMT-04:30) |
|                 |                 |                 |     Caracas -   |
|                 |                 |                 |     America\_Ca |
|                 |                 |                 | racas -         |
|                 |                 |                 |     America/Car |
|                 |                 |                 | acas            |
|                 |                 |                 | -   (GMT+01:00) |
|                 |                 |                 |     Amsterdam,  |
|                 |                 |                 |     Berlin,     |
|                 |                 |                 |     Berne,      |
|                 |                 |                 |     Rome,       |
|                 |                 |                 |     Stockholm,  |
|                 |                 |                 |     Vienna -    |
|                 |                 |                 |     Europe\_Ber |
|                 |                 |                 | lin -           |
|                 |                 |                 |     Europe/Berl |
|                 |                 |                 | in              |
|                 |                 |                 | -   (GMT-07:00) |
|                 |                 |                 |     Chihuahua,  |
|                 |                 |                 |     La Paz,     |
|                 |                 |                 |     Mazatlan -  |
|                 |                 |                 |     America\_Ch |
|                 |                 |                 | ihuahua -       |
|                 |                 |                 |     America/Chi |
|                 |                 |                 | huahua          |
|                 |                 |                 | -   (GMT+03:00) |
|                 |                 |                 |     Nairobi -   |
|                 |                 |                 |     Africa\_Nai |
|                 |                 |                 | robi -          |
|                 |                 |                 |     Africa/Nair |
|                 |                 |                 | obi             |
|                 |                 |                 | -   (GMT-04:00) |
|                 |                 |                 |     Asunción -  |
|                 |                 |                 |     America\_As |
|                 |                 |                 | uncion -        |
|                 |                 |                 |     America/Asu |
|                 |                 |                 | ncion           |
|                 |                 |                 | -   (GMT+03:00) |
|                 |                 |                 |     Bagdad -    |
|                 |                 |                 |     Asia\_Baghd |
|                 |                 |                 | ad -            |
|                 |                 |                 |     Asia/Baghda |
|                 |                 |                 | d               |
|                 |                 |                 | -   (GMT-10:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     minus 10    |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_m10 -  |
|                 |                 |                 |     Etc/GMT+10  |
|                 |                 |                 | -   (GMT-03:00) |
|                 |                 |                 |     Greenland - |
|                 |                 |                 |     America\_Go |
|                 |                 |                 | dthab -         |
|                 |                 |                 |     America/God |
|                 |                 |                 | thab            |
|                 |                 |                 | -   (GMT+02:00) |
|                 |                 |                 |     Damas -     |
|                 |                 |                 |     Asia\_Damas |
|                 |                 |                 | cus -           |
|                 |                 |                 |     Asia/Damasc |
|                 |                 |                 | us              |
|                 |                 |                 | -   (GMT-11:00) |
|                 |                 |                 |     Samoa -     |
|                 |                 |                 |     Pacific\_Sa |
|                 |                 |                 | moa -           |
|                 |                 |                 |     Pacific/Sam |
|                 |                 |                 | oa              |
|                 |                 |                 | -   (GMT-05:00) |
|                 |                 |                 |     Bogota,     |
|                 |                 |                 |     Lima,       |
|                 |                 |                 |     Quito -     |
|                 |                 |                 |     America\_Bo |
|                 |                 |                 | gota -          |
|                 |                 |                 |     America/Bog |
|                 |                 |                 | ota             |
|                 |                 |                 | -   (GMT+01:00) |
|                 |                 |                 |     Brussels,   |
|                 |                 |                 |     Copenhagen, |
|                 |                 |                 |     Madrid,     |
|                 |                 |                 |     Paris -     |
|                 |                 |                 |     Europe\_Par |
|                 |                 |                 | is -            |
|                 |                 |                 |     Europe/Pari |
|                 |                 |                 | s               |
|                 |                 |                 | -   (GMT+08:00) |
|                 |                 |                 |     Beijing,    |
|                 |                 |                 |     Chongqing,  |
|                 |                 |                 |     Hong Kong,  |
|                 |                 |                 |     Urumqi -    |
|                 |                 |                 |     Asia\_Shang |
|                 |                 |                 | hai -           |
|                 |                 |                 |     Asia/Shangh |
|                 |                 |                 | ai              |
|                 |                 |                 | -   (GMT+12:00) |
|                 |                 |                 |     Fidji -     |
|                 |                 |                 |     Pacific\_Fi |
|                 |                 |                 | ji -            |
|                 |                 |                 |     Pacific/Fij |
|                 |                 |                 | i               |
|                 |                 |                 | -   (GMT+02:00) |
|                 |                 |                 |     Athens,     |
|                 |                 |                 |     Istanbul,   |
|                 |                 |                 |     Minsk -     |
|                 |                 |                 |     Europe\_Ath |
|                 |                 |                 | ens -           |
|                 |                 |                 |     Europe/Athe |
|                 |                 |                 | ns              |
|                 |                 |                 | -   (GMT+04:00) |
|                 |                 |                 |     Tbilissi -  |
|                 |                 |                 |     Asia\_Tbili |
|                 |                 |                 | si -            |
|                 |                 |                 |     Asia/Tbilis |
|                 |                 |                 | i               |
|                 |                 |                 | -   INVALID     |
|                 |                 |                 |     VALUE -     |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_ -   |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_     |
|                 |                 |                 | -   (GMT+05:45) |
|                 |                 |                 |     Katmandu -  |
|                 |                 |                 |     Asia\_Katma |
|                 |                 |                 | ndu -           |
|                 |                 |                 |     Asia/Katman |
|                 |                 |                 | du              |
|                 |                 |                 | -   (GMT-05:00) |
|                 |                 |                 |     Indiana     |
|                 |                 |                 |     (East) -    |
|                 |                 |                 |     America\_In |
|                 |                 |                 | dianapolis -    |
|                 |                 |                 |     America/Ind |
|                 |                 |                 | ianapolis       |
|                 |                 |                 | -   (GMT-01:00) |
|                 |                 |                 |     Cape Verde  |
|                 |                 |                 |     islands -   |
|                 |                 |                 |     Atlantic\_C |
|                 |                 |                 | ape\_Verde -    |
|                 |                 |                 |     Atlantic/Ca |
|                 |                 |                 | pe\_Verde       |
|                 |                 |                 | -   (GMT+04:00) |
|                 |                 |                 |     Port        |
|                 |                 |                 |     Louis -     |
|                 |                 |                 |     Indian\_Mau |
|                 |                 |                 | ritius -        |
|                 |                 |                 |     Indian/Maur |
|                 |                 |                 | itius           |
|                 |                 |                 | -   (GMT+08:00) |
|                 |                 |                 |     Taipei -    |
|                 |                 |                 |     Asia\_Taipe |
|                 |                 |                 | i -             |
|                 |                 |                 |     Asia/Taipei |
|                 |                 |                 | -   Time zone   |
|                 |                 |                 |     of the      |
|                 |                 |                 |     database -  |
|                 |                 |                 |     \_wdbc\_ -  |
|                 |                 |                 |     \_wdbc\_    |
|                 |                 |                 | -   (GMT+06:30) |
|                 |                 |                 |     Rangoon -   |
|                 |                 |                 |     Asia\_Rango |
|                 |                 |                 | on -            |
|                 |                 |                 |     Asia/Rangoo |
|                 |                 |                 | n               |
|                 |                 |                 | -   (GMT+11:00) |
|                 |                 |                 |     Magadan,    |
|                 |                 |                 |     The Solomon |
|                 |                 |                 |     Islands,    |
|                 |                 |                 |     New         |
|                 |                 |                 |     Caledonia - |
|                 |                 |                 |     Pacific\_Gu |
|                 |                 |                 | adalcanal -     |
|                 |                 |                 |     Pacific/Gua |
|                 |                 |                 | dalcanal        |
|                 |                 |                 | -   (GMT+02:00) |
|                 |                 |                 |     Cairo -     |
|                 |                 |                 |     Africa\_Cai |
|                 |                 |                 | ro -            |
|                 |                 |                 |     Africa/Cair |
|                 |                 |                 | o               |
|                 |                 |                 | -   (GMT+05:00) |
|                 |                 |                 |     Iekaterinbu |
|                 |                 |                 | rg -            |
|                 |                 |                 |     Asia\_Yekat |
|                 |                 |                 | erinburg -      |
|                 |                 |                 |     Asia/Yekate |
|                 |                 |                 | rinburg         |
|                 |                 |                 | -   (GMT+08:00) |
|                 |                 |                 |     Irkoutsk -  |
|                 |                 |                 |     Asia\_Irkut |
|                 |                 |                 | sk -            |
|                 |                 |                 |     Asia/Irkuts |
|                 |                 |                 | k               |
|                 |                 |                 | -   (GMT+10:00) |
|                 |                 |                 |     Guam, Port  |
|                 |                 |                 |     Moresby -   |
|                 |                 |                 |     Pacific\_Gu |
|                 |                 |                 | am -            |
|                 |                 |                 |     Pacific/Gua |
|                 |                 |                 | m               |
|                 |                 |                 | -   (GMT-04:00) |
|                 |                 |                 |     Atlantic    |
|                 |                 |                 |     Standard    |
|                 |                 |                 |     Time        |
|                 |                 |                 |     (Canada) -  |
|                 |                 |                 |     America\_Ha |
|                 |                 |                 | lifax -         |
|                 |                 |                 |     America/Hal |
|                 |                 |                 | ifax            |
|                 |                 |                 | -   (GMT)       |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     mean time - |
|                 |                 |                 |     GMT - GMT   |
|                 |                 |                 | -   (GMT-04:00) |
|                 |                 |                 |     La Paz -    |
|                 |                 |                 |     America\_La |
|                 |                 |                 | \_Paz -         |
|                 |                 |                 |     America/La\ |
|                 |                 |                 | _Paz            |
|                 |                 |                 | -   Operator    |
|                 |                 |                 |     time zone - |
|                 |                 |                 |     \_login\_ - |
|                 |                 |                 |     \_login\_   |
|                 |                 |                 | -   (GMT-06:00) |
|                 |                 |                 |     Guadalajara |
|                 |                 |                 | ,               |
|                 |                 |                 |     Mexico,     |
|                 |                 |                 |     Monterrey - |
|                 |                 |                 |     America\_Me |
|                 |                 |                 | xico\_City -    |
|                 |                 |                 |     America/Mex |
|                 |                 |                 | ico\_City       |
|                 |                 |                 | -   (GMT+09:30) |
|                 |                 |                 |     Darwin -    |
|                 |                 |                 |     Australia\_ |
|                 |                 |                 | Darwin -        |
|                 |                 |                 |     Australia/D |
|                 |                 |                 | arwin           |
|                 |                 |                 | -   (GMT-05:00) |
|                 |                 |                 |     Est (United |
|                 |                 |                 |     States and  |
|                 |                 |                 |     Canada) -   |
|                 |                 |                 |     America\_Ne |
|                 |                 |                 | w\_York -       |
|                 |                 |                 |     America/New |
|                 |                 |                 | \_York          |
|                 |                 |                 | -   (GMT-05:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     minus 5     |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_m5 -   |
|                 |                 |                 |     Etc/GMT+5   |
|                 |                 |                 | -   (GMT+05:00) |
|                 |                 |                 |     Islamabad,  |
|                 |                 |                 |     Karachi,    |
|                 |                 |                 |     Tachkent -  |
|                 |                 |                 |     Asia\_Karac |
|                 |                 |                 | hi -            |
|                 |                 |                 |     Asia/Karach |
|                 |                 |                 | i               |
|                 |                 |                 | -   (GMT+03:00) |
|                 |                 |                 |     Koweït,     |
|                 |                 |                 |     Riyad -     |
|                 |                 |                 |     Asia\_Riyad |
|                 |                 |                 | h -             |
|                 |                 |                 |     Asia/Riyadh |
|                 |                 |                 | -   (GMT-08:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     minus 8     |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_m8 -   |
|                 |                 |                 |     Etc/GMT+8   |
|                 |                 |                 | -   (GMT-01:00) |
|                 |                 |                 |     The         |
|                 |                 |                 |     Azores -    |
|                 |                 |                 |     Atlantic\_A |
|                 |                 |                 | zores -         |
|                 |                 |                 |     Atlantic/Az |
|                 |                 |                 | ores            |
|                 |                 |                 | -   (GMT+07:00) |
|                 |                 |                 |     Bangkok,    |
|                 |                 |                 |     Hanoi,      |
|                 |                 |                 |     Djakarta -  |
|                 |                 |                 |     Asia\_Bangk |
|                 |                 |                 | ok -            |
|                 |                 |                 |     Asia/Bangko |
|                 |                 |                 | k               |
|                 |                 |                 | -   (GMT)       |
|                 |                 |                 |     Monrovia -  |
|                 |                 |                 |     Africa\_Mon |
|                 |                 |                 | rovia -         |
|                 |                 |                 |     Africa/Monr |
|                 |                 |                 | ovia            |
|                 |                 |                 | -   (GMT-09:00) |
|                 |                 |                 |     Alaska -    |
|                 |                 |                 |     America\_An |
|                 |                 |                 | chorage -       |
|                 |                 |                 |     America/Anc |
|                 |                 |                 | horage          |
|                 |                 |                 | -   (GMT+01:00) |
|                 |                 |                 |     Belgrade,   |
|                 |                 |                 |     Bratislava, |
|                 |                 |                 |     Budapest,   |
|                 |                 |                 |     Ljubljana,  |
|                 |                 |                 |     Prague -    |
|                 |                 |                 |     Europe\_Bel |
|                 |                 |                 | grade -         |
|                 |                 |                 |     Europe/Belg |
|                 |                 |                 | rade            |
|                 |                 |                 | -   (GMT)       |
|                 |                 |                 |     Reykjavik - |
|                 |                 |                 |     Atlantic\_R |
|                 |                 |                 | eykjavik -      |
|                 |                 |                 |     Atlantic/Re |
|                 |                 |                 | ykjavik         |
|                 |                 |                 | -   (GMT+02:00) |
|                 |                 |                 |     Bucarest -  |
|                 |                 |                 |     Europe\_Buc |
|                 |                 |                 | harest -        |
|                 |                 |                 |     Europe/Buch |
|                 |                 |                 | arest           |
|                 |                 |                 | -   (GMT+05:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 5      |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_p5 -   |
|                 |                 |                 |     Etc/GMT-5   |
|                 |                 |                 | -   (GMT+04:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 4      |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_p4 -   |
|                 |                 |                 |     Etc/GMT-4   |
|                 |                 |                 | -   (GMT+07:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 7      |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_p7 -   |
|                 |                 |                 |     Etc/GMT-7   |
|                 |                 |                 | -   (GMT+06:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 6      |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_p6 -   |
|                 |                 |                 |     Etc/GMT-6   |
|                 |                 |                 | -   (GMT+01:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 1      |
|                 |                 |                 |     hour -      |
|                 |                 |                 |     Gmt\_p1 -   |
|                 |                 |                 |     Etc/GMT-1   |
|                 |                 |                 | -   (GMT-08:00) |
|                 |                 |                 |     Pacific     |
|                 |                 |                 |     (United     |
|                 |                 |                 |     States and  |
|                 |                 |                 |     Canada) -   |
|                 |                 |                 |     America\_Lo |
|                 |                 |                 | s\_Angeles -    |
|                 |                 |                 |     America/Los |
|                 |                 |                 | \_Angeles       |
|                 |                 |                 | -   (GMT+02:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 2      |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_p2 -   |
|                 |                 |                 |     Etc/GMT-2   |
|                 |                 |                 | -   (GMT+07:00) |
|                 |                 |                 |     Krasnoïarsk |
|                 |                 |                 |  -              |
|                 |                 |                 |     Asia\_Krasn |
|                 |                 |                 | oyarsk -        |
|                 |                 |                 |     Asia/Krasno |
|                 |                 |                 | yarsk           |
|                 |                 |                 | -   (GMT+09:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 9      |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_p9 -   |
|                 |                 |                 |     Etc/GMT-9   |
|                 |                 |                 | -   (GMT+08:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 8      |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_p8 -   |
|                 |                 |                 |     Etc/GMT-8   |
|                 |                 |                 | -   (GMT+10:00) |
|                 |                 |                 |     Hobart -    |
|                 |                 |                 |     Australia\_ |
|                 |                 |                 | Hobart -        |
|                 |                 |                 |     Australia/H |
|                 |                 |                 | obart           |
|                 |                 |                 | -   (GMT+13:00) |
|                 |                 |                 |     Nuku\'alofa |
|                 |                 |                 |  -              |
|                 |                 |                 |     Pacific\_To |
|                 |                 |                 | ngatapu -       |
|                 |                 |                 |     Pacific/Ton |
|                 |                 |                 | gatapu          |
|                 |                 |                 | -   (GMT-06:00) |
|                 |                 |                 |     Central     |
|                 |                 |                 |     America -   |
|                 |                 |                 |     America\_Re |
|                 |                 |                 | gina -          |
|                 |                 |                 |     America/Reg |
|                 |                 |                 | ina             |
|                 |                 |                 | -   (GMT-03:00) |
|                 |                 |                 |     Buenos      |
|                 |                 |                 |     Aires,      |
|                 |                 |                 |     Cayenne,    |
|                 |                 |                 |     Fortaleza - |
|                 |                 |                 |     America\_Bu |
|                 |                 |                 | enos\_Aires -   |
|                 |                 |                 |     America/Bue |
|                 |                 |                 | nos\_Aires      |
|                 |                 |                 | -   (GMT-07:00) |
|                 |                 |                 |     Rocky       |
|                 |                 |                 |     Mountains   |
|                 |                 |                 |     (United     |
|                 |                 |                 |     States and  |
|                 |                 |                 |     Canada) -   |
|                 |                 |                 |     America\_De |
|                 |                 |                 | nver -          |
|                 |                 |                 |     America/Den |
|                 |                 |                 | ver             |
|                 |                 |                 | -   (GMT+01:00) |
|                 |                 |                 |     Central     |
|                 |                 |                 |     Africa -    |
|                 |                 |                 |     West -      |
|                 |                 |                 |     Africa\_Lua |
|                 |                 |                 | nda -           |
|                 |                 |                 |     Africa/Luan |
|                 |                 |                 | da              |
|                 |                 |                 | -   (GMT+02:00) |
|                 |                 |                 |     Helsinki,   |
|                 |                 |                 |     Kiev, Riga, |
|                 |                 |                 |     Sofia,      |
|                 |                 |                 |     Tallinn,    |
|                 |                 |                 |     Vilnius -   |
|                 |                 |                 |     Europe\_Hel |
|                 |                 |                 | sinki -         |
|                 |                 |                 |     Europe/Hels |
|                 |                 |                 | inki            |
|                 |                 |                 | -   (GMT)       |
|                 |                 |                 |     Greenwich M |
|                 |                 |                 | ean             |
|                 |                 |                 |     Time:       |
|                 |                 |                 |     Dublin,     |
|                 |                 |                 |     Edinburgh,  |
|                 |                 |                 |     Lisbon,     |
|                 |                 |                 |     London -    |
|                 |                 |                 |     Europe\_Lon |
|                 |                 |                 | don -           |
|                 |                 |                 |     Europe/Lond |
|                 |                 |                 | on              |
|                 |                 |                 | -   (GMT-07:00) |
|                 |                 |                 |     Arizona -   |
|                 |                 |                 |     America\_Ph |
|                 |                 |                 | oenix -         |
|                 |                 |                 |     America/Pho |
|                 |                 |                 | enix            |
|                 |                 |                 | -   (GMT+02:00) |
|                 |                 |                 |     Beirut -    |
|                 |                 |                 |     Asia\_Beiru |
|                 |                 |                 | t -             |
|                 |                 |                 |     Asia/Beirut |
|                 |                 |                 | -   (GMT+04:30) |
|                 |                 |                 |     Kabul -     |
|                 |                 |                 |     Asia\_Kabul |
|                 |                 |                 |  -              |
|                 |                 |                 |     Asia/Kabul  |
|                 |                 |                 | -   (GMT-06:00) |
|                 |                 |                 |     Center      |
|                 |                 |                 |     (United     |
|                 |                 |                 |     States and  |
|                 |                 |                 |     Canada) -   |
|                 |                 |                 |     America\_Ch |
|                 |                 |                 | icago -         |
|                 |                 |                 |     America/Chi |
|                 |                 |                 | cago            |
|                 |                 |                 | -   (GMT+11:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 11     |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_p11 -  |
|                 |                 |                 |     Etc/GMT-11  |
|                 |                 |                 | -   (GMT+10:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 10     |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_p10 -  |
|                 |                 |                 |     Etc/GMT-10  |
|                 |                 |                 | -   (GMT+13:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 13     |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_p13 -  |
|                 |                 |                 |     Etc/GMT-13  |
|                 |                 |                 | -   (GMT+12:00) |
|                 |                 |                 |     Greenwich   |
|                 |                 |                 |     Mean Time   |
|                 |                 |                 |     plus 12     |
|                 |                 |                 |     hours -     |
|                 |                 |                 |     Gmt\_p12 -  |
|                 |                 |                 |     Etc/GMT-12  |
|                 |                 |                 | -   (GMT-04:00) |
|                 |                 |                 |     Santiago -  |
|                 |                 |                 |     America\_Sa |
|                 |                 |                 | ntiago -        |
|                 |                 |                 |     America/San |
|                 |                 |                 | tiago           |
|                 |                 |                 | -   (GMT-03:00) |
|                 |                 |                 |     Montevideo  |
|                 |                 |                 | -               |
|                 |                 |                 |     America\_Mo |
|                 |                 |                 | ntevideo -      |
|                 |                 |                 |     America/Mon |
|                 |                 |                 | tevideo         |
|                 |                 |                 | -   (GMT-04:00) |
|                 |                 |                 |     Cuiaba -    |
|                 |                 |                 |     America\_Cu |
|                 |                 |                 | iaba -          |
|                 |                 |                 |     America/Cui |
|                 |                 |                 | aba             |
+-----------------+-----------------+-----------------+-----------------+
| title           | Landing page    | string (255)    |                 |
+-----------------+-----------------+-----------------+-----------------+
| trackingEnabled | Log responses   | boolean         |                 |
+-----------------+-----------------+-----------------+-----------------+
| trackingUrlName | Tracking URL    | string          |                 |
|                 | name            |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| type            | Type            | enumeration     | -   Generic -   |
|                 |                 | (byte)          |     generic - 0 |
|                 |                 |                 | -   Unsubscript |
|                 |                 |                 | ion             |
|                 |                 |                 |     from a      |
|                 |                 |                 |     service -   |
|                 |                 |                 |     unsubscript |
|                 |                 |                 | ion -           |
|                 |                 |                 |     3           |
|                 |                 |                 | -   Blacklist - |
|                 |                 |                 |     blackList - |
|                 |                 |                 |     4           |
|                 |                 |                 | -   INVALID     |
|                 |                 |                 |     VALUE -     |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_ -   |
|                 |                 |                 |     \_\_Invalid |
|                 |                 |                 | \_value\_\_     |
|                 |                 |                 | -   Acquisition |
|                 |                 |                 |  -              |
|                 |                 |                 |     acquisition |
|                 |                 |                 |  -              |
|                 |                 |                 |     1           |
|                 |                 |                 | -   Subscriptio |
|                 |                 |                 | n               |
|                 |                 |                 |     to a        |
|                 |                 |                 |     service -   |
|                 |                 |                 |     subscriptio |
|                 |                 |                 | n -             |
|                 |                 |                 |     2           |
+-----------------+-----------------+-----------------+-----------------+
| uuid            | Security ID     | string          |                 |
+-----------------+-----------------+-----------------+-----------------+
| webTrackingEnab | Enable web      | boolean         |                 |
| led             | tracking        |                 |                 |
+-----------------+-----------------+-----------------+-----------------+

## Filters

<div class="section"><h2 class="title sectiontitle">Filters</h2> <div class="sectiondiv"><p class="p">By logical status (byLogicalStatus)</p>
<div class="p">Params:<table cellpadding="4" cellspacing="0" summary="" border="1" class="simpletable"><tr class="sthead"><th valign="bottom" align="left" id="d5439e1088" class="stentry">Name</th>
<th valign="bottom" align="left" id="d5439e1090" class="stentry">Type</th>
</tr>
<tr class="strow"><td valign="top" headers="d5439e1088" class="stentry">state</td>
<td valign="top" headers="d5439e1090" class="stentry">enumeration</td>
</tr>
</table>

</div>
</div>
 <div class="sectiondiv"><p class="p">By name or label (byText)</p>
<div class="p">Params:<table cellpadding="4" cellspacing="0" summary="" border="1" class="simpletable"><tr class="sthead"><th valign="bottom" align="left" id="d5439e1106" class="stentry">Name</th>
<th valign="bottom" align="left" id="d5439e1108" class="stentry">Type</th>
</tr>
<tr class="strow"><td valign="top" headers="d5439e1106" class="stentry">text</td>
<td valign="top" headers="d5439e1108" class="stentry">string</td>
</tr>
</table>

</div>
</div>
 <div class="sectiondiv"><p class="p">By status (byState)</p>
<div class="p">Params:<table cellpadding="4" cellspacing="0" summary="" border="1" class="simpletable"><tr class="sthead"><th valign="bottom" align="left" id="d5439e1124" class="stentry">Name</th>
<th valign="bottom" align="left" id="d5439e1126" class="stentry">Type</th>
</tr>
<tr class="strow"><td valign="top" headers="d5439e1124" class="stentry">state</td>
<td valign="top" headers="d5439e1126" class="stentry">enumeration</td>
</tr>
</table>

</div>
</div>
 <div class="sectiondiv"><p class="p">By targeting resource (byTargetResource)</p>
<div class="p">Params:<table cellpadding="4" cellspacing="0" summary="" border="1" class="simpletable"><tr class="sthead"><th valign="bottom" align="left" id="d5439e1142" class="stentry">Name</th>
<th valign="bottom" align="left" id="d5439e1144" class="stentry">Type</th>
</tr>
<tr class="strow"><td valign="top" headers="d5439e1142" class="stentry">targetResource</td>
<td valign="top" headers="d5439e1144" class="stentry">string</td>
</tr>
</table>

</div>
</div>
 <div class="sectiondiv"><p class="p">Include advanced landing pages (withAdvanced)</p>
<div class="p">Params:<table cellpadding="4" cellspacing="0" summary="" border="1" class="simpletable"><tr class="sthead"><th valign="bottom" align="left" id="d5439e1160" class="stentry">Name</th>
<th valign="bottom" align="left" id="d5439e1162" class="stentry">Type</th>
</tr>
<tr class="strow"><td valign="top" headers="d5439e1160" class="stentry">advanced</td>
<td valign="top" headers="d5439e1162" class="stentry">boolean</td>
</tr>
</table>

</div>
</div>
 <div class="sectiondiv"><p class="p">Include continuous deliveries from a heterogeneous list (withContinuous)</p>
<div class="p">Params:<table cellpadding="4" cellspacing="0" summary="" border="1" class="simpletable"><tr class="sthead"><th valign="bottom" align="left" id="d5439e1179" class="stentry">Name</th>
<th valign="bottom" align="left" id="d5439e1181" class="stentry">Type</th>
</tr>
<tr class="strow"><td valign="top" headers="d5439e1179" class="stentry">withContinuous</td>
<td valign="top" headers="d5439e1181" class="stentry">boolean</td>
</tr>
</table>

</div>
</div>
 <div class="sectiondiv"><p class="p">Present during given period (byCalendar)</p>
<div class="p">Params:<table cellpadding="4" cellspacing="0" summary="" border="1" class="simpletable"><tr class="sthead"><th valign="bottom" align="left" id="d5439e1197" class="stentry">Name</th>
<th valign="bottom" align="left" id="d5439e1199" class="stentry">Type</th>
</tr>
<tr class="strow"><td valign="top" headers="d5439e1197" class="stentry">startDate</td>
<td valign="top" headers="d5439e1199" class="stentry">date</td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e1197" class="stentry">endDate</td>
<td valign="top" headers="d5439e1199" class="stentry">date</td>
</tr>
</table>

</div>
</div>
 <div class="sectiondiv"><p class="p">Published during given period (byPlanning)</p>
<div class="p">Params:<table cellpadding="4" cellspacing="0" summary="" border="1" class="simpletable"><tr class="sthead"><th valign="bottom" align="left" id="d5439e1220" class="stentry">Name</th>
<th valign="bottom" align="left" id="d5439e1222" class="stentry">Type</th>
</tr>
<tr class="strow"><td valign="top" headers="d5439e1220" class="stentry">startDate</td>
<td valign="top" headers="d5439e1222" class="stentry">date</td>
</tr>
<tr class="strow"><td valign="top" headers="d5439e1220" class="stentry">endDate</td>
<td valign="top" headers="d5439e1222" class="stentry">date</td>
</tr>
</table>

</div>
</div>
</div>