## Test additional data (targetdata) using traps {#test-additional-data-using-traps}

This section describes how to use a trap test profile to test a delivery using  additional data (also called targetdata) available in a workflow. Additional data will come from real profile as opposed to using fake test profile data. This allows you to check that the variables used in a complex workflow are accurate and to get a view of the message that your recipients will receive.

>[!CAUTION]
   >
   >Following this process implies to run the workflow and confirm sending. The email is sent for real to the targeted audience including the trap test profile.
   >Adobe recommends creating a first test workflow that will be sent to a selected target including the trap test profile, then creating a real workflow targeting the desired audience.

For example, you want to check that additional data retrieved from a Load file activity are correctly used in the email you intend to send.

First, you need to define a test profile will be part of the targeted audience.

1. Create a test profile. For more on this, see [Managing test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md#managing-test-profiles).

1. Enable **[!UICONTROL Proof]** and **[!UICONTROL Trap]** as the intended usage.

   ![](assets/trap_test_profile.png)

   >[!NOTE]
   >
   >When using a test profile as a trap, for any enriched fields in a message, the corresponding additional data is randomly picked from a real targeted profile and assigned to the trap test profile.

Then, you need to create a workflow using additional data.

1. Access the marketing activity list and create a test workflow.

   See [Creating a workflow](../../automating/using/building-a-workflow.md#creating-a-workflow).

1. Drag and drop a **[!UICONTROL Query]** activity into your workflow and open it to define the main target.

   The Query activity is presented in the [Query](../../automating/using/query.md) section.

1. Drag and drop a Load file activity to assign some data to a profile. In this example, load a file containing account numbers corresponding to some profiles of the database.

   ![](assets/trap_load_file.png)

   The Load file activity is presented in the [Load file](../../automating/using/load-file.md) section.

1. Drag and drop an **[!UICONTROL Enrichment]** activity into your workflow and link the Load file and Query activities to it.

   ![](assets/trap_test_enrichment.png)

1. Open the Enrichment activity and make sure **[!UICONTROL Query]** is selected as the **[!UICONTROL Primary set]**.

   ![](assets/trap_test_enrichment_primary_set.png)

1. In the **[!UICONTROL Advanced relations]** tab of the Enrichment activity, select the **[!UICONTROL 0 or 1 cardinality simple link]** and define the fields to be used for reconciliation.

   ![](assets/trap_test_enrichment_relation.png)

1. In the **[!UICONTROL Additional data]** tab, select the elements that you want to use in your email. Here select Account number (column from the file that you retrieved through the Load file activity).

   ![](assets/trap_test_enrichment_select_element.png)

   ![](assets/trap_test_enrichment_additional_data.png)

   The Enrichment activity is presented in the [Enrichment](../../automating/using/enrichment.md) section.

1. Drag and drop a **[!UICONTROL Segmentation]** activity into your workflow and open it to refine the main target if needed.

   ![](assets/trap_test_segmentation.png)

   The Segmentation activity is presented in the [Segmentation](../../automating/using/segmentation.md) section.

Now you need to create an email targeting the trap test profile that you want to test additional data with.

1. Drag and drop an **Email delivery** activity into your workflow and open it.

   The Email delivery activity is presented in the [Email delivery](../../automating/using/email-delivery.md) section.

1. From the email message dashboard, select the test profile with trap usage that you created.

   ![](assets/trap_test_profile_select.png)

1. Add to your email content personalization fields using the additional data that you defined in the Query activity.

   ![](assets/trap_test_perso_field.png)

1. Save the email and start the workflow.

   During message preparation, the target count includes the test profile that you selected.

   ![](assets/trap_test_workflow.png)

1. In the Sending logs of the Email delivery activity, you can see the test profile.

   ![](assets/trap_test_sending_logs.png)

   Click the test profile row. You can see on the mirror page that an account number is displayed.

   ![](assets/trap_test_mirror_page.png)

1. Click the **[!UICONTROL Confirm]** button.

   In the message sent to the trap test profile, you can also check that additional data is replaced by data from a 'real' profile.

>[!NOTE]
   >
   >Only additional data are replaced. No real profile data such as first name or last name will be used for the test profile.

Now you can duplicate the test workflow, define your real audience and run the new workflow to send an email to your 'real' intended target.