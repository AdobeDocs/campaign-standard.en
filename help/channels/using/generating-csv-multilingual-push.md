---
title: Generating a CSV file for Multilingual Push Notification with Campaign Standard
description: Uploading a CSV file to generate content for delivery is a feature used to support Multilingual Push notifications.
page-status-flag: never-activated
uuid: e90f4ec8-14e3-4304-b5fc-bce0ba08a4ef
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: email-messages
discoiquuid: 79231445-1d51-499a-adcf-0c0f6db1cfa3

internal: n
snippet: y
---

# Generating a CSV file for Multilingual Push Notification{#generating-csv-multilingual-push}

Uploading a CSV file to generate content for delivery is a feature used to support multilingual Push notifications. The format of the CSV file needs to adhere to certain guidelines for the file upload to be successful and consequently to be able to create a delivery. The following sections describe the file format and the considerations thereof.

## File format {#file-format}

Multilingual push requires 14 columns in the CSV file:

* title
* messageBody
* sound
* badge
* deeplinkURI
* category
* iosMediaAttachmentURL
* androidMediaAttachmentURL
* isContentAvailable
* isMutableContent
* customFields
* locale
* language
* silentPush

![](assets/multilingual_push_1.png)

Check the CSV sample by clicking the **[!UICONTROL Download a sample file]** in the **[!UICONTROL Manage Content Variants]** window. For more on this, refer to the this [section](../../channels/using/creating-a-multilingual-push-notification.md).

* **title, messageBody, sound, badge, deeplinkURI, category, iosMediaAttachmentURL, androidMediaAttachmentURL**: regular push payload contents. You need to provide this information in a similar manner as when creating push deliveries.
* **Custom Fields**:  use JSON format for the custom fields, e.g. `{"key1":"value1","key2":"value2"}`. Refer to the sample file above for an example of custom fields.
* **isContentAvailable**: flag for Content Available check, value 1 implies true, value 0 implies false. The default value is 0. If you leave this column blank, the value will be considered 0.
* **isMutableContent**: flag for Mutable Content, value 1 implies true, value 0 implies false. The default value is 0. If you leave this column blank, the value will be considered 0.
* **locale**: locale is the field for language variants, e.g. "en_us" for US-English and "fr_fr" for France-French.
* **language**: name of the language which is associated with the locale. For example, if locale is "en_us", the name of the language should be " English-United States".
* **silentPush**: flag for the push notification type. If it is a regular push notification, the value should be 0. If it is a silent push, the value should be 1. The default value is 0. If you leave this column blank, the value will be considered 0.

## Constraints and Guidelines for the creation of csv file {#constraints-guideline-csv}

**Name of each column is fixed**.
You should include the name of each column in the CSV file, if you don't use any columns for the content, leave it blank.

**"locale" and "language" columns are mandatory and value is unique for each row.** 
A blank value for this column will result in a failure of the file upload.

**Order of columns matters**. The order of the columns in the uploaded file needs to follow the same format as the sample file.

**Quote column content**. Since this is a CSV (stands for Comma-Separated Values) file, any column content which includes comma (,) has to be quoted. For example, "Hello, Tom!"

**UTF-8 encoding is necessary for international characters.**

**If you generate the file by plain text, separate each column by ",".**

**Variant Mismatch.** If you use content block and target audiences with specific languages, you need to list every targeted language in your CSV file or you will get error when sending the delivery.

## Insertion of personalization field in the csv file {#personalization-field-csv}

If you want to use personalization fields, you should include <span> tag in the file.

To insert "firstName" personalization field in messageBody, the message needs to be:

```

 "Hello <span class="nl-dce-field nl-dce-done"  data-nl-expr="/context/profile/firstName">First name</span>, this is message".

```

"firstName" field is represented by:

```

 <span class="nl-dce-field nl-dce-done" data-nl-expr="/context/profile/firstName">First name</span>

```

In the span there are two mandatory attributes:

* One is class which is static. No matter which personalization field you plan to use, it will always be class="nl-dce-field nl-dce-done".

* Another one is data-nl-expr which is the path of personalization field. For example, if you insert "firstName" personalization field from UI, the navigation path will be **[!UICONTROL Context (context)]** > **[!UICONTROL Profile (profile)]** > **[!UICONTROL First name (firstName)]** (as shown in the image below). In this case, the path will be

   ```

   /context/profile/firstName. data-nl-expr="/context/profile/firstName".

   ```

![](assets/multilingual_push_2.png)

## Locale and Language Names {#locale-language-names}

The following languages are supported:

