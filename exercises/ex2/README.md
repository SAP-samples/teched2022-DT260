# Exercise 2: Analyse and investigate process mining results

In the previous exercise we saw how the process `Sell from Stock - Consumer Products (5HL)` is designed in SAP S/4HANA. In this exercise you’ll jump into SAP Signavio Process Intelligence and to retrieve live insights our of how processes are **actually** executed in your SAP S/4HANA Cloud system. 


## Exercise 2.1 Jump to SAP Signavio Process Intelligence

SAP Signavio Process Intelligence is a collaborative process mining solution that helps you unleash the power in your process and experience data to transform your business.

1. Click the hyperlink as shown below, or click [here](https://editor.signavio.com/g/statics/pi/areas) to open Process Intelligence
<br>![](images/2_001.png)

2.	Open your process investigation (instead of `XXX` select your personal group number)
<br>![](images/2_002.png)

3. Open `Sell from Stock (5HL)` to start an investigation
<br>![](images/2_003.png)


## Exercise 2.2 Conformance
The first widget will give an overview about process conformance. 
The BPMN model of our best practices process (Sell from Stock - 5HL) was linked as a base process. The paths respectively hotspots are displayed as overlays (blue color). Explore some of the different process variants with the panel on the right.
<br>![](images/2_014.png)


## Exercise 2.3 Measure one of the pre-defined metrics

1. Scroll down to the end of the screen and click `Add Widget`
<br>![](images/2_004.png)

2. Select `Value`
<br>![](images/2_005.png)

3. Select type metric and select `Lead time: sales document item creation to delivery creation` (you might remember that metric from Exercise 1). Click `Save` to confirm.
<br>![](images/2_006.png)
<br>The new metric is added to the investigation.

4. Click the 3-dots to add a `Threshold`
<br>![](images/2_007.png)

5. Select `3 regions` and put thresholds like shown below
<br>![](images/2_008.png)

6. The thresholds are shown below the actual measurement
<br>![](images/2_009.png)

*Note: Further metrics of Lead-to-Cash can be found within the metric library. In the sidebar select `Metrics` and click `Add new metric` and select `From metric library`. Majority have not been configured due to the simplified data model of this exercise but will be applicable when you start with the full scale Order-to-Cash data model.*


## Exercise 2.4 Automated insights
The various Widgets available in Signavio Process Intelligence allow to flexibly drill down into data of the actual productive backend system. In this exercise we'll make use of the machine learning supported `Automated Insights` feature to __autonomously__ find correlations/anomalies.

1. Click the light bulb icon top right of the investigation screen.
<br>![](images/2_010.png)

2. Select `Automated` and select one of the suggested insights to click `Add to investigation`. In this Exercise choose `...BillToPartyCountry...` (*Press Ctrl+F to find on screen*) and confirm by clicking `Paste here`
<br>![](images/2_011.png)

3. The widget is added at the end of the investigation. Scroll down to click the 3-dots to `Edit` the widget.
<br>![](images/2_012.png)

4. You can find the SIGNAL query that was generated and change e.g. the chart type by selecting a pie chart.
<br>![](images/2_013.png)

*Note: This exercise uses a machine generated dataset so Automated Insights will only be able to return artificial results.*


## Summary

Yay! 🥳 You've now started your first basic investigation based on a simplified data model for this exercise. Typically you'd start with one of [SAP Signavio Process Intelligence Accelerators](https://documentation.signavio.com/suite/en-us/Content/process-intelligence/accelerators-intro.htm) which are sets of different contents, like transformation templates and metrics. They are designed to help you speed up your business process transformation. For example, they simplify event log creation and reduce the time to insight.

Continue to - **[Exercise 3: Adapt the process data model](../ex3/README.md)**

Back to the [Overview](../../README.md)
