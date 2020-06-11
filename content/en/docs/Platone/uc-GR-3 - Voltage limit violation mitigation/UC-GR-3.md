# 1. Description of the Use Case

## 1.1. Name of the Use Case

*Use case identification*
| ID  | Area /Domain(s)/Zone(s)| Name of the Use Case |
| --- | ---                    | ---                  |
| UC-GR-3| Area: Energy system </br> Domains: Distribution, DER, Customer Premises/ </br> Zones: Station, Operation  </br> | Voltage limit violation mitigation |

***Notes:***
* **ID** - uniqe identification label: DE-1/GR-3/IT-2
* **Area /Domain(s)/Zone(s)** - placement of the use case in the SGAM domains and zones. It can be left blank if you are not sure.

## 1.2. Version Management

*Version management*
|Version No.|Date     |Name of author(s)|Changes|Approval status|
|---        |---      |---              |---    |---            |
|0.1|17th June 2020|Panagiotis Pediaditis, Themistoklis Xygkis, Dimitris Stratogiannis, Eleni Daridou, Stavroula Tzioka|Initial creation|Draft|

## 1.3. Scope and Objectives of Use Case

*Scope and objectives of use case*
|||
| --- | --- |
| Scope | The scope of the UC is to examine the operational use of flexibility tools in order to satisfy EN50160 in case of a voltage level violation in the distribution network and especially in MV lines with flexible loads availability. The DSO will examine the operation of tools and services for decision making support to mitigate voltage violations, assuming that the grid state estimation has a good degree of certainty . <br/> Network: MV <br/> Markets: Near Real Time|
| **Objective(s)** | * To monitor and control the voltage level at a network node always into the operational limit. <br/> * To immediately respond in case of a violation employing flexibility capabilities.|
| **Related business case(s)** |add text|

***Notes:***
* **Scope** - describes the aims and boundaries of the use case in a short, precise text.
* **Objective(s)** - goals of the use case, in form of bullet points and a short headline.
* **Realted business case(s)** - optional

## 1.4. Narrative of Use Case


**Short description**
Various types of flexible loads -aggregated for the scope of the Use Case- react to network tariffs sent by the DSO, so that voltage limit violation is mitigated.

**Complete description**
Customers with flexible loads are connected to the distribution network and their loads are considered aggregated for the scope of the UCs regarding their management in the MV level. State of the network is known with a good degree of certainty based on the available measurements and the topology via the AMR, GIS and SCADA data. In the first case: a) via the state estimation tool, it is identified that a voltage limit is violated on a node, in a second case: b) an alarm coming from the SCADA/DMS informs us for an undervoltage in an MV line that is controlled by DSO Regional Control Centre. The alarm signal is transferred in the DSO technical platform via an API and the information is shared with the appropriate tools and services. The DSO calculated and communicated the appropriate network tariffs that reflect the situation of the network. The flexible loads react to these tariffs and the problem is mitigated.

add text - longer narrative from user viewpoint about *what* happens *how*, *where*, *when*, *why* and *under which assumptions*. It has to be written in a way that it can also be understood by non-experts.


## 1.5. Key Performance Indicatiors (KPI)

|ID   |Name   | Description   | Reference to mentioned use case objectives|
|-----|-------|---------------|-------------------------------------------|
|add text|add text|add text|add text|

***Notes:***
Can be left blank now

## 1.6. Use case conditions

|Assumptions| Prerequisites|
|-----------|-------------|
|add text| add text|

