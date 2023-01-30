# Scenario Introduction

This session scenario helps you to learn more about <b>Hyperautomation</b> by implementing an event-driven scenario where you react and respond to a new hire business event from <b>SAP SuccessFactors</b> using <b>SAP Integration Suite</b> and <b>SAP Build Process Automation</b>.

In this, we implement an end-to-end <b>Recruit-to-Retire (R2R)</b> business process across a heterogeneous landscape. From <b>SAP Integration Suite</b> we would leverage <b>Advanced Event Mesh</b> and <b>Cloud Integration</b> capabilities. This also includes human interactions to achieve an end-to-end employee onboarding business process using <b>SAP Build Process Automation</b>.

## Business Scenario
Presume in your organization, you are using <b>SAP SuccessFactors</b> as a central Human Capital Management (HCM) application and you like to automate a few aspects of a newly hired employee in real-time like:

1. You like to send a welcome email to the newly hired candidate along with the <b>Qualtrics</b> survey link to understand the candidate's onboarding experience.

2. You also like to initiate the newly hired candidate's equipment and training approval workflow to the manager using the SAP Build Process Automation.

Instead of developing point-to-point integration for the above two use cases, you will learn and understand how we can achieve the same via an event-driven integration pattern.

## Scenario Architecture

<img src="/intro/intro1/images/scenario_architecture.png" width=100% height=100%>

1. As and when you add(hire) a new employee in SAP SuccessFactors, with the proper [configurations](/intro/intro2), it publishes a new employee data event with the required payload.
<br><br>
2. The new employee data event gets published directly to <b>SAP Integration Suite, Advanced Event Mesh</b> topic using the <b>REST</b> interface.
3. First Subscriber handles the task of automatically informing the new Employee of the process and next steps.
2a. It then sends a welcome email to the newly hired candidate's email id along with the qualtrics survey link using the Cloud Integration Mail receiver adapter.
2b. By clicking the qualtrics survey link, candidate provides the onboarding experience feedback.

Second Subscriber handles the task of automatically informing the manager of the new employee addition and setting up the workflow to onboard the employees necessary equipment.
3a. It will trigger the equipment and training approval workflow in SAP Build Process Automation and assign the task to the manager on the given manager's email id using the Cloud Integration HTTPS receiver adapter. This will be visible in the Task Center(one inbox).
3b. On approval or rejection, workflow notify the newly hired candidate on the given candidate's email id.

Summary
You should now be familiar with the scenario.

Now, we show what all configurations has been done in SAP SuccessFactors to enable new hire events publication to Cloud Integration. Continue to - [SAP SuccessFactors Configuration](/intro/intro2)
