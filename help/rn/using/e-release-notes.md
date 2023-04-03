>[!CAUTION]
>
> This content is subject to changes without prior notice until the stage environments upgrade date. Learn more in the [release planning page](../../rn/using/release-planning.md).
>
## Release 22.3.2 {#dec-22}

### Security update{#rn-security2}

This release comes with the following security upgrade: Debian has been upgraded to v11.0.

## Release 22.3 - Fall/Winter 2022 {#sept-22}

### Security update{#rn-security}

This release comes with the following security upgrade: Apache Tomcat has been upgraded from v7.0 to v8.0.

### Fixes{#e-rn-fixes}

* Fixed an issue with scheduled reports, which were triggered an hour prior to the scheduled timing. (CAMP-51502)
* Fixed an issue on the Delivery indicators in the Delivery dashboard which did not match Sending Logs (nms:broadLogRcp). (CAMP-51127)
* Fixed an issue which prevented custom resources extension with ACS Connector (Prime Offering). (CAMP-51033)
* Improved the publication process for Privacy requests responses to avoid delay. (CAMP-50613)