***Notes:***
* **Assumptions** - general presumptions about conditions or system configurations (e.g. customer's consent required for some steps; simulation of TSO)
* **Prerequisites** - specify which requirements have to be met so that the basis scenario use case can be successfully accomplished.


## 1.7. Further information to the use case for classification/mapping

OPTIONAL - you can leave it blank

|Relation to other use cases|
|---------------------------|
|include uc-GR-1 and potentially uc-GR-2|
|**Level of depth**|
|detailed|
|**Prioritisation**|
|obligatory|
|**Generic, regional or national relation**|
|generic|
|**Nature of the use cases**|
|technical, market|
|**Further keywords for classification**|
|add text|

***Notes:***
* **Relation to other use cases** - relation to other use cases in the same project or thematic area. Possible relation types are for instance include, extend, invoke, or associate.
* **Level of depth** - reflects the degree of specialisation of the use case. Although no common notation is settled, descriptions like high level use case, generic, detailed, or specialised use case are often used.
* **Prioritisation** - helps to rate the use cases in a project from very important to nice-to-have with labels like obligatory/mandatory or optional which have to be agreed upon beforehand.
* **Generic, regional or national relation** - for the purpose of generalisation if use case is applied to areas where restictions by law or silimiar issues occur.
* **Nature of the use cases** - describes the viewpoint and field of attention like *technical, political, business/market, test*, etc.


## 1.8. General remarks

|General remarks|
|---|
|- add text <br/> - add text <br/> - add text|

***Notes:***
Add any remarks which do not fit in any other category

# 2. Diagrams of Use Case

\&lt;! Example for img1: {{\&lt; imgproc img\_1 Fit &quot;600x400&quot; \&gt;}} Diagram 1 {{\&lt; /imgproc \&gt;}} !\&gt;

# 3. Technical Details

## 3.1. Actors

| **Actor Name** | **Actor Type** | **Actor Description** | **Further information specific to this Use Case** |
| --- | --- | --- | --- |
| DSO | Person | add text| DMS, DSO technical Platform , PMUs , State estimation tool, Measurement Data, Network topology|
| Residential consumer | Person | add text| Load information (aggregated) and Measurements|
| Commercial consumer | Person | add text| Load information (aggregated) and Measurements|
| Aggregator| Person | add text| add text|
| RES production| Person | add text| Measurements|
| State Estimation tool| System | Tool that allows and assists the use of other DMS services and applications to provide network state estimation, improvement of measurement data reliability and better network observability | Alarm sent by the State Estimation tool is the triggering event for this Use Case|

***Notes:***
* **Actor Type** - Device/ Sytem/ Person

## 3.2. References

OPTIONAL - you can leave it blank

| **No.** | **References Type** | **Reference** | **Status** | **Impact on Use Case** | **Organistaor / Organisation** | **Link** |
| --- | --- | --- | --- | --- | --- | --- |
|add text|add text|add text|add text|add text|add text|


# 4. Step by Step Analysis of Use Case

## 4.1. Overview of Scenarios

| **No.** | **Scenario Name** | **Primary Actor** | **Triggering Event** | **Pre-Condition** | **Post-Condition** |
| --- | --- | --- | --- | --- | --- |
| 1 | Voltage limit violation mitigated| SCADA | Voltage measurements of a node/multiple nodes out of permissible range |Distribution network observability | Voltage limit violation mitigated |
| 2 | Voltage limit violation mitigated-Alarm via the State Estimation tool| SCADA | Voltage measurements of a node/multiple nodes out of permissible range |Distribution network observability | Voltage limit violation mitigated |
| 3 | Voltage limit violation not mitigated| SCADA | Voltage measurements of a node/multiple nodes out of permissible range |Distribution network observability | Voltage limit violation not mitigated |

***Notes***
This part describes the possible scenarios of the use case. The scenarios should comply with the sequence diagrams in Sect. 2 of the template, so that every step describes one part of a communication or action. Apart from a normal success scenario, different failure scenarios or alternatives can be included to describe situations where preconditions are not satisfied or unwanted states are attained.
* **Primary Actor** - the first actor appearing in the scenario at the incident causing the scenario to begin.
* **Triggering Event** - the incident causing the scenario to begin.
* **Pre-Condition** - indicates which terms have to be fulfilled for the scenario to be executed.
* **Post-Condition** - indicates which terms should be valid after the scenario. TIt can also specify whether a scenario has been successfully completed or not.

## 4.2. Steps – Scenarios

**Scenario Name: No. 1 - Voltage limit violation mitigated**

| **Step No.** | **Event.** | **Name of Process/ Activity** | **Description of Process/ Activity.** | **Service** | **Information Producer (Actor)** | **Information Receiver (Actor)** | **Information Exchanged** | **Requirements, R-ID** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 |Measurements of voltage at a node/multiple nodes out of the permissible range|Alarm generation|Alarm informing the DSO about the thermal line limit violation|CREATE|SCADA|DSO|Alarm||
| 2 |Alarm informing the DSO about the voltage limit violation|Tariffs calculation|Tariffs calculation that reflect the situation of the network|EXECUTE|DNO|DNO|Network tariffs||
| 3 |Tariffs calculation|Tariffs communication|Tariffs are communicated to the Aggregator|CREATE|DSO|Aggregator|Network tariffs||
| 4 |Tariffs communication|Setpoint sent to Residential Customer| Sending setpoint to the flexibility load|CREATE|Aggregator|Residential consumer|Setpoint||
| 5 |Tariffs communication|Setpoint sent to Commercial Customer| Sending setpoint to the flexibility load|CREATE|Aggregator|Commercial consumer|Setpoint||
| 6 |Tariffs communication|Setpoint sent to RES| Sending setpoint to the RES producer|CREATE|Aggregator|RES production|Setpoint||
| 7 |Setpoints sent to flexibility loads|Data Aquisition|New Distribution Network state (Distribution Network state updated following the Aggregator's response)|CHANGE|SCADA,DMS,GIS,AMR|DSO|Measurements||

**Scenario Name: No. 2 - Voltage limit violation mitigated - Alarm via the State Estimation tool**

| **Step No.** | **Event.** | **Name of Process/ Activity** | **Description of Process/ Activity.** | **Service** | **Information Producer (Actor)** | **Information Receiver (Actor)** | **Information Exchanged** | **Requirements, R-ID** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 |Measurements from the Distribution Network|Data Aquisition| Various field measurements that reflect the network state are communicated |REPORT|SCADA,DMS,GIS,AMR|State Estimation tool|Measurements||
| 2 |Measurements of voltage at a node/multiple nodes out of the permissible range|Alarm generation|Alarm informing the DSO about the thermal line limit violation|CREATE|State Estimation tool|DSO|Alarm||
| 3 |Alarm informing the DSO about the voltage limit violation|Tariffs calculation|Tariffs calculation that reflect the situation of the network|EXECUTE|DNO|DNO|Network tariffs||
| 4 |Tariffs calculation|Tariffs communication|Tariffs are communicated to the Aggregator|CREATE|DSO|Aggregator|Network tariffs||
| 5 |Tariffs communication|Setpoint sent to Residential Customer| Sending setpoint to the flexibility load|CREATE|Aggregator|Residential consumer|Setpoint||
| 6 |Tariffs communication|Setpoint sent to Commercial Customer| Sending setpoint to the flexibility load|CREATE|Aggregator|Commercial consumer|Setpoint||
| 7 |Tariffs communication|Setpoint sent to RES| Sending setpoint to the RES producer|CREATE|Aggregator|RES production|Setpoint||
| 8 |Setpoints sent to flexibility loads|Data Aquisition|New Distribution Network state (Distribution Network state updated following the Aggregator's response)|CHANGE|SCADA,DMS,GIS,AMR|DSO|Measurements||

**Scenario Name: No. 3 - Voltage limit violation not mitigated**

| **Step No.** | **Event.** | **Name of Process/ Activity** | **Description of Process/ Activity.** | **Service** | **Information Producer (Actor)** | **Information Receiver (Actor)** | **Information Exchanged (IDs)** | **Requirements, R-ID** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 |Measurements from the Distribution Network|Data Aquisition| Various field measurements that reflect the network state are communicated |REPORT|SCADA,DMS,GIS,AMR|State Estimation tool|Measurements||
| 2 |Measurements of voltage at a node/multiple nodes out of the permissible range|Alarm generation|Alarm informing the DSO about the thermal line limit violation|CREATE|State Estimation tool|DSO|Alarm||
| 3 |Alarm informing the DSO about the voltage limit violation|Tariffs calculation|Tariffs calculation that reflect the situation of the network|EXECUTE|DNO|DNO|Network tariffs||
| 4 |Tariffs calculation|Tariffs communication|Tariffs are communicated to the Aggregator but the Aggregator does not respond to it and does not take further action|CREATE|DSO|Aggregator|Network tariffs||


***Notes***
This part describes the possible scenarios of the use case. The scenarios should comply with the sequence diagrams in Sect. 2 of the template, so that every step describes one part of a communication or action. Apart from a normal success scenario, different failure scenarios or alternatives can be included to describe situations where preconditions are not satisfied or unwanted states are attained.
* **Event** - Event triggering a step, specific for that use case.
* **Name of Process/ Activity** - general classification of process/activity (e.g. data aquisition).
* **Description of Process/ Activity** - more detailed description of the step.
* **Service** - addresses the nature of the information flow. Possible: GET (The information receiver obtains information from the
information producer after an implicit request.), CREATE (The information producer creates an information object.), CHANGE (The information producer performs an update of the information at the information receiver’s.), DELETE (The information producer deletes information of the receiver.), CANCEL/CLOSE (A process is terminated.), EXECUTE (An action or service is performed.), REPORT (The information producer supplies information of its own account.), TIMER (The actor which represents both information producer
and receiver has to enforce a waiting period.), REPEAT (A number of steps has to be repeated until a break condition (stated in the field Event) is satisfied. The contemplated steps have to be added in parentheses.).
* **Information Producer and Receiver (Actor)** - actors from actor list in section 3.1
* **Information exchanged (IDs)** - ID of the information defined further in section 5

# 5. Information Exchanged

|**Information exchanged ID**|**Name of Information** | **Description of Information Exchanged** | **Requirements to information data** |
| --- | --- | --- | --- |
|I-01|Measurements|Measurements from the Distribution Network (e.g. voltage levels, power injections, etc)||
|I-02|State Vector|Voltage magnitudes and angles of all network buses||
|I-03|Alarm| Alarm about the thermal line limit violation||
|I-04|Network tariffs|Network tariffs that reflect the Disribution Network state||
|I-05|Setpoint|Setpoint for adjustment of flexible load/RES production||

***Notes***
* **Information exchanged ID** - unique number (I-01,I-02...) for identification
* **Requirements to information data** - optional, defined in section 6

# 6. Requirements (optional)

# 7. Common Terms and Definitions

| **Term** | **Definition** |
| --- | --- |
|Dynamic tariffs|Price signals communicated to the flexible loads in order to incentivise their behaviour.|


# 8. Custom Information (optional)

| **Key** | **Value** | **Refers to Section** |
| --- | --- | --- |
|||
