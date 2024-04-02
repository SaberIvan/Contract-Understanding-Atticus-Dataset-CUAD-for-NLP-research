# Project Overview

This project comprises two distinct parts: a Cloud Computing Assignment focusing on the use of Spark RDD API for text analysis in cloud environments, and a RAKE Implementation Report that applies the Rapid Automatic Keyword Extraction (RAKE) algorithm for keyword extraction in natural language processing (NLP). Each part contributes to the understanding and practical application of cloud computing and NLP methodologies.

## Table of Contents

- [Cloud Computing Assignment (COMP5349)](#cloud-computing-assignment-comp5349)
- [RAKE Implementation Report](#rake-implementation-report)
- [Deployment on AWS EC2 with YARN Cluster](#deployment-on-aws-ec2-with-yarn-cluster)
- [Conclusion](#conclusion)

## Cloud Computing Assignment (COMP5349)

### Introduction

Designed by Dr. Ying Zhou, this assignment challenges students to extract keywords from legal documents using the Spark RDD API. It utilizes a dataset adapted from the Contract Understanding Atticus Dataset (CUAD), comprising over 13,000 clauses from 510 legal contracts.

### Task Overview

Students are tasked with implementing an extraction algorithm using basic Spark RDD API operations to analyze "Governing Law", "Change of Control", and "Anti-assignment" clauses. The goal is to extract the top 20 keywords from these categories.

### Deliverables

Submissions include a Jupyter notebook with the implemented solution, a README file with execution instructions on Google Colab, and a detailed report on the implementation's data flow and RDD usage.

## RAKE Implementation Report

**

## Deployment on AWS EC2 with YARN Cluster

This section guides you through deploying your Spark application on an AWS EC2 instance within a YARN-managed cluster. We'll use the `spark-submit` command to deploy and run `Assignment2.py`, outputting the results to a specified location.

### Prerequisites

Before proceeding, ensure you have:

- An AWS account and basic knowledge of EC2 instances.
- A Spark cluster set up on AWS EC2 instances, configured to run with YARN as the cluster manager.
- The `Assignment2.py` Spark application ready for deployment.

### Steps for Deployment

1. **Log into Your EC2 Instance:**

   
   Use SSH to connect to your master EC2 instance where Spark is configured:

   ```bash
   ssh -i /path/to/your-key.pem ec2-user@your-ec2-instance-public-dns
   
2. **Navigate to Your Spark Application Directory:**
cd /path/to/your-spark-application-directory
3. **Deploy and Run Your Spark Application:**
sh submit_cluster.sh
Ensure submit_cluster.sh contains the appropriate spark-submit command tailored to your project and environment, similar to the one provided in the previous instructions.

Conclusion
Integrating cloud computing with NLP through Spark's RDD API and the RAKE algorithm, this project underscores the importance of efficient data processing and keyword extraction. It demonstrates the practical application of these technologies in extracting meaningful information from large datasets, offering valuable insights into cloud computing and NLP fields.

