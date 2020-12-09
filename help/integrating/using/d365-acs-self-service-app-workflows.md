# Workflows

The Workflows screen in the integration application UI lists the three workflows available, gives you the ability to edit them, and allows you to start and stop them.   This documentation will explain how this screen works; however, it assumes that you understand the basics of these workflows.   If you don't fully understand them, then it is recommended that you  visit the [Data Flows](using-the-campaign-standard-and-microsoft-dynamics-365-integration.md#data-flows) section in the "Use the Microsoft Dynamics 365 integration"" documentation page.

![](assets/d365-to-acs-ui-page-workflows.png)

The Workflows page list the three workflows with the fo:
* Dynamics 365 to Campaign (a.k.a. "Ingress")
* Campaign to Dynamics 365 (a.k.a. "Egress")
* Opt In/Out

Here is a description of what the values mean under each of the columns in the "Workflows" page:

* Name
  
  - Dynamics 365 to Campaign (a.k.a. "Ingress")
  - Campaign to Dynamics 365 (a.k.a. "Egress")
  - Opt In/Out

* Backlog

  This integration application first reads in data and then writes data to the destination.  The "Backlog" value indicates the number of records that have been queued and are waiting to be written.   This value is expected to grow when you run have a large amount of data to process (e.g., you are running the integration for the first time, you are replaying the data, etc.).   If you feel that your Dynamics 365 and/or ACS records are not updating, then this is the first place you should check to see if there is a large number of records waiting to be written to the destination.    

* Status

  This is an indicator letting you know the state of the background processes associated with the workflow.  Here are the possible values for the status:
  - <u>RUNNING</u>:
    The process is currently running and your data should be synchronized.
    
  - <u>STOPPED</u>:
    The process is not currently running, so you should not expect your data should be synchronized.
     
  - <u>STARTING</u>:
    You have requested that the workflow processes to start.    The application has not yet started to synchronize the data associated with this workflow, but you can expect it will after a few minutes (when it will then show the status of "RUNNING") 
  
  - <u>FAILED</u>:
    The workflow processes were running but they encountered error(s) and they could not recover from these. 

* Actions
  
  Actions refer to actions that you can take on the workflow (seee the following): 
  
  - ![](assets/d365-to-acs-icon-edit.png) Edit  
  
    Clicking the pencil icon will send you to another page that will allow you to make updates to the workflow.   Keep in mind that any changes you make will NOT take effect until you stop the workflow and then restart it.
  
  - ![](assets/d365-to-acs-icon-start.png) Start 
    
    A Start button requests that a stopped workflow be started.   This button will only appear when the processes associated with the workflow are currently stopped.   The processes will first change to "STARTING" and then to "RUNNING".   The data associated with the workflow will not start synching until the workflow is in a "RUNNING" state.  
    
    The start button is a toggle.   If the workflow processes have been started already,  the button will change to a "Stop" button.  See the next bullet (directly below) for more information about Stop.
    
    >[!CAUTION]
    >                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       
    > It is strongly recommended that you stop the Ingress workflow before publishing changes to either Adobe Campaign Standard or Microsoft Dynamics 365.   These changes include updates to resources/entities (and their associated fields), links, identifier columns, etc… that are currently in use by the integration.   Failure to do so could lead to data loss and/or the workflow stopping unexpectedly.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     
    
  - ![](assets/d365-to-acs-icon-stop.png) Stop
  
    A Stop button requests that a running workflow be stopped.   This button will only appear when the processes associated with the workflow are currently running.
    
    The Stop button is a toggle.   If the workflow processes have been stopped already, then the button will change to a "Start" button.  See the previous bullet (directly above) for more information about Start.
    
    It's important to understand that when you edit a workflow, your updates are NOT immediately incorporated into the running processes' rules.   It's not until you stop the workflow (by clicking the stop button) and then click the Start button that your updates are incorporated into the running processes (once the process returns to a "RUNNING" state).  A warning indication is added to the Stop button to let you know when you've (a) made updates to workflow, but (b) have not done a Stop/Start of this workflow.   When changes have occurred to the workflow that require it be stop/started, it will look like the following:          
    ![](assets/d365-to-acs-icon-stop-with-changes.png)
