# New Hire event configuration in SAP SuccessFactors (for your information only)

To enable the <b>New Hire</b> event in SAP SuccessFactors(SFSF) Employee Central, the following configuration steps has already been done by the session owner for you. This section is for your understanding only. 

Run through the following steps in the given order:

1. Logon to the <b>SAP SuccessFactors</b> with the SFSF Admin User ID
    <br><img src="/intro/intro2/images/1. SFSF_Logon.PNG" width=60% height=60%>

2. Go to <b>Integration Center</b> by searching it in the search field
    <br><img src="/intro/intro2/images/2. SFSF_Admin.PNG" width=90% height=90%>

3. Select <b>My Integrations</b> from the Integration Center landing page
    <br><img src="/intro/intro2/images/3. SFSF_Search_IC_Result.PNG" width=90% height=90%>

4. We have aready created an integration with the name <b>D-Com 2023 HO010 - Hyperautomation</b>. <br/>
In this we have defined the <b>New Hire</b> attributes and <b>REST Destination</b> to publish the new hire event data to <b>SAP Integration Suite, Advanced Event Mesh</b> where all the subscribers can subscribe to the new hire event.</br>
Click on the <b>Edit Integration</b> button to see the integration details
    <br><img src="/intro/intro2/images/Open_DCom_2023 HO010_Hyperautomation.PNG" width=90% height=90%>

5. In the <b>Options</b> tab, we provide the <b>Integration Name</b> and <b>Description</b>. Click <b>Next</b> to see the configured fields
    <br><img src="/intro/intro2/images/Tab1_Options.PNG" width=90% height=90%>

6. In the <b>Configure Fields</b> tab, we have defined the <b>New Hire</b> attributes like employee name, position, manager name, etc. that is required for this scenario. As this event contains all the fields necessary for the scenario, we do not need to do a callback to get the employee details.<br/>
On right side you can also see the data preview. Click <b>Next</b> to see the response fields
    <br><img src="/intro/intro2/images/Tab2_Configure_Fields.PNG" width=90% height=90%>

7. In the <b>Response Fields</b> tab, we can configure fields for processing the REST response.<br/>
We have not defined any fields here as this is not required for this event-driven integration scenario. Click <b>Next</b> to see the filters
    <br><img src="/intro/intro2/images/Tab3_Response_Fields.PNG" width=90% height=90%>

8. In the <b>Filter</b> tab, we can configure the advanced filter and sort options.<br/>
We have not defined any filters, click <b>Next</b> to see the destination settings
    <br><img src="/intro/intro2/images/Tab4_Filter.PNG" width=90% height=90%>

9. In the <b>Destination Settings</b> tab, we have defined the REST endpoint of <b>SAP Integration Suite, Advanced Event Mesh</b> and the Authentication Type as <b>Basic Authentication</b> with User Name and Password. Click <b>Next</b> to review and run the integration
    <br><img src="/intro/intro2/images/Tab5_Destination_Settings.PNG" width=90% height=90%>

10. In the <b>Review and Run</b> tab, we can review the settings of the integration before committing it and run as well.
    <br><img src="/intro/intro2/images/Tab6_Review_and_Run.PNG" width=90% height=90%>

11. After the review and run, save it and go to <b>Intelligent Service Center(ISC)</b>
    <br><img src="/intro/intro2/images/10. IC_Review_Run_Go_To_ISC.PNG" width=90% height=90%>
    
12. ISC showing the published event 
    <br><img src="/intro/intro2/images/11. ISC.PNG" width=90% height=90%>    
    
## Summary

You should now be familiar with all the configurations that has been done in SAP SuccessFactors to enable new hire events publication to Cloud Integration.


