# Exercise 3: Adapt the process data model

In the previous exercise we analysed standard activities related to 'Sell from Stock' process. In this exercise we'll further extend the process data model to also another Business Events and context data out of the connected SAP S/4HANA Cloud system.



## Exercise 3.1 Navigate to the process data model

1. Click `Process settings`
<br>![](images/3_001.png)

2. Under tab `Data` click `View`
<br>![](images/3_002.png)

This will lead you to the underlying process data model. 

Process data management involves a wide range of tasks, such as extracting, transforming, and loading data. A process data pipeline is used to carry out these tasks. The process data pipeline regularly extracts data from a source system, transforms it, and loads it into a process. So, process analysts can always investigate latest representations of a process.


## Exercise 3.2 Add further Events

1. Click `Sales Order` in the process data pipeline step to open the Event collector
<br>![](images/3_003.png)

2. Click `Add event collector`
<br>![](images/3_004.png)

3. Copy & paste the following code into the new collector. You might also rename it to `Block delivery`
```
SELECT
    'Block delivery for Sales Order' as c_eventname,
    replace(ltrim(replace(SAPBusinessObjectNodeKey1, '0', ' ')), ' ', '0') AS c_caseid, /* remove leading zeros */
    FROM_UNIXTIME(BusEvtLogCreationDateTime / 1000) AS c_time, 
    CreatedByUser AS CreatedByUser,
    IsTechnicalUser
FROM 
   C_BusEvtLogEventDEX AS e
   LEFT JOIN  C_BusEvtLogPayloadDEX as p ON e.businesseventuuid = p.businesseventuuid
WHERE 
   e.SAPObjectType = 'SalesOrder' AND
   e.SAPObjectNodeType != 'SalesOrderItem' AND
   e.BusinessEventType = 'OvrlDlvBlkStsChgd' AND
   p.BusEvtLogNewFieldValue IN ('C') -- C=blocked
```
The SQL-based transformation add the new event to our process instances (*Cases*; each case equals to a single Sales Order).

4. Click the `preview` button to check if the extractor returns entries
<br>![](images/3_011.png)

5. Note, to find further events open [api.sap.com](api.ap.com), navigate to `S/4HANA Cloud` -> `Events`
<br>![](images/3_005.png)

Further details can be found in `Event reference` as well as in the `Business Documentation`. Follow the links to learn more about the underlying process details. 


## Exercise 3.3 Add further case attributes

1. Select `Case attributes` and search for column `DistributionChannel`, add it to the case attributes in the SQL editor (Mind the comma!).
<br>![](images/3_006.png)

2. Click the `preview` button to check if the new column was added correctly
<br>![](images/3_011.png)

3. Note, to learn more about the S/4HANA virtual data model go to [api.sap.com](api.ap.com), navigate to `S/4HANA Cloud` -> `CDS Views`
<br>![](images/3_007.png)

4. Navigate back to the pipeline overview
<br>![](images/3_008.png)


## Exercise 3.4 Retrieve the latest data out of the productive S/4HANA Cloud system

1. Click `Run T&L` to run the transform & load step. 
<br>![](images/3_009.png)
<br>Note: Click the ETL button will also retrieve the latest delta out of the actual S/4HANA Cloud backend,
<br>Note: During the exercise all participants are connected to the very same system and clicking ETL will lead to additional delays. 

2. Find the pipeline logs below the pipeline overview and click the latest entry to see the progress of the transform and load steps. 
<br>![](images/3_010.png)

3. Wait until both indicators show a green status
<br>![](images/3_012.png)

Note: in case of errors click the log entry to find further details about the error. You might need to fix/adjust your extraction scripts and re-run T&L.

4. Click target of the process pipeline to navigate again into the investigation view. 
<br>![](images/3_013.png)


## Summary

You've now added further events and attributes to the process data model. You can and work with the additional  context in your investigation. 

Continue to - [Exercise 4: Investigate and improve your process](../ex4/README.md)
