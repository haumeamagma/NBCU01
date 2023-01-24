# SAP SuccessFactors Configuration

These are the SAP SuccessFactors configuration steps which are already completed. This section is for review only. 
In this section, you get a view of the pre-configurations done so that an integration designed and deployed in SAP Integration Suite is triggered when there is a change in event(New Hire) in Employee Central. 

Run through the following steps:

1. Logon to the SAP SuccessFactors with the SFSF Admin User ID
    <br><img src="/intro/intro2/images/1. SFSF_Logon.PNG" width=70% height=70%>

2. Enter "Integration Center" in the search field. This would bring us to IC.
    <br><img src="/intro/intro2/images/2. SFSF_Admin.PNG" width=70% height=70%>

3. Select “My Integrations” from the Landing Page
    <br><img src="/intro/intro2/images/3. SFSF_Search_IC_Result.PNG" width=70% height=70%>

4. Open “IN260 Confluent Kafka” from the landing page
    <br><img src="/intro/intro2/images/4. IC_Landing_Page.PNG" width=70% height=70%>

5. In the Options Tab, we provide Integration Name and Description for the same 
    <br><img src="/intro/intro2/images/5. My_IC_Options.PNG" width=70% height=70%>

6. In the Configure Fields, we provide the file input fields. These would be the fields being sent to the iFlow on the event which is Employee Creating/Change. 
On right side is the Metadata of the output
    <br><img src="/intro/intro2/images/6. IC_Configure_Fields_1.PNG" width=70% height=70%>

7. Filter tab is in case there are filters to be stup. We do not have any filters so we go to the next step
    <br><img src="/intro/intro2/images/7. IC_Filter.PNG" width=70% height=70%>

8. In the destination section we provide the REST based URL for the end point where the iFlow is and the Authentication Type which is our case is OAuth
    <br><img src="/intro/intro2/images/8. IC_Destination_Settings.PNG" width=70% height=70%>

9. In this section we do Review and Run
    <br><img src="/intro/intro2/images/9. IC_Review_Run.PNG" width=70% height=70%>

10. After Run, you select Intelligent Service Center(ISC)
    <br><img src="/intro/intro2/images/10. IC_Review_Run_Go_To_ISC.PNG" width=70% height=70%>
    
11. ISC showing the published event 
    <br><img src="/intro/intro2/images/11. ISC.PNG" width=70% height=70%>    
    
## Summary

You should now be familiar with all the configurations that has been done in SAP SuccessFactors to enable new hire events publication to Cloud Integration.

Now, we show pre-deployed integration flow to publish events to Confluent Kafka. Continue to - [Publish to Confluent Kafka](/intro/intro3)

