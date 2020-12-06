# Workflows

The Workflows page in the integration app lists the three workflows available, gives you the ability to edit them, as  well as the ability to start and stop the process.   This documentation will explain how this page works, however, it  assumes that you understand the basics of these workflows.   If you don't fully understand these, then it would be a  good idea to visit the [Data Flows](d365-acs-using-the-integration#data-flows)  section in the "Use the Microsoft Dynamics 365 integration documentation page.

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

  This integration app first reads in the data before it is then "written" to the destination.  The "Backlog" value  indicates the number of records that have been queued and are waiting to get written.   This value is expected to grow  when you run the integration for the first time or when you "replay" the data.   If you feel that your updates (from  the data source) are not visible in the destination, then this is the first place you should look to see if there are  a large number of records waiting to get written to the destination.   

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
  
  Actions refer to actions that you can take on the workflow.    You have the option to 
  
  - ![](assets/d365-to-acs-icon-edit.png) Edit  
  
    Clicking the pencil icon will send you to another page that will allow you to make updates to the workflow.   Keep in mind that any changes you make will NOT take effect until you stop the worflow and then restart it.
  
  - ![](assets/d365-to-acs-icon-start.png) Start 
    
    A Start button requests that a stopped workflow be started.   This button will only appear when the processes associated with the workflow are currently stopped.   The processes do not start immediately, so expect that state will first change to "STARTING" and then after a short time it will show "RUNNING".   The data associated with the workflow will not start syncing until the workflow is in a RUNNNING state. 
    
    The start button is a toggle.   If the workflow processes have been started already, then the button will change to a "Stop" button.  See the next bullet (directly below) for more information about stop.
    
  - ![](assets/d365-to-acs-icon-stop.png) Stop
  
    A Stop button requests that a running workflow be stopped.   This button will only appear when the processes associated with the workflow are currently running.
    
    The Stop button is a toggle.   If the workflow processes have been stopped already, then the button will change to a "Start" button.  See the previous bullet (directly below) for more information about stop.
    
    It's important to understand that when you edit a workflow that your updates are NOT immediately incorporated into the running processes' rules.   It's not until you stop the workflow (by clicking the stop button) and then click the Start button that your updates will be incorporated into the running processes (once the process returns to a "RUNNING" state).  A warning indication is added to the Stop button to let you know when you've (a) made updates to workflow, but (b) have not done a Stop/Start of this workflow.   When changes have occurred to the workflow that require it be stop/started then it will look like the following:          
    ![](assets/d365-to-acs-icon-stop-with-changes.png)
