# Exercise 1: Explore best practices processes of SAP S/4HANA Cloud

In this exercise you’ll use SAP Signavio Process Explorer to examine standard processes of an SAP S/4HANA Cloud system. You’ll learn how to find latest product innovations related to the process and learn about typical related KPI metrics. 


## Exercise 1.1 Logon

Open the SAP Signavio Process Explorer [(https://editor.signavio.com/p/hub)](https://editor.signavio.com/p/hub)
Logon with your username/password as provided by the trainings 

_**⚠️ Attention: throughout the exercise replace `XXX` with your personal participant number!**_

<br>![](images/0_001.png)




## Exercise 1.2 Navigate SAP Signavio Process Explorer

1. Click on the ➕ icon below `Processes` to navigate to the End-to-End Process House: 
<br>![](images/0_002.png)

2. An overview of all End-to-End processes for a cross industry appears. As we are interested in the Consumer Product Industry, we click on `Consumer Industries` 
<br>![](images/0_003.png)

3. In the sidebar (Attribute field), click on `E2E Processes for Consumer Products`
<br>![](images/0_004.png)

4. E2E Process House for Consumer Products is open, and you can explore the content per each end-to-end process. We would like to drill down further into the Lead-to-Cash process. Therefore, we are clicking on the `Lead-to-Cash` button
<br>![](images/0_011.png)

5. And follow the navigation by clicking `Lead to Cash (Consumer Products - Cloud)` within the sidebar
<br>![](images/0_012.png)

6. With another click on the Lead-to-Cash diagram we will land on the overview page of the process: 
<br>![](images/0_013.png)

7. To navigate to the Sell from Stock process, we drill down deeper on the `Order to Fulfill (Standard B2B)` process by clicking on the ➕ sign
<br>![](images/0_006.png)

8. To see now the BPMN (Business Process Modelling Notation) best practice process for Sell from Stock in SAP S/4HANA Cloud, click on the ➕ sign of `Manage Customer Orders`
<br>![](images/0_007.png)

9. You'll find an overview of the best practice process `5HL - Sell from Stock - Consumer Products` in BPMN diagram, all involved business roles and tasks to fulfill this activity, and links to subsequent processes (e.g. J59 Account Receivable)
<br>![](images/0_008.png)

10. To evaluate the metrics for Sell from Stock, activate the `Overlay` functionality and chose `Metrics`.
<br>![](images/0_009.png)

11. Click one of the orange elements to peek into relevant metrics. 
<br>![](images/0_010.png)

12. Click one of the listed metrics in the sidebar 
<br>![](images/0_018.png)

13. And open the `Metric Documentation` 
<br>![](images/0_019.png)

14. The documentation lists all relevant metrics for Order-to-Cash, e.g. you can also find the `Lead time: Sales document item creation to delivery creation`
<br>![](images/0_020.png)

15. Close the browser tab to navigate back to the diagram.

16. Can you find the Fiori App related to the `Create Sales Order` activity? 
<br>![](images/0_014.png)

17. Click the blue marker to open the sidebar. Follow the link to the Fiori Apps Library
<br>![](images/0_015.png)

18. The SAP Fiori Apps Reference Library lets you explore, plan and implement SAP Fiori, the latest user experience from SAP including all relevant content!
<br>![](images/0_016.png)
💡 You can also search for known transaction codes (e.g. try `VA02`) to find related Fiori apps. Get [recommendations](https://help.sap.com/docs/SAP%20Fiori%20Apps%20Reference%20Library/187a50cf8191418ab7b52505fcef1789/0f2b580b2e454a5a91b79119350ff4e7.html) that are relevant for you based on the business processes you use, and readiness describes how ready your system is to use SAP Fiori apps. Or check out the new [SAP Fiori Upgrade Impact Analysis](https://help.sap.com/docs/SAP%20Fiori%20Apps%20Reference%20Library/187a50cf8191418ab7b52505fcef1789/5d5ede164e4a4e95b32431c02c58dfac.html)


## Summary

You now learned how to find solution best practices processes of SAP S/4HANA Cloud, get an overview of innovations and new Fiori apps. In the next exercise you'll analyze how the process **actually** runs in your SAP S/4HANA Cloud system.

*Note: The content in this Teched exercise tenants was reduced to a subset and  shows a preview version only. Today you can already find recommendations in our [SAP Best Practices Explorer](https://rapid.sap.com)*. In additon an early beta program of the SAP Signavio Process Explorer can be accessed [here](https://www.signavio.com/one-process-acceleration-layer/). Product launch is planned mid January 2023.

Continue to - **[Exercise 2 - Analyze and investigate process mining results](../ex2/README.md)**

Back to the [Overview](../../README.md)
