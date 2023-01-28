# Scenario Introduction

This session scenario helps you to learn event-driven integration pattern using SAP Integration Suite Cloud Integration and Event Mesh.

In this, we implement an end-to-end Recruit-to-Retire (R2R) business process across a heterogeneous and hybrid landscape i.e. SAP SuccessFactors, Email and SAP Build Process Automation.

## Business Scenario
Presume in your organization, you are using SAP SuccessFactors as a central Human Capital Management (HCM) application and you like to automate few aspects of newly hired employee in real-time like:

You like to send a welcome email to the newly hired candidate along with the qualtrics survey link to understand the candidate's onboarding experience.

You would also like to initiate the newly hired candidate's equipment and training approval workflow to the manager using the SAP Build Process Automation.

Instead of developing point-to-point integration for the above two use cases, you will learn and understand how we can achieve the same via event-driven integration pattern along with the exactly-once quality of service.

## Scenario Architecture

<b> !! :boom: Insert Architecture Diagram here :boom: !!</b>

As and when you add a new employee in SAP SuccessFactors,
1a. It will publishes an event with the required payload to Cloud Integration REST interface.

First Subscriber handles the task of automatically informing the new Employee of the process and next steps.
2a. It then sends a welcome email to the newly hired candidate's email id along with the qualtrics survey link using the Cloud Integration Mail receiver adapter.
2b. By clicking the qualtrics survey link, candidate provides the onboarding experience feedback.

Second Subscriber handles the task of automatically informing the manager of the new employee addition and setting up the workflow to onboard the employees necessary equipment.
3a. It will trigger the equipment and training approval workflow in SAP Build Process Automation and assign the task to the manager on the given manager's email id using the Cloud Integration HTTPS receiver adapter. This will be visible in the Task Center(one inbox).
3b. On approval or rejection, workflow notify the newly hired candidate on the given candidate's email id.

Summary
You should now be familiar with the scenario.

Now, we show what all configurations has been done in SAP SuccessFactors to enable new hire events publication to Cloud Integration. Continue to - [SAP SuccessFactors Configuration](/intro/intro2)
