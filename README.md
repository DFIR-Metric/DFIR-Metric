# DFIR-Metric: A Benchmark Dataset for Evaluating Large Language Models in Digital Forensics and Incident Response

DFIR-Metric is a comprehensive benchmark designed to evaluate Large Language Models (LLMs) in Digital Forensics and Incident Response (DFIR), addressing the current lack of standardized evaluation. The benchmark includes three components: expert-reviewed knowledge questions, NIST-aligned practical tasks, and realistic forensic challenges requiring multi-step reasoning. We assess 20 LLMs using DFIR-Metric and propose a new metric, the Task Understanding Score (TUS), to better evaluate performance in complex, low-accuracy scenarios.

Authors: _Bilel Cherif, Aaesha Aldahmani, Saeed Alshehhi, Tamas Bisztray, Richard A. Dubniczky, Norbert Tihanyi_

## Dataset

|Module|Dataset|Test Count|Details|
|--|--|--|--|
|`MCQ`|[DFIR-Metric-MCQ.json](/DFIR-Metric-MCQ.json)|700|Expert-reviewed 4-option quiz questions to test knowledge|
|`CTF`|[DFIR-Metric-CTF.json](/DFIR-Metric-CTF.json)|150|Realistic forensic challenges requiring multi-step reasoning in a CTF style|
|`NSS`|[DFIR-Metric-NSS.json](/DFIR-Metric-NSS.json)|500|Forensic disk analysis using NIST string search challenges|

## Framework

![DFIR-Metric Framework Diagram](./assets/DFIR-Metric-Framework.png)

## Module I - 700 Multiple-Choice Questions

This module contains 700 multiple-choice questions derived from industry-standard certifications and official documentation. Each question has been reviewed and validated by human experts to ensure high quality. You can download the dataset from: [DFIR-Metric-MCQ.json](/DFIR-Metric-MCQ.json)

An example question from the dataset:
```json
{
  "question": "Which code does the FAT file system use to mark the file as deleted?",
  "options": {
    "A": "ESh",
    "B": "h5E",
    "C": "E5h",
    "D": "5Eh"
  },
  "answer": "C"
}
```









## Module II 


## Module III 