| locale  |  language |
|:-:|:-:|
| af_za  | Afrikaans - South Africa |
| sq_al  |  Albanian - Albania |
|  ar_dz | Arabic - Algeria  |
| ar_bh   | Arabic - Bahrain  |
|  ar_iq | Arabic - Iraq  |
|  ar_il | Arabic - Israel   |
|  ar_jo | Arabic - Jordan  |
| ar_kw |  Arabic - Kuwait |
|  ar_lb |  Arabic - Lebanon |
|  ar_ma | Arabic - Morocco  |
| ar_om  |  Arabic - Oman |
|  ar_qa | Arabic - Qatar  |
|  ar_sa | Arabic - Saudi Arabia  |
|  ar_sy | Arabic - Syria  |
|  ar_tn |  Arabic - Tunisia |
| ar_ae  | Arabic - United Arab Emirates |
| ar_ye  | Arabic - Yemen  |
|  hy_am |  Armenian - Armenia |
| az_az  |  Azeri - Azerbaijan |
|  be_by | Belarussian - Belarus  |
|  bs_ba |  Bosnian - Bosnia |
|  bg_bg |  Bulgarian - Bulgaria |
| ca_es| Catalan - Spain  |
|  zh_cn | Chinese (Simplified) - China  |
|  zh_sg |  Chinese (Simplified) - Singapore |
| zh_hk  | Chinese (Traditional) - Hong Kong SAR of China  |
|  zh_tw | Chinese (Traditional) - Taiwan region  |
|  hr_hr |  Croatian - Croatia |
|  cs_cz|   Czech - Czechia |
|  da_dk | Danish - Denmark  |
|  nl_be | Dutch - Belgium  |
| nl_nl  | Dutch - Netherlands  |
| en_au  | English - Australia  |
| en_bz |   English - Belize |
|  en_ca | English - Canada  |
| en_in  | English - India  |
| en_ie  | English - Ireland  |
| en_jm | English - Jamaica  |
|  en_nz | English - New Zealand  |
|  en_ph |  English - Philippines |
|  en_za | English - South Africa  |
|  en_tt | English - Trinidad and Tobago  |
| en_gb  | English - United Kingdom  |
|  en_us | English - United States  |
| en_zw  | English - Zimbabwe  |
|  et_ee | Estonian - Estonia  |
| fi_fi  | Finnish - Finland  |
|  fr_be | French - Belgium  |
| fr_ca  |  French - Canada |
| fr_fr | French - France  |
|  fr_lu | French - Luxembourg  |
| fr_ch  |  French - Switzerland |
|  de_at| German - Austria   |
|  de_de |  German - Germany |
| de_lu  | German - Luxembourg  |
|  de_ch | German - Switzerland  |
| el_cy  |  Greek - Cyprus |
|  el_gr | Greek - Greece  |
|  gu_in | Gujarati - India  |
|  he_il |  Hebrew - Israel |
|  hi_in |  Hindi - India |
|  hu_hu | Hungarian - Hungary  |
| is_is  |  Icelandic - Iceland |
| id_id  |  Indonesian - Indonesia |
| it_it  | Italian - Italy  |
|  it_ch|  Italian - Switzerland  |
| ja_jp  | Japanese - Japan  |
|  kn_in | Kannada - India  |
| kk_kz  | Kazakh - Kazakhstan  |
|  ko_kr |  Korean - South Korea |
| lv_lv  | Latvian - Latvia  |
| lt_lt  |  Lithuanian - Lithuania |
| mk_mk  |  Macedonian - Macedonia |
| ms_my |   Malay - Malaysia |
| mr_in  |  Marathi - India |
| no_no  | Norwegian - Norway  |
|  pl_pl| Polish - Poland   |
| pt_br  |  Portuguese - Brazil |
|  pt_pt |  Portuguese - Portugal |
| pa_in  | Punjabi - India  |
| ro_md  |  Romanian - Moldova |
|  ro_ro | Romanian - Romania  |
|  ru_kz |  Russian - Kazakhstan |
| ru_ru  | Russian - Russia  |
|  ru_ua |  Russian - Ukraine |
|  a_in | Sanskrit - India |
|  sr_ba|  Serbian - Bosnia |
| sr_rs |  Serbian - Serbia  |
|  sk_sk | Slovak - Slovakia  |
| sl_si | Slovenian - Slovenia  |
| es_ar  |  Spanish - Argentina |
|  es_bo | Spanish - Bolivia  |
| es_cl  |  Spanish - Chile |
|  es_co | Spanish - Colombia  |
| es_cr  |  Spanish - Costa Rica |
|  es_do | Spanish - Dominican Republic  |
|  es_ec | Spanish - Ecuador  |
| es_sv  | Spanish - El Salvador  |
|  es_gt | Spanish - Guatemala  |
| es_hn  | Spanish - Honduras  |
| es_mx  | Spanish - Mexico  |
| es_ni  | Spanish - Nicaragua  |
| es_pa  | Spanish - Panama  |
| es_py  | Spanish - Paraguay  |
| es_pe | Spanish - Peru   |
|  es_pr| Spanish - Puerto Rico   |
|  es_es |  Spanish - Spain |
|  es_uy | Spanish - Uruguay  |
| es_ve  | Spanish - Venezuela  |
| sw_ke  | Swahili - Kenya  |
| sv_fi  |  Swedish - Finland |
|  sv_se | Swedish - Sweden  |
| ta_in  | Tamil - India  |
|  tt_ru | Tatar - Russian  |
|  te_in |  Telugu - India |
|  th_th | Thai - Thailand  |
| tr_cy  | Turkish - Cyprus  |
|  tr_tr |  Turkish - Turkey |
|  uk_ua | Ukrainian - Ukrain  |
|  ur_in |  Urdu - India |
| ur_pk | Urdu - Pakistan  |
|  vi_vn | Vietnamese - Vietnam  |
