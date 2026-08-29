# Data Analytics Projects
**Author**: Jacob Joshua
___

## Project 1: [Supply Chain Service Level Tracking Analysis & ELT Modelling](https://github.com/jacobdbt2100/supply-chain-service-level-tracking)

<img src="https://raw.githubusercontent.com/jacobdbt2100/supply-chain-service-level-tracking/main/dashboards/service_level_report.jpg" width="1000">

[...view project repo](https://github.com/jacobdbt2100/supply-chain-service-level-tracking)

Developed warehouse-ready operations analytics models and reporting workflows for supply chain service-level tracking using Python, SQL, dbt, and Power BI.

Analysed fulfilment reliability and delivery performance using OTIF, On-Time, In-Full, Line Fill Rate, and Volume Fill Rate metrics to support KPI monitoring, operational benchmarking, and service-level analysis.

## Project 2: [Monitoring & Evaluation System for Smallholder Farm Productivity](https://github.com/jacobdbt2100/Monitoring-and-Evaluation-System)

<img src="https://raw.githubusercontent.com/jacobdbt2100/Monitoring-and-Evaluation-System/main/power%20bi%20report/01_programme%20overview.jpg" width="1200">

[...view project repo](https://github.com/jacobdbt2100/Monitoring-and-Evaluation-System)

Developed an end-to-end monitoring and evaluation system for an agricultural development programme covering digital data collection, case management, data processing, programme performance monitoring, and executive reporting.

Built a structured data workflow using CommCare, Python, PostgreSQL, SQL, Excel, and Power BI to track programme reach, training, input distribution, farm monitoring, adoption of recommended practices, and data quality.

## Project 3: [Manufacturing Downtime Analysis](https://github.com/jacobdbt2100/Manufacturing-Downtime-Analysis/tree/main)

<img src="https://raw.githubusercontent.com/jakejosh6751/Manufacturing-Downtime-Analysis-/main/manufacturing downtime report.jpg" width="1000">

[...view project repo](https://github.com/jacobdbt2100/Manufacturing-Downtime-Analysis/tree/main)

Developed an operations analytics report to evaluate manufacturing downtime drivers, production efficiency, and operational disruptions across production batches and downtime factors.

Analysed downtime patterns using line efficiency, Pareto analysis, and operator-related downtime metrics to identify major production bottlenecks and operational risks.

## Project 4: [Trial Activation & Conversion Behaviour Analysis with ELT Modelling](https://github.com/jacobdbt2100/trial_activation_analysis)

<img src="https://raw.githubusercontent.com/jacobdbt2100/trial_activation_analysis/main/notebooks/03_descriptive_analysis_and_product_metrics_output.png" width="1200">

[...view project repo](https://github.com/jacobdbt2100/trial_activation_analysis)

Built an analytics-ready product analytics workflow for a SaaS workforce management platform to analyse trial activation and conversion behaviour across 102k+ cleaned product events.

Applied behavioural segmentation, chi-square testing, Mann–Whitney U testing, logistic regression, and layered dbt models to evaluate activation hypotheses, onboarding effectiveness, and conversion patterns.
___









This is a statement with a footnote. [^1]

[^1]: This is the footnote text.


Databricks uses Delta Lake.[^delta]

[^delta]: Delta Lake provides ACID transactions and other reliability features.




## 13.0. Project Updates [^13]

This section documents **issues, observations, and design improvements** identified during or after project implementation. Updates will be made periodically rather than for every individual observation, particularly where changes would require extensive revisions to completed components.

The purpose is to preserve lessons from the current project for future implementations and avoid repeating identified issues when developing similar systems for actual programmes.

[^13]: ### 13.1. Data Collection Forms

**Training Attendance**

Question 5, **“Did the farmer attend the training?”**, can be omitted from the Training Attendance form. Where the form is completed only for farmers who attended, the question is redundant because attendance is already established by the submission. **Attendance Status** (Full Attendance or Partial Attendance) is sufficient for recording the level of attendance.

### [^13]: 13.2. Synthetic Data Generation

**Training Attendance**

The current synthetic data generation logic should be refined to better reflect realistic training-session participation. The generated data contains **845 training sessions but only 779 training attendance records**, with **99 sessions having no recorded attendees** and some other sessions having only a very small number of farmer records.

Future revisions should generate multiple farmer-level attendance records per training session, with realistic session sizes and attendance outcomes. This will produce a more credible relationship between **Training Sessions Conducted**, **Training Attendance Records**, and **Farmers Trained**.

### 13.3. Date Slicer

Enable Filtering by Follow-Up Date
