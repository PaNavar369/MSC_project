# MSC_Project

## MSc Thesis Project on Centralized and Distributed Machine Learning for Large-Scale Web Traffic Data Processing

---

# Project Overview

This repository contains the implementation, experiments, and analysis conducted for my MSc thesis project focused on centralized and distributed machine learning architectures for large-scale web traffic data processing.

The project investigates how distributed computing frameworks such as Apache Hadoop and Apache Spark can improve scalability, fault tolerance, reliability, and computational efficiency when processing large datasets compared to traditional centralized systems.

The implementation includes data preprocessing, feature engineering, machine learning models, deep learning models, and comparative behavioural analysis using both centralized and distributed architectures.

---

# Research Objectives

The main objectives of this project are:

* To process and analyze large-scale web traffic datasets
* To implement centralized and distributed machine learning pipelines
* To evaluate system scalability and performance
* To compare centralized and distributed architectures
* To investigate computational efficiency using Hadoop and Spark ecosystems

---

# Technologies and Frameworks

## Operating System

* Ubuntu Server 24.04 LTS

## Development Environment

The following frameworks and software components were installed and configured:

* Python 3.x
* OpenJDK 11
* Apache Hadoop
* Hadoop Distributed File System (HDFS)
* Apache Spark (PySpark)
* Jupyter Notebook

---

# Libraries Used

* Pandas
* NumPy
* Scikit-learn
* TensorFlow
* Keras
* Matplotlib
* Seaborn
* PySpark

---

# System Implementation

## Step 1: System Update

```bash
sudo apt update
sudo apt upgrade
```

---

## Step 2: Java Installation

```bash
sudo apt install openjdk-11-jdk
java -version
```

---

## Step 3: Python and Package Installation

```bash
sudo apt install python3-pip

pip install pandas numpy scikit-learn tensorflow keras matplotlib seaborn pyspark
```

---

## Step 4: Hadoop and HDFS Configuration

Apache Hadoop was installed and configured to support distributed storage and fault-tolerant data management.

### HDFS Initialization

```bash
hdfs namenode -format
start-dfs.sh
start-yarn.sh
jps
```

### Features Provided by HDFS

* Distributed storage
* Block-level replication
* Fault tolerance
* Scalability
* High-throughput access

---

## Step 5: Apache Spark Configuration

Apache Spark was integrated with Hadoop to enable distributed computation and large-scale data processing.

### Spark Services

```bash
start-all.sh
```

### Dedicated PySpark Environment

A separate virtual environment was used to avoid PySpark kernel instability issues.

```bash
source ~/pyspark_env/bin/activate
```

---

## Step 6: Dataset Upload to HDFS

The web traffic dataset obtained from Kaggle was uploaded into HDFS using:

```bash
hdfs dfs -mkdir /data
hdfs dfs -put train_1.csv /data
```

---

## Step 7: Data Processing using PySpark

PySpark transformations were implemented to:

* Read datasets from HDFS
* Perform data cleaning
* Handle missing values
* Conduct feature engineering
* Prepare training datasets

---

# Machine Learning and Deep Learning Models

## Centralized Architecture Models

The following models were implemented in the centralized environment:

* Logistic Regression (LR)
* Decision Tree (DT)
* Random Forest (RF)
* Artificial Neural Network (ANN)
* Gated Recurrent Unit (GRU)

---

## Distributed Architecture Models

The following distributed models were implemented using Spark-based architectures:

* Distributed Logistic Regression
* Distributed Decision Tree
* Distributed Random Forest
* Distributed ANN
* Distributed GRU

---

# Google Colab Implementation

The GRU model was additionally implemented using Google Colab due to computational limitations on local infrastructure.

Relevant parquet datasets were utilized during the distributed deep learning experiments.

---

# Performance Evaluation

The implemented systems and models were evaluated using multiple metrics.

## Classification Metrics

* Accuracy
* Precision
* Recall
* F1-score

## Computational Metrics

* Training Time
* Execution Time
* Memory Utilization

## Behavioural Metrics

* Reliability
* Scalability
* Fault Tolerance
* System Availability

---

# Project Structure

```text
```text
MSC_Project/
│
├── data/
│   │
│   ├── raw_data/
│   │   ├── train_1.csv
│   │   └── train_2.csv
│   │
│   └── processed_data/
│       ├── feature_engineering/
│       ├── pyspark_transformations/
│       └── system_state/
│
├── notebooks/
│   │
│   ├── Feature_Engineering.ipynb
│   ├── Pyspark_Transformations.ipynb
│   ├── centralized_ML.ipynb
│   ├── centralized_DL.ipynb
│   ├── distributed_ML.ipynb
│   ├── Distributed_DL.ipynb
│   ├── GRU_Google_Colab.ipynb
│   ├── comparison_behavioural.ipynb
│   └── system_state.ipynb
│
├── distributed_csv/
│
├── sample_1m_parquet/
│
├── sample_3m_parquet/
│
├── sample_5m_parquet/
│
├── results/
│   │
│   ├── ann_scalability_results.csv
│   └── comparison_results.csv
│
├── centralized_DL.ipynb
│
├── comparison.ipynb
│
└── README.md
```

```

---

# Installation Guide

## Clone the Repository

```bash
git clone https://github.com/PaNavar369/MSC_Project.git
cd MSC_Project
```

---

## Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Run notebooks sequentially according to the workflow:

1. Feature Engineering
2. PySpark Transformations
3. Centralized ML Models
4. Distributed ML Models
5. Deep Learning Models
6. Behavioural Comparison

---

# Dataset Information

# Dataset Source

The dataset used in this project was obtained from Kaggle.

Dataset Link:

```text
https://www.kaggle.com/c/web-traffic-time-series-forecasting/data


```

The dataset was used for large-scale web traffic analysis, preprocessing, feature engineering, and distributed machine learning experiments using Hadoop and Apache Spark.


```text
data/
sample_1m_parquet/
sample_3m_parquet/
sample_5m_parquet/
```

---

# Git Ignore Recommendations

Example `.gitignore` configuration:

```gitignore
*.parquet
*.csv
.ipynb_checkpoints/
outputs/
__pycache__/
```

---

# Future Improvements

Possible future extensions include:

* Hyperparameter optimization
* Real-time streaming analytics
* Distributed GPU training
* Kubernetes deployment
* Advanced fault-tolerant pipelines
* Cloud-based distributed computing integration

---

# Author

PaNavar369

---

# License

This project is intended for academic and research purposes only.
