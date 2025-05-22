# DFIR-Metric: A Benchmark Dataset for Evaluating Large Language Models in Digital Forensics and Incident Response

DFIR-Metric is a comprehensive benchmark designed to evaluate Large Language Models (LLMs) in Digital Forensics and Incident Response (DFIR), addressing the current lack of standardized evaluation. The benchmark includes three components: expert-reviewed knowledge questions, NIST-aligned practical tasks, and realistic forensic challenges requiring multi-step reasoning. We assess 20 LLMs using DFIR-Metric and propose a new metric, the Task Understanding Score (TUS), to better evaluate performance in complex, low-accuracy scenarios.

## Dataset

|Module|Dataset|Test Count|Details|
|--|--|--|--|
|`MCQ`|[DFIR-Metric-MCQ.json](/DFIR-Metric-MCQ.json)|713|Expert-reviewed 4-option quiz questions to test knowledge|
|`CTF`|[DFIR-Metric-CTF.json](/DFIR-Metric-CTF.json)|150|Realistic forensic challenges requiring multi-step reasoning in a CTF style|
|`NSS`|[DFIR-Metric-NSS.json](/DFIR-Metric-NSS.json)|510|Forensic disk analysis using NIST string search challenges|
