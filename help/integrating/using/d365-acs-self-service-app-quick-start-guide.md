
# Quick Start Guide

This will be a quick start guide to get to the app, configure the credentials, and starting the first workflow.
### Pre-requisites
   - make sure that Dynamics 365 has been configured 
        (click [here](integrating/using/d365-acs-configure-d365.md) to configure)
   - make sure that adobe.io has been configured 
        (click [here](integrating/using/d365-acs-configure-adobe-io.md) to configure)
   - make sure your user has been given access to the Integration App in the Experience Cloud 
        (click [here](integrating/using/d365-acs-self-service-app-control-access.md) for instructions configure)
   - make sure you understand the [Concepts and Restrictions](integrating/using/d365-acs-self-service-app-overview.md#concepts-and-restrictions) associated with the integrations app 
### How to access the integration self-service app   
Open a browser and browse to the connector associated with your region:
   - [Asia Pacific](http://d365-acs-ap.ea.adobe.com/)
   - [Europe, Middle East, or Africa (EMEA)](http://d365-acs-em.ea.adobe.com/)
   - [Americas](http://d365-acs-na.ea.adobe.com/)
   
    >[!NOTE]
    >
    > We suggest that you bookmark this link for future use.
   
### Setting up your credentials   
When you browse to the app for the first time, then you should see a page with a header that looks like this:    

![](assets/d365-to-acs-ui-header.png)

    >[!NOTE]
    >
    > It's normal to get alerts that mention that it's "unable to connect" to Adobe Campaign Standard or 
    > Dynamics 365 if the app settings have not yet been configured.
  
Please verify that the "ORG" and "INSTANCE" selections are the ones you plan on configuring.  If not, then click on them and change the entry to the correction selection.   

    >[!WARNING]
    >
    > If you are configuring the connector for the first time and/or you are new to this process, then 
    > we **strongly** urge you to select the "stage" or "dev" instance.    You'll want to make sure that you verify 
    > that your configuration works well before attempting to work on it in production. 

If you have the correct org and instance, then click on the "hamburger" (i.e. the icon with the three horizontal lines) to expose a drop down menu.   Then click "Settings" in the drop down menu to visit the page where you can enter your credentials into the Integration App (see below).
     
![](assets/d365-to-acs-ui-page-workflows-menu-pointers.png)    

In the Settings page, fill in the information in the following sections: 
* Microsoft Dynamics 365 Credentials
* Adobe Credentials
  
Go [here](d365-acs-self-service-app-settings.md) to find more detailed information about where to find the information  for each input.   When you are done then click the "Save" button at the bottom.   We suggest that you save incrementally  if the process of finding the credential information is taking a long time.  This will prevent loss of data if you have internet connectivity issues.

### Verifying Your ingress configuration

Assuming that you have completed the pre-requisites above and have correctly add all your credentials, let's now navigate to the "Workflows" page.   This is the default page shown when you first enter the Integration app.  If you following the steps above, then this is the page you should have returned to when you clicked "Save" on the credentials. page.

In the Workflows page, click the pencil icon associated with the "Dynamics 365 to Campaign" workflow to edit its configuration.
    
![](assets/d365-to-acs-ui-page-workflows-ingress-edit-pointer.png)
    
You should now see the "Dynamics 365 to Campaign" page (shown below).   This will show the list of the table mappings that you have configured.   It will default you to a contact/profile mapping out-of-the-box.   All other custom entities will need to be configured separately.   For now, we will just focus on the contact/profile mapping.
    
![](assets/d365-to-acs-ui-page-ingress-top-pointers.png)
       
In the "Edit Table Mapping" page, check the Mappings section to ensure that files from Dynamics 365 are being mapped to the correct field in Adobe Campaign.   If you need to add any other mappings then do so now, as well as any replacements or filters.    Please view the detailed documentation [here](integrating/using/d365-acs-self-service-app-ingress-individual-mapping.md) for more information on how to configure this page.

When you are done then click the "Save" button.    As mentioned before, we encourage you to save often if your updates are taking more than a few minutes.

After returning to the "Dynamics 365 to Campaign" page, then you'll need to decide if you want to add more mappings to this list or if you're satisfied with running the connector with just the contact/profile mapping configured.   If you want to learn more about adding new mappings, then click [here](integrating/using/d365-acs-self-service-app-ingress-list.md) for more information on it.   If you are satisfied with just the contact/profile mapping then click the "Return" button to return to the "Workflows" page.

If you feel that your configuration is correct then you could now click the "Play" button next to the "Dynamics 365 to Campaign" workflow in order to start the integration and the flow of data.  Again, we **strongly** recommend that you first run this in your Stage or Dev environments before running in Production.   Please check that the stage/dev intance is selected in the header.

If you feel you are ready to "turn on" the integration then hit the "play" button shown below.   This will initiate a process that will start the connector (note: this can take a few minutes).

![](assets/d365-to-acs-ui-page-workflows-ingress-play-pointer.png)

Once running, then you should be able to test by adding or modifying entries in the Dynamics 365 that you configured and seeing those changes appear in Adobe Campaign within a few minutes.   Remember that it will only map the entries that you configured for each of the Dynamics 365 resources.

If at any time you need to stop this data flow, then simply press the play/stop button to stop it (it's a toggle button that allows you to switch from start to stop).

This was just a quick start guide to get you up-and-running as quick as possible.   We now encourage you to visit the  other documentation related to the Adobe Campaign Standard integration with Dynamics 365 self-service app to gain a  full understanding of how it works and how to configure it in the integration app.   Reference the  [Understanding the User Interface](integrating/using/d365-acs-self-service-app-overview.md#understanding-ui) section in the Overview article for a full listing of the pages related to the user interface.

 