---
title: List of functions
seo-title: List of functions
description: List of functions
seo-description: The query editing tool allows you to use advanced functions to carry out complex filtering.
uuid: 4dc28ee4-6b41-4c6b-9c85-a675ec08eac1
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/list-of-functions
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 57.975-0400
cq-lastreplicated: 2018-07-23T05 57 48.765-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: filtering-data
cq-template: /apps/help/templates/article-3
discoiquuid: 1510144e-f986-4c27-8d24-8d15d92991b4
firstPublishExternalDate: 2018-07-23T05:57:48.648-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 03 11.921-0400
jcr-createdby: admin
jcr-description: List of functions
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:48.648-0400
lochandoffdate: 2018-07-25T09 29 57.975-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: List of functions
publishexternaldate: 2018-07-23T05 57 48.648-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/list-of-functions.html
sha1: 0744dbaa57298dfd4f2471a57ccc5836168bfc08
topicBrowsingSortDate: 2018-07-23T05:57:48.648-0400
index: y
internal: n
snippet: y
---

# List of functions

List of functions

## About functions

The query editing tool allows you to use advanced functions to carry out complex filtering. To do this, the tool palette contains the **Expression** element that you can use in the workspace. Further information on this element is detailed in a [specific section](../../automating/using/advanced-expression-editing.md).

This element allows you to enter your conditions manually. Here you can use the functions defined in the following sections.

Several function types are available, depending on the desired results and the types of manipulated data:

* Dates
* Geomarketing
* Numerical values
* Other functions
* Aggregates
* String manipulation
* Sorting

## Dates

The date functions are used to manipulate date or time values. 
||||
|--- |--- |--- |
|Name|Description|Syntax|
|AddDays|Adds a number of days to a date|AddDays(<date>, <number>)|
|AddHours|Adds a number of hours to a date|AddHours(<date>, <number>)|
|AddMinutes|Adds a number of minutes to a date|AddMinutes(<date>, <number>)|
|AddMonths|Adds a number of months to a date|AddMonths(<date>, <number>)|
|AddSeconds|Adds a number of seconds to a date|AddSeconds(<date>, <number>)|
|AddYears|Adds a number of years to a date|AddYears(<date>, <number>)|
|DateOnly|Returns the date only (with time at 00:00)|DateOnly(<date>)|
|Day|Returns the number representing the day of the date|Day(<date>)|
|DayOfYear|Returns a number representing the day in the year of the date|DayOfYear(<date>)|
|DaysAgo|Returns the current date minus n days|DaysAgo(<number>)|
|DaysAgoInt|Returns the current date minus n days (as an integer yyyymmdd)|DaysAgoInt(<number>)|
|DaysDiff|Number of days between two dates|DaysDiff(<end date>, <start date>)|
|DaysOld|Returns the age in days of a date|DaysOld(<date>)|
|GetDate|Returns the current system date of the server|GetDate()|
|Hour|Returns the hour of the date|Hour(<date>)|
|HoursDiff|Returns the number of hours between two dates|HoursDiff(<end date>, <start date>)|
|LocalToUTC|Converts a local date and time to UTC|LocalToUTC(<date>, <Time Zone>)|
|Minute|Returns the minutes of the date|Minute(<date>)|
|MinutesDiff|Returns the number of minutes between two dates|MinutesDiff(<end date>, <start date>)|
|Month|Returns the number representing the month of the date|Month(<date>)|
|MonthsAgo|Returns the date corresponding to the current date minus n months|MonthsAgo(<number>)|
|MonthsDiff|Returns the number of months between two dates|MonthsDiff(<end date>, <start date>)|
|MonthsOld|Returns the age in months of a date|MonthsOld(<date>)|
|Second|Returns the seconds of the date|Second(<date>)|
|Oldest|Returns the oldest date|Oldest(<Date>, <Date>)|
|SecondsDiff|Returns the number of seconds between two dates|SecondsDiff(<end date>, <start date>)|
|SubDays|Subtracts a number of days from a date|SubDays(<date>, <number>)|
|SubHours|Subtracts a number of hours from a date|SubHours(<date>, <number>)|
|SubMinutes|Subtracts a number of minutes from a date|SubMinutes(<date>, <number>)|
|SubMonths|Subtracts a number of months from a date|SubMonths(<date>, <number>)|
|SubSeconds|Subtracts a number of seconds from a date|SubSeconds(<date>, <number>)|
|SubYears|Subtracts a number of years from a date|SubYears(<date>, <number>)|
|ToDate|Converts a date + time as a date|ToDate(<date + time>)|
|ToDateTime|Converts a string to a date + time|ToDateTime(<string>)|
|TruncDate|Rounds a date+time to the nearest second|TruncDate(@lastModified, <number of seconds>)|
|TruncDateTZ|Rounds a date + time to a given precision expressed in seconds|TruncDateTZ(<date>, <number of seconds>, <time zone>)|
|TruncQuarter|Rounds a date off to the quarter|TruncQuarter(<date>)|
|TruncTime|Rounds the time part up to the nearest second|TruncTime(<date>, <number of seconds>)|
|TruncWeek|Rounds a date off to the week|TruncWeek(<date>)|
|TruncYear|Rounds a date + time to January 1st of the year|TruncYear(<date>)|
|WeekDay|Returns the number representing the day in the week of the date|WeekDay(<date>)|
|Year|Returns the number representing the year of the date|Year(<date>)|
|YearAnd Month|Returns the number representing the year and month of the date|YearAndMonth(<date>)|
|YearsDiff|Returns the number of years between the two dates|YearsDiff(<end date>, <start date>)|
|YearsOld|Returns the age in years of a date|YearsOld(<date>)|


