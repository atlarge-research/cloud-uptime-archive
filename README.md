# Cloud Uptime Archive (CUA)

The cloud uptime archive is a collection of failure traces from different cloud services. The cleaned and extracted traces are located in the `traces` folder. For some services, the traces have been collected from both the service operator and user reports to failure reporting websites such as Outage Report.

The traces folder contains a different csv file for each service-source pair. Each trace is in the following format:

| Start time  | End time | Severity |
| ----------- | -------- | -------- |
| timestamp   | timestamp| value between 0-1      |
| ...         | ...      | ...      |

Start time corresponds to the start time of the failure, and end time corresponds to the end time. Severity is a synthetic metric we generate based on the number of services and users affected. It can be interpreted as the probability that a task or a user request will fail in the time period represented by the start time and end time.

### Analysis scripts

The scripts to analyze the data to produce the figures in the paper are in the `analysis_scripts` folder.

### Simulation configuration

The CUA uses the [OpenDC](https://github.com/atlarge-research/opendc) simulator for experiments. The experiment configurations we use are in the `simulation_config` folder.

### Raw data processing

The code to clean and extract failure traces from the data is also include in the repository, in the `process_raw_data` folder. However, the raw data itself is not included as it is large. The raw dataset is available on Zenodo.
