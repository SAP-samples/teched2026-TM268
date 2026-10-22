[Home - Workshops about the ABAP Cloud development model (ABAP Cloud)](https://github.com/SAP-samples/abap-platform-rap-workshops/blob/main/README.md)

[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/teched2026-TM268)](https://api.reuse.software/info/github.com/SAP-samples/teched2026-TM268)

# TM268 - Analyze and optimize ABAP Cloud model apps built on core data services

## Description 
This repository contains the material for the SAP TechEd 2026 session called [TM268 | Analyze and optimize ABAP Cloud model apps built on core data services](https://www.sap.com/events/teched/berlin/flow/sap/te26/catalog/page/catalog/session/1786138286996001tjEl).


- [Overview](#overview)
- [Presentation](#presentation)
- [Exercises](#-exercises)
- [Requirements](#requirements-for-attending-this-workshop)
- [How to obtain support](#how-to-obtain-support) 

## Overview
[^Top of page](#)

Performance issues can hide within data models for extensions. Analyze real-world anti-patterns in business applications built with the ABAP Cloud 💎 development model on core data services–based data models. Learn to analyze and resolve bottlenecks using **ABAP Cross Trace** and **SAP HANA SQL Analyzer** (PlanViz) in **Visual Studio Code**.

In this session, you will create and enhance a RAP application built on the **SAP Flight Reference Scenario** (`/DMO/FLIGHT`):

<kbd><img src="exercises/exercise-06/images/RAP_Carrier.png" alt="generate UI service" width="50%"></kbd>

When you double-click the row with **Airline ID = `LH`**, the left side shows the original navigation, which you can enhance to display the booking overview created in the read-only app (shown on the right side):

| Original Navigation in RAP App | Navigation enhanced by your Reporting List |
|---|---|
|<img src="exercises/exercise-06/images/RAP_Navigation_before.png" alt="generate UI service" width="100%"> | <img src="exercises/exercise-06/images/RAP_Navigation_after.png" alt="generate UI service" width="100%">|

Before that, you expose this enhancement in isolation as a read-only app not only to ensure functional correctness ([Exercise 1](exercises/exercise-01/readme.md)) but also to optimize the performance and resource utilization of this enhancement ([Exercise 2](exercises/exercise-02/readme.md) to [Exercise 5](exercises/exercise-05/readme.md)).

Finally, in [Exercise 6](exercises/exercise-06/readme.md) you extend a RAP application to consume the optimized code in the navigation.

## Presentation

* Access the presentation: 📄[TM268@SAPTechEd2026.pdf](/resources/TM268@SAPTechEd2026.pdf)

---

## 🛠 Exercises
[^Top of page](#)

| Exercise Block | -- |
| ------------- | -- |
| **Getting Started** | -- |
| [Getting Started](exercises/getting-started/readme.md) | -- |
| **Exercises for Functional Analysis** | -- |
| [Exercise 1: Functional Analysis of a Read-Only UI Service on Top of a CDS View](exercises/exercise-01/readme.md) | -- |
| **Exercises for Performance Analysis** | -- |
| [Exercise 2: Performance Analysis using the ABAP Cross Trace](exercises/exercise-02/readme.md) | -- |
| [Exercise 3: Execution Plan Analysis using SAP HANA SQL Analyzer](exercises/exercise-03/readme.md) | -- |
| [Exercise 4: Rewrite with CASE and Execution Plan Analysis using SAP HANA SQL Analyzer](exercises/exercise-04/readme.md) | -- |
| **Exercises (optional) for Performance Analysis** | -- | 
| [Exercise 5: Analyze the anti-patterns in the HEX engine](exercises/exercise-05/readme.md) | -- |
| **Exercises (optional) for Functional Enhancement of a RAP Application** | -- | 
| [Exercise 6: Consume the Read-Only UI Service in a RAP Application](exercises/exercise-06/readme.md) | -- |

In the [_Getting Started_](exercises/getting-started/readme.md) section you learn how to log on to the system and to access your package for these exercises. A brief introduction covers the CDS views used in the exercises.

In [_Exercise 1_](exercises/exercise-01/readme.md) you investigate the Read-Only service you will use throughout the exercises. In the first analysis, you will see that no data is displayed. With the tools **ABAP Cross Trace** and the **F12 Developer Tools** you examine the root cause and you will fix the functional issue. This gives you a working List Reporting app which you can later consume in a RAP application.

In [_Exercise 2_](exercises/exercise-02/readme.md) you focus on the performance. You use the **ABAP Cross Trace** and the **SAP HANA SQL Analyzer** (in **Visual Studio Code**) for analyzing the runtime and retrieve the execution plan.

In [_Exercise 3_](exercises/exercise-03/readme.md) you analyze the execution plan, learn about **anti-patterns** in CDS views with regard to SAP HANA performance. 

The focus of [_Exercise 4_](exercises/exercise-04/readme.md) is on different techniques to improve the runtime of the CDS views. In addition, you learn about further **anti-patterns**. 

While the previous exercises were using the legacy engine, in [_Exercise 5_](exercises/exercise-05/readme.md) you learn how the **HEX engine** improves the runtime.

Start with the [_Getting Started_](exercises/getting-started/readme.md) section — it is mandatory, so please work through it carefully, step by step.

> [!WARNING]
> **GitHub Navigation Limitations**
>
> Links and images may open in the same tab, and using the browser's `Back` button may not restore your previous scroll position.
>
> **Recommendation:** Keep the training instructions open in a separate tab and use `Ctrl + click` to open links in a new tab.

---

## 📋Requirements for attending this workshop
[^Top of page](#)

> To complete the practical exercises in this workshop, you need the latest version of the ABAP Development Tools for Eclipse (ADT) on your laptop or PC and access to a suitable ABAP system* and [Visual Studio Code](https://code.visualstudio.com/) and [SAP HANA SQL Analyzer for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=SAPSE.vsc-extension-sa).
> 
> The appropriate flavor of the [ABAP Flight Reference Scenario](https://github.com/SAP-samples/abap-platform-refscen-flight) must be present in the relevant system.
> 
> (*) SAP BTP ABAP environment and SAP S/4HANA Cloud Public Edition - as of release 2505 - are currently supported.
>
> #### ⚠ Exception regarding SAP-led events, such as TechEd 2026 
> → A dedicated ABAP system for the hands-on workshop participants will be provided.
> → Access to the system details for the workshop will be provided by the SAP instructors during the session.

<details>
  <summary>🔵 Requirements to follow the exercises</summary>

  The requirements to follow the exercises in this repository are:
  1. [Install the latest Eclipse platform and the latest ABAP Development Tools (ADT) plugin](https://developers.sap.com/tutorials/abap-install-adt.html)
  2. [Install the latest Visual Studio Code](https://code.visualstudio.com/)
  3. [Install the latest SAP HANA SQL Analyzer for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=SAPSE.vsc-extension-sa)
  4. [Import the ABAP Flight Reference Scenario](https://github.com/SAP-samples/abap-platform-refscen-flight) 
  5. [Create an ABAP Cloud Project in your ADT installation](https://developers.sap.com/tutorials/abap-environment-create-abap-cloud-project.html)
  6. [Adapt the Web Browser settings in your ADT installation](https://github.com/SAP-samples/abap-platform-rap-workshops/blob/main/requirements_rap_workshops.md#4-adapt-the-web-browser-settings-in-your-adt-installation) 

</details>
<br>

> [!NOTE]
> **DISCLAIMER**: Please note that information about SAP’s strategy and possible future developments is subject to change and may be changed by SAP at any time for any reason without prior notice. 

---

## Contributing
[^Top of page](#)

If you wish to contribute code, offer fixes or improvements, please send a pull request. For legal reasons, contributors will be asked to accept a DCO when they create the first pull request to this project. This happens in an automated fashion during the submission process. SAP uses [the standard DCO text of the Linux Foundation](https://developercertificate.org/).

## Code of Conduct
[^Top of page](#)

Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support 
[^Top of page](#)

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
[^Top of page](#)

Copyright (c) 2026 SAP SE or an SAP affiliate company and teched2026-TM268 contributors. All rights reserved. Please see our [LICENSE](https://github.com/SAP-samples/teched2026-TM268/blob/main/LICENSE) for copyright and license information. Detailed information including third-party components and their licensing/copyright information is available [via the REUSE tool](https://api.reuse.software/info/github.com/SAP/TM268).