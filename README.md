# Keeping our rivers clean: information-theoretic online anomaly detection for streaming business process events
This repository shows developed algorithm of adjected leverage score and online setting for anomaly detection over event streams.
The algorithm of online anomaly detection is coded using statistical package R as seen in folder "code" and it calculates anomaly score for each case in trace level and designs the anomaly score for online setting. 

## Prepared Data1 - 5 artificial logs
We used 5 types of process models including small, medium, large, huge, and wide refered from [2] to generate artificial logs. 

## Prepared Data2 - 2 artificial logs
The second arficial logs are generated by simulating two BPMN processes loosely modelled based on real world processes using the BIMP process simulator. The process Credit refers to the processing of credit card applicationsat a bank, whereas the Pub log refers to the process of preparing and servingfood at a restaurant. 

## Prepared Data3 - 3 real-life logs
For the real life logs, we consider the Helpdesk event log contain-ing events logged by a ticketing management system of the help desk of an Italian software company,  the Hospital Billing event log containing events about the billing of medical services that have been obtained from the financial modules of the ERP system of a regional hospital, and the BPIC2013 event log representing an incident and problem management process from Volvo IT.

For all logs, we injected 6 types of anomaly patterns including "insert", "skip", "early", "late", "replace", and "rework" used in [1,2,3]. The statistics of datasets are summarised in Table 2 in our paper.

## Options in online setting
There are 3 design options: Prefix-length or Trace-level (batch=True/False in streaming_score function of code), Deep_embedding (embedding_size_p = rate in [0,1], if 0, deep embedding will not be applied), and Removing (remove = True/False). Note that, in paper, the deep_embedding option has not been introduced since it does not show any interesting point for us. 

## Performance comparison with baselines (OC-SVM, iForest)

![aa](./data/t1.PNG){: width="80%" height="80%"}
![aa](./data/t2.PNG){: width="80%" height="80%"}


&#x1F53A; Be careful to correctly set your working directory for each R file as uploaded files contain my own local directory.

## References
[1] Nguyen, H. T. C., Lee, S., Kim, J., Ko, J., & Comuzzi, M. (2019). Autoencoders for improving quality of process event logs. Expert Systems with Applications, 131, 132-147.

[2] Nolle, T., Luettgen, S., Seeliger, A., & Mühlhäuser, M. (2019). Binet: Multi-perspective business process anomaly classification. Information Systems, 101458.

[3] Ko, J., & Comuzzi, M. (2021). Detecting anomalies in business process event logs using statistical leverage. Information Sciences, 549, 53-67.
