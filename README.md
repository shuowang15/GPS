# Vehicle GPS Trajectory Sample & Built Environment 

_Exploring how street connectivity and food environment around stopping points shape restaurant choices_

We appreciate your interest in this repository. Here we share a small, anonymized sample of original in‑vehicle GPS trajectory data (6 CSV files), together with the conceptual research idea that we are developing using such data. 

---

## 1. What’s in this Repository

- **6 raw GPS trajectory CSV files** recorded by private cars in Changsha, China.  
    Each file contains timestamps, longitude, land atitude. Vehicle IDs are fully anonymized (random bit strings), and no personal driver information is collected.
    
- **`data_dictionary.md`** – a brief description of the columns.
    
- **This README** – contextualizes the sample and outlines the research idea.
    

> The 6 CSV files contain the sample data **selected from the 183‑day collection period (July–December 2022) and used for the analysis in this study**. They are provided to help others understand the data format and to enable reproduction of the data processing steps or extension of related analyses.

---

## 2. Research Idea (Non‑confidential Overview)

### Background

Dining out is an increasingly common dietary pattern linked to chronic disease risk. While the home neighborhood food environment has been widely studied, less is known about the role of the built environment around **stopping points** – the locations where vehicle trips actually pause – in shaping restaurant choices.

### Objective (Work in Progress)

Using large‑scale vehicle trajectory data, we are investigating how **street connectivity** (road density) and **restaurant availability** around stopping points relate to the type of restaurant visited. Specifically, we compare **fast‑food** and **sit‑down restaurant** visits, and we examine whether the observed relationships vary across different spatial buffers (400 m to 3,000 m).

Our broader goal is to understand whether the environmental correlates of eating‑out behavior differ by restaurant type and by spatial scale, which could inform more targeted urban planning and public health interventions.

### General Approach

- **Stopping point identification**: Engine‑off events are filtered and spatially matched with POI data; dwell‑time criteria are applied to define visits.
    
- **Environmental variables**: Numbers of fast‑food and sit‑down restaurants, as well as total road length (and road density), are calculated within concentric buffers around each stopping point.
    
- **Statistical modeling**: Fixed‑effects logistic regression (or similar panel methods) is used to account for individual heterogeneity, temporal effects, weather, and land‑use mix.
    

### Expected Contribution

The work is intended to demonstrate how passively collected vehicle GPS data can be repurposed to study mobility‑based environmental exposures. Early explorations suggest distinct patterns for fast‑food and sit‑down establishments, but all substantive results are **under review and not disclosed here**.

_Once the manuscript is accepted for publication, we will update this repository with the full citation and, where possible, a preprint or link to the paper._

---

## 3. Data Source & Ethical Statement

The original, large‑scale trajectory dataset was collected by the group of **Prof. Zhu Xiao** at Hunan University, using devices installed with users’ fully informed consent. The collection and transmission process was purely anonymous:

- No personal information (driver identity, license plate, etc.) is stored.
    
- Vehicle identifiers are irreversibly anonymized.
    
- Data are used strictly for non‑profit, scientific research.
    

The 6 CSV files provided here are shared solely for non‑commercial scientific research and educational purposes. If you require the complete trajectory dataset, please follow the instructions in the repository below:
[PrivateCarTrajectoryData repository](https://github.com/HunanUniversityZhuXiao/PrivateCarTrajectoryData)

For any questions regarding the original data collection, you may contact **Prof. Zhu Xiao** ( zhxiao@hnu.edu.cn ).

---

## 4. How to Use This Sample

1. Load the CSV files using Python (pandas) or R to inspect the trajectory structure.
    
2. Adapt the ideas to your own urban context or to other health‑relevant behaviors.
    

> We kindly ask that any public use of this sample or its derivatives acknowledge both this repository and the original trajectory dataset.

---

## 5. License, Citation & Contact

The 6 sample CSV files are made available **free of charge for non‑commercial, scientific research**. By using the data, you agree to:

- Use them solely for non‑profit research or education.
    
- Appropriately cite the original trajectory data source and, once published, the related paper.
