# Exercise 1.3 - Configure and deploy the welcome email integration flow

In this exercise, you will configure and deploy the beforehand copied integration flow.

Let us begin with understanding the copied integration flow. This integration flow has three steps:
1. JSON to XML Converter - The message received from AEM is in JSON format via AMQP sender adapter. The security credentials of AEM is already stored in the Security Material of the Cloud Integration capability. Working with XML message formats opens up many possibilities with Integration Suite, hence we transform the message from JSON to XML.
<br>![Script collection](/exercises/ex1/images/01-0018-step1.png)
<br>![Script collection](/exercises/ex1/images/01-0018-payload2.png) 

2. Content Modifier to **Extract New Hire Attributes** - In this step the following values needed for further processing are extracted from the XML payload using the XPath: 
<br><br>employeeId,employeeName,hireDate,gender,dateOfBirth,email,cellPhone,managerId,managerName,managerHR,company,jobTitle,departmentCode,departmentText,businessunitCode, businessunitText,divisionCode,divisionText,location and country.
<br>![Script collection](/exercises/ex1/images/01-0018-step2.png)

3. Content Modifier to **Set Email Body** - Here the New Hire Welcome Email is composed based on the dynamic values extracted in the previous step. The email is then send to the configured newly hired Email Id using the Mail receiver adapter. The security credentials of the SMTP server is also stored in the Security Material of the Cloud Integration capability.
<br>![Script collection](/exercises/ex1/images/01-0018-step3.png)

## Exercise steps

Run through the following steps
1. After having copied the integration flow template, you should see one integration flow in your package. From the *Actions* menu of your integration flow, select the menu entry <b>Configure</b>
<br>![Script collection](/exercises/ex1/images/01-0010.png)

2. In the upcoming dialog, maintain the Queue name **HO010_XX_Email**, replacing **XX** with the participant number assigned to you.
<br>![Script collection](/exercises/ex1/images/01-0011.png)
    
3. Switch to the <b>Receiver</b> Tab in the same dialog and replace **New Hire EMail ID** with your own Email ID where you can login and check the emails. This has been done to overwrite the email id of the newly hired candidate so that each one of you can get the welcome email on your own configured email id. 
<br>Then select *Save*, in case of any warning just ignore it. Once saved, select *Deploy*
<br><img src="/exercises/ex1/images/01-0012.png" width=80%>
    
4. Close the next dialog if the warning message is shown. Then click on **Yes** to deploy and close the confirmation dialog.
<br>![Script collection](/exercises/ex1/images/01-0013-warning.png)
<br>![Script collection](/exercises/ex1/images/01-0014_2.png)
<br>![Script collection](/exercises/ex1/images/01-0014.png)

## Summary

At the end of this exercise, you should have configured and deployed the integration flow responsible for sending the welcome email along with Qualtrics survey link. 

Next, we will check the deployment status. 
<br>Continue to - [Exercise 1.4 - Check the deployment status of welcome email integration flow](/exercises/ex1/ex14)
