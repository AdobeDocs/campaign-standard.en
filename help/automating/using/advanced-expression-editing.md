---
title: Advanced expression editing
seo-title: Advanced expression editing
description: Advanced expression editing
seo-description: The query edition wizard allows you to define advanced expressions.
uuid: 5fe10282-bf13-463a-bd46-a592ee65408e
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/advanced-expression-editing
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 57.424-0400
cq-lastreplicated: 2018-07-23T05 57 46.386-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: filtering-data
cq-template: /apps/help/templates/article-3
discoiquuid: ceffd5bc-ba36-4086-82a7-b0b0b954b666
firstPublishExternalDate: 2018-07-23T05:57:46.292-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 26.316-0400
jcr-createdby: admin
jcr-description: Advanced expression editing
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:46.292-0400
lochandoffdate: 2018-07-25T09 29 57.424-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Advanced expression editing
publishexternaldate: 2018-07-23T05 57 46.292-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/advanced-expression-editing.html
sha1: 64fa365c417520ce48ce772820c494865296e097
topicBrowsingSortDate: 2018-07-23T05:57:46.292-0400
index: y
internal: n
snippet: y
---

# Advanced expression editing

Advanced expression editing

## About advanced expression editing

Editing an expression involves manually entering conditions to form a rule.

This mode allows you to use advanced functions. These functions let you manipulate the values used to carry out specific queries such as manipulating dates, strings, numerical fields, sorting, etc.

You can edit expressions in order to:

* Define a query, via the **Advanced mode** option which is available when a rule is added.

  ![](assets/expression_editor_2.png)

* Edit an expression in a workflow. For example, to add additional data to an activity.
* Edit a visibility condition to define how a block in the HTML content editor is displayed. In this case, the expression is edited in JavaScript format and does not offer the use of advanced functions as standard.

## Edit an expression

Advanced expression edition lets you manually define an expression that corresponds specifically to your needs.

Editing expressions can be used in the Audience window while creating an email or in a Query activity while creating a workflow.

1. Access the expression editing window via one of the methods detailed in the [About advanced expression editing](../../automating/using/advanced-expression-editing.md#about-advanced-expression-editing) section. It involves the following elements:

    * An input field in which the expression is defined.
    * The list of available fields that can be used in the expression and correspond to the targeting dimension of the query (see [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources)).
    * The list of available functions, sorted by category.

   ![](assets/expression_editor_1.png)

1. Edit the expression by entering an expression directly in the corresponding field or by using the lists of available fields and functions.

   Double clicking a field or an expression adds it to the expression in which the cursor is placed.

1. Give your rule a specific name if needed. The name entered will appear as the rule name in the query editor workspace.

Editing an expression lets you personalize the Audiences expression to target your population as needed.

**Related Topics:**

* [Expression Syntax](../../automating/using/advanced-expression-editing.md#expression-syntax)
* [List of functions](../../automating/using/list-of-functions.md)

## Expression Syntax

### Standard syntax

The standard expressions are made up of one or several conditions that respect the following syntax elements:

* Each condition takes the form of **&lt;value1&gt; &lt;comparison operator&gt; &lt;value2&gt;** whereby:

    * **&lt;value1&gt;** is a field or a function. For example **@created** for the date a profile was created or **Year(@created)** for the year a profile was created.
    * **&lt;comparison operator&gt;** is one of the operators listed in the [Comparison operators](../../automating/using/advanced-expression-editing.md#comparison-operators) section. This operator defines the comparison method between **&lt;value1&gt;** and **&lt;value2&gt;**.
    * **&lt;value2&gt;** is a field, a function, or a value inputted manually.

  >[!NOTE]
  >
  >The **&lt;value1&gt;** and **&lt;value2&gt;** type data must be identical. For example, if **&lt;value1&gt;** is a date, then **&lt;value2&gt;** must also be a date.

* If you would like to use several conditions, they can be combined using logical operators.

    * **AND**: two conditions are intersected.
    * **OR**: two conditions are combined.

For example:

```
Year(@created) = Year(GetDate()) AND Month(@created) = Month(GetDate())
```

In this example, the profiles whose creation date is in the current month and year are targeted.

### JavaScript syntax

When defining the visibility conditions of a text type block of the HTML content editor, you must use an expression with JavaScript type syntax.

JavaScript expressions are made up of one or multiple conditions, and they use the following syntax elements:

* Each condition takes the form of **&lt;context&gt; &lt;comparison operator&gt; &lt;value2&gt;** whereby:

    * **&lt;context&gt;** is a field or a function that allows you to specify the context. For example **context.profile.@email** for a profile's email address or **context.profile.firstName.length()** for the number of characters of a profile's first name.
    * **&lt;comparison operator&gt;** is one of the operators listed in the [Comparison operators](../../automating/using/advanced-expression-editing.md#comparison-operators) section. This operator defines the comparison method between **&lt;context&gt;** and **&lt;value2&gt;**.
    * **&lt;value2&gt;** is a field, a function, or a value inputted manually.

  >[!NOTE]
  >
  >The **&lt;context&gt;** and **&lt;value2&gt;** type data must be identical. For example, if **&lt;context&gt;** is a date, then **&lt;value2&gt;** must also be a date.

* If you would like to use several conditions, they can be combined using logical operators.

    * **&&**: two conditions are intersected.
    * **||**: two conditions are combined.

For example:

```
context.profile.age > 21 && context.profile.firstName.length() > 0
```

In this example, profiles older than 21 years of age and whose first name has been provided (symbolized by the fact that the **firstName** field contains at least one character).

## Comparison operators

For some rules, the query editor lets you chose a value to define your condition.

Conditions must be linked to values by using one of the following operators.

|Operator|Standard syntax|JavaScript syntax|Description|Example|
|--- |--- |--- |--- |--- |
|Equal to|=|==|The first value must be completely identical to the second value.|@lastName = Martin retrieves profiles whose last name is 'Martin', with only these identical characters.|
|Greater than|>|>|The first value must categorically be more than the second value.|@age > 50 retrieves profiles who are older than '50', so '51', '52', etc.|
|Less than|<|<|The first value must categorically be less than the second value.|@created < DaysAgo(100) retrieves all profiles created in the database less than 100 days ago.|
|Greater than or equal to|>=|>=|The first value must be more than or equal to the second value.|@age >= 30 retrieves profiles aged 30 years and older.|
|Less than or equal to|<=|<=|The first value must be less than or equal to the second value.|@age <= 60 retrieves profiles aged 60 or less.|
|Different|!=|!=|The first value must be different from the second value.|@language != English retrieves profiles that have not been defined as English speaking.|
|Contains|IN|N/A|The first value must contain the second value.|@domain IN mail. Here, all the domain names with the 'mail' value are returned in the result. Consequently, the 'gmail.com' domain name will make up part of the returned results.|
|Like|LIKE|N/A|Like is very similar to the Contains operator. It lets you insert a % wild card character in the value that is being searched.|@lastName LIKE Mart%n. Here, the substitution character % serves as a "joker" to find the name "Martin" in the hypothetical case that the spelling is not correct.|
|Not like|NOT|N/A|Is similar to Like. It lets you not recover the entered value. Here too, the entered value must contain the % wild card character.|@lastName NOT Smi%h. Here, the recipients correspond to the name 'Smi%h' (so Smith, etc.) are not returned as a result.|
|Is empty|IS NULL|N/A|The first value must correspond to an empty value.|@mobilePhone IS NULL retrieves all the profiles whose mobile phone number has not been provided.|

