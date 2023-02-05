# Exercise 2.2 - Configure and deploy the equipment and training approval integration flow
In this exercise, you will configure and deploy the beforehand copied integration flow.

Let us begin with understanding the integration flow copied. This integration flow has three steps:
1. Content Modifier where user can **Define Email ID** - The message received from AEM is in JSON format via AMQP sender adapter. The security credentials of AEM is already stored in the Security Material of the Cloud Integration capability.
<br>This step is used to input the newly hired employee and manager's Email ID.
<br>![Script collection](/exercises/ex2/images/02-0010-step1.png)

2. Message mapping step where the newly hired event data which is in JSON format is transformed to the othet JSON format expected to trigger the SAP Build Process Automation workflow.
<br>![Script collection](/exercises/ex2/images/02-0010-step2.png) 
<br>![Script collection](/exercises/ex2/images/02-0010-step3.png)

3. Trigger Call to *external system* that is the SAP Build Process Automation workflow through a Request Reply Step. This will trigger the workflow on the given manager's email id using the Cloud Integration HTTPS receiver adapter. The security credentials of the SAP Build Process Automation is already stored in the Security Material of the Cloud Integration capability.
<br>![Script collection](/exercises/ex2/images/02-0010-step4.png)

## Exercise steps

Run through the following steps.
1. After having copied the equipment and training approval integration flow template. From the *Actions* menu of your integration flow, select the menu entry *Configure*
<br>![Script collection](/exercises/ex2/images/02-0005.png)

2. In the upcoming dialog, maintain the Queue name **HO010_XX_Workflow**, replacing **XX** with the participant number assigned to you.
<br>![Script collection](/exercises/ex2/images/02-0006.png)
    
3. Switch to the <b>More</b> Tab in the same dialog and replace **Manager_EmailID** to **userXX@techedusers.com** , replacing **XX** with the participant number assigned to you and **NewHire_EmailID** with your email address where you can login and check the emails. This has been done to overwrite the email id of the newly hired candidate so that you can get the approval status email from the manager to your own email id.
<br>Then select *Save*, in case of any warning just ignore it. Once saved, select *Deploy*
<br><img src="/exercises/ex2/images/02-0007.png" width=80%>
    
4. Close the next dialog if the warning message is shown. Then click on **Yes** to deploy and close the confirmation dialog.
<br>![Script collection](/exercises/ex2/images/02-0008-warning.png)
<br>![Script collection](/exercises/ex2/images/01-0008_0.png)
<br>![Script collection](/exercises/ex2/images/02-0008.png)



## Summary

At the end of this exercise, you should have configured and deployed the integration flow responsible for triggering the equipment and training approval workflow.

Next, we will check the deployment status. 
<br>Continue to - [Exercise 2.3 - Check the deployment status of equipment and training integration flow](/exercises/ex2/ex23)
