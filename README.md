**Problem Statement**  
Classify network traffic flows as benign or malicious

**Target Accuracy Measures** (for competitive model)  
1. Relatively low (<10%) false positive rate - accuracy  
2. Near perfect (>99%) rate of capturing all true positives - recall  
3. As little data as possible

ABOUT THE DATASET

**A Realistic Cyber Defense Dataset (CSE-CIC-IDS2018) was accessed on 03/24/2024 from https://registry.opendata.aws/cse-cic-ids2018**

CSE-CIC-IDS2018 from Canadian Institute of Cybersecurity
Link for more detail - https://registry.opendata.aws/cse-cic-ids2018/

We have folder that contains the processed packet captures from days of typical traffic with attacks periodically throughout. The packets are organized into flows using CIC Flow Meter.

Flows are just the start to finish communication between two IP's and includes all the packets sent between them during the communication.

**How do we reduce the size of the dataset**
1. Optimize the normal data so that our model can learn the trends with as little duplicate data as possible, maybe only take a subset of flows where the source and destination are both internal to our network.

2. Reduce the dimensionality of the dataset by removing entire features that we find to be ineffective, 80 features is likely far beyond what we actually need with a dataset this large.