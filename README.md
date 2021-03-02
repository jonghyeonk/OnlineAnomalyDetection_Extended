# Online anomaly detection using statistical leverage for streaming business process events
This repository shows developed algorithm of adjected leverage score and online anomaly detection for event log.
The algorithm of online anomaly detection is coded using statistical package R as seen in folder "code" and it calculates anomaly score for each case in trace level and designs the anomaly score for online setting. 

## Prepared Data1 - 2 artifical logs
We used 2 types of process models including small, medium refered from [2] to generate artificial logs. In process models of small and medium, we injected 5 types of anomaly patterns including "insert", "skip", "early", "late", and "rework" used in [2]

## Prepared Data2 - 1 real-life logs
For real-life logs, we used Helpdesk log which contains events logged by a ticketing management system of the help desk of an Italian software company.
About anomaly patterns, we injected 5 types of anomaly patterns as same with artificial logs.

The statistics of datasets are summarised in Table 2 in our paper.


## References
[2] Nolle, T., Luettgen, S., Seeliger, A., & Mühlhäuser, M. (2019). Binet: Multi-perspective business process anomaly classification. Information Systems, 101458.

