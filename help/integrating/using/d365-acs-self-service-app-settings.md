---
title: Egress Workflow
description: Egress Workflow
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
---

#Settings Screen

The Settings screen allows you to specify Dynamics 365 and Adobe API credentials.   There are also inputs to add specifics related to the Adobe Campaign SFTP instance.

## Microsoft Dynamics 365 Credentials

The Microsoft Dynamics 365 Credentials give the integration application permission to pull your data from Microsoft Dynamics 365.  You must first follow the steps on the screen 
"[Configure Dynamics 365 for Campaign integration](integrating/using/d365-acs-configure-d365.md)" 
in order to generate the values that will be pasted into this screen.   The inputs described below will reference this screen.

![](assets/d365-to-acs-ui-page-workflows-settings-d365.png)

* <u>Client ID</u>: Reference the section "Register a new application" in the screen referenced above in order to 
   determine your Client ID.  

* <u>Client Secret</u>: Reference the section "Generate client secret" in the screen referenced above in order to get 
   your client secret.
   
* <u>Tenant</u>: Reference the section "Get the tenant ID" in the screen above to determine how to find your Tenant.

* <u>URL</u>: The url will have the format https://<i>&lt;servername&gt;</i>.api.crm.dynamics.com/.   


## Adobe Credentials

The Adobe Campaign credentials are generated using adobe.io.  You will need to visit the screen [Configure Adobe I/O](integrating/using/d365-acs-configure-adobe-io.md) and follow the instructions there before you will be able to fill out the inputs in this section.

The following image will explain in detail the mapping between adobe.io and the settings screen inputs.
 
![](assets/d365-to-acs-ui-page-workflows-settings-adobeio.png)

* <u>Private Key</u>: the process to to define this starts by clicking the "Generate public/private keypair" button.   This will create a zip file that you must download.   Once you download it then unzip the file which will result in two files named certificate_pub.crt and private.key.   Make sure to put the private.key is a secure place and don't share it. Open the private.key file in a text editor.  Copy the entire value in the text editor (ctrl-A then ctrl-C on a PC, or  cmd-A then cmd-C on a Mac).   This should include the lines with "BEGIN PRIVATE KEY" and "END PRIVATE KEY" in their entirety.   Paste this entire, multi-line text into the "Private Key" input in the Settings screen.

* <u>URL</u>: This value will fit the pattern https\://mc.adobe.io/<i>&lt;campaign-instance-name&gt;</i>.   The header of the integration app includes both the "Org" and "Instance".   The "campaign-instance-name" portion of the url would simply be the name found in this instance value.
  

## Optional Adobe Campaign SFTP Settings

As the title implies, this section only needs to be defined if you plan on using the Adobe Campaign SFTP instance.  One reason to use the SFTP instance is if you ever want to output logs from the connector.  This will be helpful if you experience issues when the integration is running and you need to debug why the output does not meet your  expectations.   The other reason to setup the SFTP server would be if you plan on running the Opt in/out workflow and there is a flow of data from Adobe Campaign to Dynamics 365 (either "Unidirectional Adobe Campaign to Dynamics 365" or "Bidirectional").

![](assets/d365-to-acs-ui-page-workflows-settings-sftp.png)

* <u>SFTP Host</u>: This will look like this:  <i>&lt;campaign-instance-name&gt;</i>.campaign.adobe.com.   The header of the integration app includes both the "Org" and "Instance".   The "campaign-instance-name" portion of the url would simply be the name found in this instance value.
  
* <u>SFTP User</u>: If you have the SFTP user, add it here.  If you don't, then see the "SFTP Setup in Adobe Campaign Standard" section below.   As part of the process, you will be shown the username.

* <u>SFTP Key</u>: If you have an SSH Key, add it here.   If you don't, then see the "SFTP Setup in Adobe Campaign Standard" section below.

* The *IP Ranges* will be needed to be included in your Adobe Campaign Standard SFTP configuration.   These will need to be whitelisted in order for the integration to make use of the SFTP endpoint.  

* The "Do you want to export logs to your Adobe Campaign SFTP?" allows you to determine if the integration will output logging information to the SFTP endpoint.   This can be used to help with debugging if Campaign or Dynamics 365 isn't showing the information you are expecting.

## SFTP Setup in Adobe Campaign Standard

Visit [this page](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/monitoring-server-capacity.html?lang=en#sftp-management) for information about the Adobe Campaign Standard SFTP server.   There are pages that describe the IP Ranges, generating SSH Key, and connecting to the SFTP Server.   You can also supplement these with the instructions below:

1. Browse to the Experience Cloud
1. select the org (in the top-right dropdown)
1. Click on Campaign
1. Click "Control Panel" (instead of selecting a Campaign Instance)
1. In the "SFTP" card, click the "Manage" button
1. In the "Instance List" dropdown (near the top-right), select stage instance
1. Click the "Key Management" tab
1. Click "Add new public key" button
1. On your local, open up file associated with the SSH public key and copy it
    1. Go [here](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/generate-ssh-key.html?lang=en#sftp-management) if you want to see how to generate an SSH Key.
    1. In the browser, paste the public key into the "Public Key" field in the modal window
    1. Click the "Save" button
1. Click on the "Add PI to allow list" button
1. Adding IP Range
    1. Note: You can get the "IP Ranges" from them inputs in the Settings screen (see description above) 
    1. click on the "Add new IP Range"
        1. Add the first "IP Range" for prod
        1. Give it a label that will be clear if it's dev, stage, or prod and an index 1 (ex: "d365-int-prod-1").
        1. Click the "Save" button 
    1. click on the "Add new IP Range"
        1. Add the second "IP Range" for prod
        1. Give it a label that will be clear if it's dev, stage, or prod and the index 2 (ex: "d365-int-prod-2").
        1. Click the "Save" button 
1. Log into the SFTP server with the private key and create the directory "d365_loads/exports"