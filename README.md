# Project Summary: Processing CUAD with Spark

## Overview

This project addresses the challenges of processing the Contract Understanding Atticus Dataset (CUAD) for NLP research in the legal domain. Due to the extensive length of legal contracts and the intricate structure of data, conventional processing methods can lead to inefficiencies and Out-of-Memory (OOM) issues. The project involves developing a Spark application to preprocess the data efficiently in parallel, leveraging the Spark RDD and SQL API capabilities for data transformation and analysis.

## Objectives

- **Data Preprocessing:** Convert raw CUAD data into a format suitable for NLP model inputs by segmenting contract texts into manageable sequences.
- **Performance Optimization:** Tune the Spark implementation and execution environment to enhance processing speed and reduce resource consumption.

## Implementation

### Data Flow

The processing begins with reading the CUAD dataset, followed by extracting three types of samples: positive, possible negative, and impossible negative. The `explode()` and `explode_outer()` functions in PySpark are utilized for data recombination and separation based on the "is_impossible" field. The contracts are then divided into sequences of 4096 bytes using a stride of 2048 bytes for efficient handling.

### Sample Extraction

- **Positive Samples:** Identified through the segmentation of contract contexts, adjusting start and end indices based on the segmented sequences.
- **Negative Samples:** Selection is based on the count of positive samples within the same contract, ensuring a balanced dataset for model training.

## Execution Plan

The application is executed via a `.sh` script that submits the Spark job to a cluster. It involves several steps, from reading the JSON file to splitting sequences, classifying samples, and writing the processed data back to JSON format. Performance tuning and scalability tests are conducted to ensure optimal resource usage and adaptability to different data sizes.

## Deployment on AWS EC2 with YARN Cluster

To deploy this Spark application on an AWS EC2 instance managed by a YARN cluster, follow these general steps:

1. **Set up an AWS EC2 instance** with the appropriate configuration for Spark and YARN.
2. **Deploy the Spark application** using the provided `.sh` script, customizing it for your AWS and Spark environment.
3. **Monitor and adjust** the Spark and EC2 settings based on performance observations to achieve optimal processing times and resource utilization.

## Conclusion

This project demonstrates an effective approach to preprocessing complex legal documents for NLP applications, showcasing the power of Spark in handling large datasets and the importance of performance tuning in distributed computing environments. By adapting to the scalable infrastructure provided by AWS EC2 and YARN, the project ensures efficient processing and flexibility in resource management.
