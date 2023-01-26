# Exercise 1.3 - Configure and deploy your welcome email integration flow

In this exercise, you will configure and deploy the beforehand copied integration flow.

Integration flow design,

Let us begin with understanding the integration flow copied. This integration flow has three steps:
1. JSON to XML Converter - The message received from AEM is in JSON format. Working with XML message formats opens up many possibilities with Integration Suite, hence we transform the message from JSON to XML. Learn more about [JSON to XML Converter](https://help.sap.com/docs/CLOUD_INTEGRATION/368c481cd6954bdfa5d0435479fd4eaf/5a7c0cd2a3e8497c89ffcda41787477f.html?q=JSON to XML&locale=en-US). 

<br>![Script collection](/exercises/ex1/images/01-0018-step1.png)

2. Content Modifier to **Extract New Hire Attributess** and
In this step the following values needed for further processing are extracted from the input payload : employeeId,employeeName,hireDate,gender,dateOfBirth,email,cellPhone,managerId,managerName,managerHR,company,jobTitle,departmentCode,departmentText,businessunitCode, businessunitText,divisionCode,divisionText,location and country.

<br>![Script collection](/exercises/ex1/images/01-0018-step2.png)

3. Content Modifier to **Set Email Body**
Here theNew Hire Welcome Email is composed based on values extracted in the previous step. The New Hire Email is inputed from the user through configuration.
Learn more about content modifier basics here- https://help.sap.com/docs/CLOUD_INTEGRATION/368c481cd6954bdfa5d0435479fd4eaf/b0576a824cdf46868fcc70fd9e697f16.html?q=content modifier&locale=en-US

<br>![Script collection](/exercises/ex1/images/01-0018-step3.png)

## Exercise steps

Run through the following steps.
1. After having copied the integration flow template, you should see one integration flow in your package. From the *Actions* menu of your integration flow, select the menu entry *Configure*

    <br>![Script collection](/exercises/ex1/images/01-0010.png)

2. In the upcoming dialog, maintain the Queue name **HO010_XX_Email** whereas replacing **XX** with the participant number assigned to you.
    <br>![Script collection](/exercises/ex1/images/01-0011.png)
    
4. Switch to the Receiver Tab in the same dialog and replace **New Hire EMail ID** to your own Email ID where you can login and check the emails.
   Then select *Save*. Once saved, select *Deploy*

    <br><img src="/exercises/ex1/images/01-0012.png" width=80%>
    
6. Confirm the next dialog and click on Ok.

    <br>![Script collection](/exercises/ex1/images/01-0013.png)
    <br>![Script collection](/exercises/ex1/images/01-0014.png)

## Summary

At the end of this exercise, you should have triggered the deployment of the integration flow.

Next, we will check the deployment status. Continue to - [Exercise 1.4](/exercises/ex1/ex14)

