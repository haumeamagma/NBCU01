# Exercise 2.2 - Configure and deploy the build process automation integration flow

Let us begin with understanding the integration flow copied. This integration flow has three steps:
1. Content Modifier where user can **Define Email ID** - This step is used to input the user and manager Email ID.
<br>![Script collection](/exercises/ex2/images/02-0010-step1.png)

2. Message mapping step where the JSON format received from the SuccessFactors sender system is transformed to the structure expected by the receiver system- SAP Build Process Automation.

<br>![Script collection](/exercises/ex2/images/02-0010-step2.png) 
<br>![Script collection](/exercises/ex2/images/02-0010-step3.png)

3. Trigger Call to *external system* which is the SAP Build Process Automation through a Request Reply Step.
<br>![Script collection](/exercises/ex2/images/02-0010-step4.png)

In this exercise, you will configure and deploy the beforehand copied integration flow.

## Exercise steps

Run through the following steps.
1. After having copied the integration flow template, you should see one integration flow in your package. From the *Actions* menu of your integration flow, select the menu entry *Configure*

    <br>![Script collection](/exercises/ex2/images/02-0005.png)

2. In the upcoming dialog, maintain the Queue name **HO010_XX_Workflow** whereas replacing **XX** with the participant number assigned to you.
    <br>![Script collection](/exercises/ex2/images/02-0006.png)
    
4. Switch to the *More* Tab in the same dialog and replace **Manager_EmailID** to **userXX@techedusers.com** , replacing **XX** with the participant number assigned to you and **NewHire_EmailID** with your email address where you can login and check the emails.
   Then select *Save*. Once saved, select *Deploy*

    <br><img src="/exercises/ex2/images/02-0007.png" width=80%>
    
6. Confirm the next dialog and click on Ok.

    <br>![Script collection](/exercises/ex2/images/02-0008.png)

## Summary

At the end of this exercise, you should have triggered the deployment of the integration flow.

Next, we will check the deployment status. Continue to - [Exercise 2.3](/exercises/ex2/ex23)


