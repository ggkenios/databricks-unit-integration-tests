# Databricks Tests
| | |
| --- | --- |
| Tests | [![CI - Test](https://github.com/ggkenios/databricks-champion/actions/workflows/cicd.yml/badge.svg)](https://github.com/ggkenios/databricks-champion/actions/workflows/cicd.yml) |
<br>

## Table of Contents
- [What it does](#what-it-does)
- [Requirements](#requirements)
- [Inspired By](#inspired-by)
<br>

## What it does
A simple implementation of a CI/CD pipeline for Databricks using **`GitHub Actions`** & **`Databricks Workflows`**. <br>
The pipeline is triggered when a new commit is pushed to selected branches. <br>
<br>
The pipeline consists of the following steps:
* **Push** <br>
    Pushes the code to the Databricks workspace and runs 
    - **`Unit Test`** on databricks worflows 
    - **`Integration Test`** on databricks worflows or DLT

* **Release** <br>
    If the tests pass on the staging environment, the code is released to the production environment.
<br>

## Requirements
* **`Databricks workspace`**
* **`GitHub variables & secrets`** for:
    * DATABRICKS_HOST <br>
      Variable: The url of the databricks workspace
    * DATBRICKS_TOKEN <br>
      Secret: The access token of a user with admin rights
<br>

## Inspired By
https://github.com/alexott/databricks-nutter-repos-demo