## Geomarketing

The geomarketing functions are used to manipulate geographical values. 

||||
|--- |--- |--- |
|Name|Description|Syntax|
|Distance|Returns the distance between two points defined by their longitude and latitude, expressed in degrees|Distance(<Longitude A>, <Latitude A>, <Longitude B>, <Latitude B>)|


## Numerical

The numerical value functions are used to convert text to numbers. 

||||
|--- |--- |--- |
|Name|Description|Syntax|
|Abs|Returns the absolute value of a number|Abs(<number>)|
|Ceil|Returns the lowest integer greater than or equal to a number|Ceil(<number>)|
|Floor|Returns the greatest integer greater than or equal to a number|Floor(<number>)|
|Greatest|Returns the greater of two numbers|Greatest(<number 1>, <number 2>)|
|Least|Returns the smaller of two numbers|Least(<number 1>, <number 2>)|
|Mod|Returns the remainder of the integer division from n1 by n2|Mod(<number 1>, <number 2>)|
|Percent|Returns the ratio of two numbers expressed as a percentage|Percent(<number 1>, <number 2>)|
|Random|Returns the random value|Random()|
|Round|Rounds off a number to n decimals|Round(<number>, <number of decimals>)|
|Sign|Returns the sign of the number|Sign(<number>)|
|ToDouble|Converts an integer to a float|ToDouble(<number>)|
|ToInt64|Converts a float to a 64 bit integer|ToInt64(<number>)|
|ToInteger|Converts a float to an integer|ToInteger(<number>)|
|Trunc|Truncates n1 to n2 decimals|Trunc(<n1>, <n2>)|

## Others

This table contains the remaining functions avalaible. 

||||
|--- |--- |--- |
|Name|Description|Syntax|
|Case|Returns value 1 if the condition is verified. Otherwise, returns value 2|Case(When(<condition>, <value 1>), Else(<value 2>))|
|ClearBit|Deletes the Flag in the value|ClearBit(<identifier>, <flag>)|
|Coalesce|Returns value 2 if value 1 is zero or null, otherwise returns value 1|Coalesce(<value 1>, <value 2>)|
|Decode|Returns value 3 is value 1 = value 2, otherwise returns 4|Decode(<value 1>, <value 2>, <value 3>, <value 4>)|
|Else|Returns value 1 (may only be used as a parameter of the case function)|Else(<value 1>)|
|GetEmailDomain|Extracts the domain from an email address|GetEmailDomain(<value>)|
|GetMirrorURL|Retrieves the URL of the mirror page server|GetMirrorURL(<value>)|
|Iif|Returns value 1 if the expression is true, otherwise returns value 2|Iif(<condition>, <value 1>, <value 2>)|
|IsBitSet|Indicates whether the Flag is in the value|IsBitSet(<identifier>, <flag>)|
|IsEmptyString|Returns value 2 if the string is empty, otherwise returns value 3|IsEmptyString(<string>, <value 2>, <value 3>)|
|NoNull|Returns the empty string if the argument is NULL|NoNull(<value>)|
|RowId|Returns the line number|RowId|
|SetBit|Forces the Flag in the value|SetBit(<identifier>, <flag>)|
|SetVar|Sets a variable|SetVar(<variable>, <expression>)|
|ToBoolean|Converts a number into a Boolean|ToBoolean(<number>)|
|When|Returns value 1 if the expression is verified. Otherwise, returns value 2 (may only be used as a parameter of the case function)|When(<condition>, <value 1>)|
|newUUID|Returns a new UUID.|newUUID|


## String

The string functions are used to manipulate a set of strings.

