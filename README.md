# Procure-to-Pay Process Mining Analysis

## Overview
This repository contains a **process mining analysis** of the Procure-to-Pay (P2P) workflow using Python. The analysis identifies **bottlenecks, delays, and high-frequency activities** by combining data-driven metrics, network analysis, and PM4Py process mining techniques.

The goal is to help organizations understand where their P2P process can be optimized for efficiency.

---

## Dataset
- **Filename:** `P2P_EventLog_ProcessMining.xlsx`
- **Columns Required:**
  - `Case ID`: Unique identifier for each process instance
  - `Activity`: Name of the activity performed
  - `Timestamp`: Date and time of the activity
- **Notes:** The dataset can be split into multiple logs for decentralized or federated analysis.

---

## Features / Analysis

1. **Activity Frequency Analysis**
   - Counts occurrences of each activity.
   - Identifies high-frequency steps that may cause congestion.

2. **Time-based Bottleneck Detection**
   - Calculates the time difference between consecutive activities per case.
   - Determines activities with high average delays.

3. **Network-based Analysis**
   - Builds a directed graph of activity transitions.
   - Uses **degree centrality** to detect critical activities (structural bottlenecks).

4. **Process Mining with PM4Py**
   - Generates a **Process Tree** using the Inductive Miner.
   - Converts to a **Petri Net** for formal visualization of process flows.

---

## Installation

```bash
# Install dependencies
pip install pandas networkx pm4py openpyxl
