# DFIR-Metric: A Benchmark Dataset for Evaluating Large Language Models in Digital Forensics and Incident Response


## Description

**DFIR-Metric** is a comprehensive benchmark developed to assess the performance of Large Language Models (LLMs) in the field of Digital Forensics and Incident Response (DFIR), aiming to fill the gap in standardized evaluation methods. The benchmark comprises three key components: (a) MODULE I: expert-validated knowledge-based questions , (b)  MODULE II: realistic forensic challenges that require multi-step reasoning, (c) MODULE III: practical string search tasks derived from the NIST Computer Forensics Tool Testing Program (CFTT). We evaluated state-of-the-art LLMs using the DFIR-Metric benchmark and introduced a new metric—*Task Understanding Score (TUS)*—to more effectively assess performance in complex scenarios where overall accuracy is low.

## Framework

![DFIR-Metric Framework Diagram](./assets/DFIR-Metric-Framework.png)

## Authors

Bilel Cherif, Aaesha Aldahmani, Saeed Alshehhi, Tamas Bisztray, Richard A. Dubniczky, Norbert Tihanyi

## Dataset

|Module|Dataset|Test Count|Details|
|--|--|--|--|
|`MCQ`|[DFIR-Metric-MCQ.json](/DFIR-Metric-MCQ.json)|700|Expert-reviewed 4-option quiz questions to test knowledge|
|`CTF`|[DFIR-Metric-CTF.json](/DFIR-Metric-CTF.json)|150|Realistic forensic challenges requiring multi-step reasoning in a CTF style|
|`NSS`|[DFIR-Metric-NSS.json](/DFIR-Metric-NSS.json)|500|Forensic disk analysis using NIST string search challenges|


## Module I - 700 Multiple-Choice Questions

This module contains 700 multiple-choice questions derived from industry-standard certifications and official documentation. Each question has been reviewed and validated by human experts to ensure high quality. You can download the dataset from: [DFIR-Metric-MCQ.json](/DFIR-Metric-MCQ.json)

An example question from the `DFIR-Metric-MCQ` dataset:
```python
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
Fourteen state-of-the-art LLMs have been evaluated using the DFIR-Metric MCQ dataset. The results of this evaluation are presented in the following table:

![DFIR-Metric Framework Diagram](./assets/MCQ_result.png)


## Module II - CTF Style Practical Challenges

This module includes 50 dynamic templates for CTF-style forensic challenges. Each template contains variables that can be randomized, allowing for the generation of an unlimited number of unique challenges from the base templates. For our evaluation, we used k=3, resulting in 150 practical CTF-style challenges for testing LLMs. You can download the dataset of 150 challenges here: [DFIR-Metric-CTF.json](/DFIR-Metric-CTF.json)

An example practical question from the `DFIR-Metric-CTF` dataset. Identify the suspicious IP address responsible for potentially malicious activity based on the following web server logs:

```python

10.12.19.134 - - [22/May/2025:13:00:07 +0000] "POST /api/v1/Li4vLi4vLi4vLi4vYmluL2Jhc2g= HTTP/1.1" 403 1434  
192.168.181.243 - - [22/May/2025:05:08:31 +0000] "GET /about.html HTTP/1.1" 200 1434  
192.168.209.58 - - [22/May/2025:11:14:49 +0000] "GET /index.html HTTP/1.1" 200 1434  
192.168.58.17 - - [22/May/2025:16:14:29 +0000] "GET /index.html HTTP/1.1" 200 1434  
192.168.133.223 - - [22/May/2025:03:24:11 +0000] "GET /contact.html HTTP/1.1" 200 1434  
192.168.92.89 - - [21/May/2025:21:51:37 +0000] "GET /contact.html HTTP/1.1" 200 1434  
192.168.58.169 - - [21/May/2025:20:49:46 +0000] "GET /index.html HTTP/1.1" 200 1434  
192.168.218.239 - - [22/May/2025:08:48:20 +0000] "GET /contact.html HTTP/1.1" 200 1434
192.168.205.104 - - [22/May/2025:17:10:03 +0000] "GET /download?file=....//....//etc/passwd HTTP/1.1" 403 1434  
192.168.211.175 - - [22/May/2025:04:35:56 +0000] "POST /about.html HTTP/1.1" 200 1434  
192.168.160.92 - - [21/May/2025:22:13:09 +0000] "GET /index.html HTTP/1.1" 200 1434  
192.168.198.181 - - [22/May/2025:04:06:33 +0000] "POST /contact.html HTTP/1.1" 200 1434  

answer: <xml>192.168.205.104</xml>
```

The example above represents a relatively simple task for LLMs. However, challenges such as reverse-engineering cryptographic keys or analyzing memory dumps significantly increase the complexity of the dataset compared to theoretical questions. As a result, the Confidence Index (CI) of the best-performing LLMs (without tool assistance) is substantially lower than their scores on multiple-choice questions. The results can be viewed here:

![DFIR-Metric Framework Diagram](./assets/CTF_result.png)

To generate additional challenges from the dynamic templates, we have provided a generator script in a Google Colab notebook, which can be downloaded here: [DFIR_Metric_CTF_generator.ipynb](./assets/DFIR_Metric_CTF_generator.ipynb)

).

In the Colab file, simply navigate to line 3178 and modify the following line:

## Module III 

