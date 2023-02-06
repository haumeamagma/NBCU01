# SAP Integration Suite, Advanced Event Mesh configuration (for your information only)

## Service Description

Take advantage of a complete event streaming, event management, and monitoring platform that incorporates best practices, expertise, and technology for event-driven architecture (EDA) on a single platform. The following features are available for advanced event mesh:

- **Event Streaming:** Deploy event broker services, create event meshes, and optimize and monitor your event-driven system.
- **Event Management:** Design, discover, visualize, share, and manage various aspects of your event-driven architecture (EDA). You can also model your EDA to visualize component relationships.
- **Event Monitoring and Insights:** Use monitoring dashboards and configurable notifications to detect potential issues before they negatively impact your brokers and event broker services.

Find out more about **SAP Integration Suite, Advanced Event Mesh(AEM)** in the [SAP Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/advanced-event-mesh).

## Configuration Overview

To enable the event-driven architecture in this integration scenario, the following configuration steps has already been done for you. This section is for your information only, no SAP Integration Suite, Advanced Event Mesh access has been provided for this hands-on session.

Run through the following steps in the given order:

1. <b>REST endpoint:</b> This is the endpoint used by SAP SuccessFactors to send events to AEM. The shown endpoint is providing the hostname. The actual topic the event is sent to, will be part of the URL configuration in SFSF. You can get more information about the SFSF configurations [here](../intro2). 
<br><img src="/intro/intro3/images/AEM_01.jpg" width=90% height=90%> 	

2. <b>AMQP endpoint:</b> This is the endpoint used by the Integration Flows in Cloud Intgeration capability of SAP Integration Suite to connect to AEM. 
<br><img src="/intro/intro3/images/AEM_02.jpg" width=90% height=90%> 	

3. <b>Queues:</b> For each participant there are 2 queues are preconfigured. **HO010_XX_Email** and **HO010_XX_Workflow** with **XX** the participant number assigned to you. You will deploy 2 Integration Flows, each subscribing to one of the queues.
<br><img src="/intro/intro3/images/AEM_03.jpg" width=90% height=90%> 	

4. <b>Topic Subscription:</b> Each of the queues is subscribed to the topic exposed by SAP SuccessFactors i.e. `SuccessFactors/NewHire`. For each New Hire in SFSF an event is raised once and send to AEM topic. Each subscriber (=queue) gets its own copy of the event and can process it indepedently. 
<br><img src="/intro/intro3/images/AEM_04.jpg" width=90% height=90%> 	

## Summary

If you want some more information on the general concepts around **Event-Driven Architectures**, you can check [here](https://solace.com/what-is-event-driven-architecture/) for a brief introduction.

Now that you have gone through all the introduction chapters, you should have a clear picture of the overall integration scenario and could start with the actual exercises.

Navigate to - [Exercise overview page](/README.md#exercises)
