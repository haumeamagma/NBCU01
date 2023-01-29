# New Hire event configuration in SAP SuccessFactors (for your information only)

To enable the <b>New Hire</b> event in <b>SAP SuccessFactors(SFSF) Employee Central</b>, the following configuration steps has already been done for you. This section is for your information only, no SFSF system access has been provided for this hands-on session. 

Run through the following steps in the given order:

1. Logon to the <b>SAP SuccessFactors</b> with the SFSF Admin User ID.
    <br><img src="/intro/intro2/images/SFSF_Logon.png" width=60% height=60%>

2. Go to <b>Integration Center</b> by searching it in the search field.
    <br><img src="/intro/intro2/images/Search_Integration_Center.png" width=90% height=90%>

3. Select <b>My Integrations</b> from the Integration Center landing page.
    <br><img src="/intro/intro2/images/Integration_Center.png" width=90% height=90%>

4. We have aready created an integration with the name <b>D-Com 2023 HO010 - Hyperautomation</b>.<br/>
In this we have defined the <b>New Hire</b> attributes and <b>REST Destination</b> to publish the new hire event data to <b>SAP Integration Suite, Advanced Event Mesh</b> where all the subscribers can subscribe to the new hire event.</br></br>
Click on the <b>Edit Integration</b> button to see the integration details.
    <br><img src="/intro/intro2/images/Integration_Center_List.png" width=90% height=90%>

5. In the <b>Options</b> tab, we have provided the <b>Integration Name</b> and <b>Description</b>. Click <b>Next</b> to see the configured fields.
    <br><img src="/intro/intro2/images/IC_Options.png" width=90% height=90%>

6. In the <b>Configure Fields</b> tab, we have defined the <b>New Hire</b> attributes like employee name, position, manager name, etc. that is required for this scenario. As this event contains all the fields necessary for the scenario, we do not need to do a call back to get the newly hired details.<br/>
On the right side, you can also see the data preview. Click <b>Next</b> to see the response fields.
    <br><img src="/intro/intro2/images/IC_Configure_Fields.png" width=90% height=90%>

7. In the <b>Response Fields</b> tab, we can configure fields for processing the REST response.<br/>
We have not configured any fields here as this is not required for this scenario. Click <b>Next</b> to see the filters.
    <br><img src="/intro/intro2/images/IC_Response_Fields.png" width=90% height=90%>

8. In the <b>Filter</b> tab, we can configure the advanced filter and sort options.<br/>
We have not defined any filters for this scenario, click <b>Next</b> to see the destination settings.
    <br><img src="/intro/intro2/images/IC_Filter.png" width=90% height=90%>

9. In the <b>Destination Settings</b> tab, we have defined the REST endpoint and Authentication details of <b>SAP Integration Suite, Advanced Event Mesh</b> along with the topic name i.e. <b>SuccessFactors/NewHire</b>. The new hire events would get published to this topic only. <br/><br/>
Click <b>Next</b> to review and run the integration.
    <br><img src="/intro/intro2/images/IC_Destination_Settings.png" width=90% height=90%>

10. In the <b>Review and Run</b> tab, we can review the settings of the integration before committing it and run as well.</br>
After the review and run, save it to deploy it to the server
    <br><img src="/intro/intro2/images/IC_Review_and_Run.png" width=90% height=90%>
    <br><br><img src="/intro/intro2/images/IC_Save_Deploy.png" width=90% height=90%>

11. After the review and run, save it to deploy it to the server. Go to <b>Intelligent Service Center(ISC)</b>.
    <br><img src="/intro/intro2/images/IC_Goto_ISC.png" width=90% height=90%>
    
12. ISC showing the published event.
    <br><img src="/intro/intro2/images/11. ISC.PNG" width=90% height=90%>    
    
## Summary

You should now be familiar with all the configurations that has been done in SAP SuccessFactors to enable new hire events publication to Cloud Integration.