||||
|--- |--- |--- |
|Name|Description|Syntax|
|AllNonNull2|Indicates if all parameters are non-null and not empty|AllNonNull2(<string>, <string>)|
|AllNonNull3|Indicates if all parameters are non-null and not empty|AllNonNull3(<string>, <string>, <string>)|
|ASCII|Returns the ASCII value of the first character in the string|Ascii(<string>)|
|Char|Returns the character corresponding to the 'n' ASCII code|Char(<number>)|
|Charindex|Returns the position of string 2 in string 1|Charindex(<string>, <string>)|
|DataLength|Returns the number of characters in a string|DataLength(<String>)|
|GetLine|Returns the nth (from 1 to n) line of the string|GetLine(<string>)|
|IfEquals|Returns the third parameter if the first two parameters are equal otherwise returns the last parameter|IfEquals(<string>, <string>, <string>, <string>)|
|IsMemoNull|Indicates if the memo passed as a parameter is null|IsMemoNull(<Memo>)|
|JuxtWords|Concates the two strings passed as parameters. A space is added between each string in the returned value.|JuxtWords(<string>, <string>)|
|JuxtWords3|Concates the three strings passed as parameters. A space is added between each string in the returned value.|JuxtWords3(<string>, <string>, <string>)|
|LPad|Returns the completed string on the left|LPad(<string>, <number>, <caractère>)|
|Left|Returns the first n characters of the string|Left(<string>, <number>)|
|Length|Returns the string length|Length(<string>)|
|Lower|Returns the string in lowercase|Lower(<string>)|
|Ltrim|Removes spaces to the left of the string|Ltrim(<string>)|
|Md5Digest|Returns an hexadecimal representation of the MD5 key of a string|Md5Digest(<string>)|
|MemoContains|Specifies whether the memo contains the string passed as a parameter|MemoContains(<memo>, <string>)|
|RPad|Returns the completed string on the right|RPad(<string>, <number>, <character>)|
|Replace|Replaces all occurrences of a specified string (2nd parameter) value with another string value (3rd parameter) in a string (1st parameter)|Replace(<String>, <String>, <String>)|
|Right|Returns the last n characters of the string|Right(<string>)|
|Rtrim|Removes spaces to the right of the string|Rtrim(<string>)|
|Sha256Digest|Calculates the standard SHA256 hash for a given UTF8 string|Sha256Digest(<String>)|
|Sha384Digest|Calculates the standard SHA384 hash for a given UTF8 string|Sha384Digest(<String>)|
|Sha512Digest|Calculates the standard SHA512 hash for a given UTF8 string|Sha512Digest(<String>)|
|Smart|Returns the string with the first letter of each word in capitals|Smart(<string>)|
|Substring|Extracts the sub-string starting at character n1 of the string and with a length of n2|Substring(<string>, <offset>, <length>)|
|ToIntlString|Converts the number to a string|ToIntlString(<number>)|
|ToString|Converts the number to a string|ToString(<number>)|
|Upper|Returns the string in capitals|Upper(<string>)|
|VirtualLink|Returns the foreign key of a link passed as a parameter if the other two parameters are equal|VirtualLink(<number>, <number>, <number>)|
|VirtualLinkStr|Returns the foreign (text) key of a link passed as a parameter if the other two parameters are equal|VirtualLinkStr(<string>, <number>, <number>)|
|encryption_aescbcDecrypt|Decrypts an encrypted value in HEX format with "x" prefix (1st parameter) using a key in HEX format (2nd parameter) and an initialization vector in HEX format (3rd parameter)|encryption_aescbcDecrypt(<String>, <String>, <String>)|
|encryption_aescbcEncrypt|Encrypts an UTF8 value (1st parameter) to HEX format without "x" prefix using a key in HEX format (2nd parameter) and an initialization vector in HEX format (3rd parameter) For example: encryption_aescbcEncrypt(johndoe@example.com, "x0123456789ABCDEF0123456789ABCDEF", "x0123456789ABCDEFFEDCBA9876543210")|encryption_aescbcEncrypt(<String>, <String>, <String>)|


## Aggregates

The aggregation functions are only available when [adding additional data](../../automating/using/query.md#enriching-data) from a workflow's **Query** activity.

The aggregate functions are used to perform calculations on a set of values.

||||
|--- |--- |--- |
|Name|Description|Syntax|
|Avg, Average|Returns the average in a numerical column.|Avg(<value>)|
|Count, Count (except NULL)|Counts the non-null values in a column.|Count(<value>)|
|CountAll, Count all|Counts all of the values (including null values and duplicates).|CountAll()|
|Countdistinct, Distinct count|Counts the non-null, distinct values in a column.|Countdistinct(<value>)|
|Max, Max|Returns the maximum value in a numerical, string, or date column.|Max(<value>)|
|Min, Min|Returns the minimum value in a numerical, string, or date column.|Min(<value>)|
|Sum, Sum|Returns the sum of the values in a numerical column.|Sum(<value>)|


## Representation

The representation functions are used to order values. 

||||
|--- |--- |--- |
|Name|Description|Syntax|
|Desc|Applies a descending sort|Desc(<value 1>)|
|OrderBy|Sorts the result within the partition|OrderBy(<value 1>)|
|PartitionBy|Partitions the result of a query on a table|PartitionBy(<value 1>)|
|RowNum|Generates a line number based on the table partition and on a sorting sequence. This function is not supported for MySQL|RowNum(PartitionBy(<value 1>), OrderBy(<value 1>))|
