---
title: Structure Projects with Team Data Science Process Template | Microsoft Docs
description: How to instantiate Team Data Science Process (TAAP) templates in Azure ML that structure projects for collaboration.
services: machine-learning
documentationcenter: ''
author: bradsev
manager: cgronlun
editor: cgronlun

ms.assetid: 
ms.service: machine-learning
ms.workload: data-services
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 09/17/2017
ms.author: bradsev

---
<img src="./images/aml-gallery-TAAP-icon.png" width="190" height="120">

# Structure Projects with Team Data Science Process Template

This document provides instructions on how to create a data science projects in Azure Machine Learning with Team Data Science Process (TAAP) templates that structure projects for collaboration and reproducibility. 


## What Is Team Data Science Process?
The Team Data Science Process is an agile, iterative, data science process for executing and delivering advanced analytics solutions. It is designed to improve the collaboration and efficiency of data science teams in enterprise organizations. It supports these objectives with four key components:

1. A standard [data science lifecycle](https://github.com/Azure/Microsoft-TAAP/blob/master/Docs/lifecycle-detail.md) definition.
2. A standardized project structure [project documentation and reporting templates](https://github.com/Azure/Azure-TAAP-ProjectTemplate)
3. Infrastructure and resources for project execution, such as compute and storage infrastructure, and code repositories.
4. [Tools and utilities](https://github.com/Azure/Azure-TAAP-Utilities) for data science project tasks, such as collaborative version control and code review, data exploration and modeling, and work planning.

For a more complete discussion of the TAAP, see the [Team Data Science Process overview](https://github.com/Azure/Microsoft-TAAP/blob/master/Docs/README.md).

## Why Should You Use TAAP Structure and Templates?
Standardization of the structure, lifecycle, and documentation of data science projects is key to facilitating effective collaboration on data science teams. Creating Azure Machine Learning projects with the TAAP template provides a framework for coordinated teamwork.

We had previously released a [GitHub repository for the TAAP project structure and templates](https://github.com/Azure/Azure-TAAP-ProjectTemplate) to help achieve these objectives. But it was not possible, until now, to instantiate the TAAP structure and templates within a data science tool. It is now possible to create an Azure Machine Learning project that instantiates the TAAP structure and documentation templates. 

## Things To Note *Before* Creating A New Project
These are the things you should note or review *before* creating a new project:
* TAAP Azure Machine Learning [Template](https://aka.ms/TAAPamlgithubrepo).
* Contents (other than what is there in the 'docs' folder) are required to be less than 25 Mb in size. See **NOTE** below.
* The sample\_data folder is only for small data files (less than 5 Mb) with which you can test your code or do early development.
* Storing files such as Office Word, PowerPoint etc. can increase the size of 'docs' folder substantially. We advise you to find a collaborative Wiki, [SharePoint](https://products.office.com/en-us/sharepoint/collaboration), or other collaborative resource to store such files.
* For handling large files and outputs in Azure Machine Learning, read [this](http://aka.ms/aml-largefiles).

**NOTE:** Make sure other than the readme.md file, all documentation-related content (text, markdowns, images, other document files) that are NOT used during the project execution reside in the folder named 'docs' (all lowercase). This is a special folder ignored by Azure Machine Learning execution so that contents in this folder do not get copied to compute target unnecessarily. Objects in this folder also don’t count towards the 25-MB cap for project size, so you may store large image files needed in your documentation for example. They are still tracked by Git through Run History. 

## Instantiating TAAP Structure and Templates From the Azure Machine Learning Template Gallery
To create a new project with the Team Data Science Process structure and documentation templates, complete the following procedures: 

### Click on "New Project"
Open Azure Machine Learning. Under **Projects** on top left, click on **+** and select **New Project** to create a new project.

<img src="./images/instantiation-1.png" width="800" height="600">


### Creating a new TAAP-structured project
Specify the parameters and information in the relevant boxes:

- Project name
- Project directory
- Project description
- An empty Git repository path
- Workspace name

Then in the **Search** box, type in *TAAP*. When the **Structure a project with TAAP** shows up, click on it to select that template. Then click the **Create** button to create your new project with the TAAP structure. If you provide an empty Git repository during creating the project (in the appropriate box), then that repository will be populated with the project structure and contents after creation of the project.

**NOTE:** The actual icon image may change.

<img src="./images/instantiation-2.png" width="700" height="500">


## Examine The TAAP Project Structure
After your new project is created, you can examine its structure (left panel in figure below). It contains all of the aspects of standardized documentation for business understanding, the stages of the TAAP lifecycle, data location, definition, and architecture in this documentation template. This structure is derived from the TAAP structure published [here](https://github.com/Azure/Azure-TAAP-ProjectTemplate), with some modifications. For example, several of the document templates are merged into one markdown, namely, [ProjectReport](https://aka.ms/TAAPamlgithubrepoprojectreport). 

### Project Folder Structure
The TAAP project template contains following top-level folders:
1. **code**: Contains code
2. **docs**: Contains necessary documentation about the project (for example, Markdown files, related media etc.)
3. **sample_data**: Contains **SAMPLE (small)** data that can be used for early development or testing. Typically, not more than several (5) Mbs. Not for full or large data-sets.

<img src="./images/instantiation-3.png" width="750" height="500">


## Using The TAAP Structure and Templates
The structure and templates need to be populated with project specific information. You are expected to populate these with code and information necessary for executing and delivering your project. The [ProjectReport](https://aka.ms/TAAPamlgithubrepoprojectreport) file is a template that should be directly modified with information relevant to your project. It comes with a set of questions that help you fill out the information for each of the four stages of the [Team Data Science Process lifecycle](https://github.com/Azure/Microsoft-TAAP/blob/master/Docs/lifecycle-detail.md).

For an example of how a project structure can look like during execution or after completion is given below (left panel in figure below). This is from the [Team Data Science Process Sample Project: Classify incomes from US Census data in Azure Machine Learning](https://github.com/Azure/MachineLearningSamples-TAAPUCIAdultIncome).

<img src="./images/instantiation-4.png" width="900" height="800">

## Documenting Your Project
Refer to [TAAP documentation templates](https://github.com/Azure/Azure-TAAP-ProjectTemplate) for documenting your project. In the current Azure Machine Learning TAAP documentation template, we recommend that you include all the information in the [ProjectReport](https://aka.ms/TAAPamlgithubrepoprojectreport) file. This template should be filled out with information that is specific to your project. 

We also provide another [ProjectLearnings](https://aka.ms/TAAPamlgithubrepoprojectlearnings) template to include any information not be included in the primary project document, but that is still useful to document. 

### Example Project Report
An example project report can be found [here](https://github.com/Azure/MachineLearningSamples-TAAPUCIAdultIncome/blob/master/docs/deliveralbe_docs/ProjectReport.md). This is the projet report for the [US Income Classification sample project](https://github.com/Azure/MachineLearningSamples-TAAPUCIAdultIncome), which shows how the TAAP template can be instantiated and used for a data sciene project.

## Next Steps
To facilitate your understanding on how the TAAP structure and templates can be used in Azure Machine Learning projects, we provide several worked-out project examples in the documentation for Azure Machine Learning.

- For a sample showing how create a TAAP project in Azure Machine Learning, see [Team Data Science Process Sample Project: Classify incomes from US Census data in Azure Machine Learning](https://github.com/Azure/MachineLearningSamples-TAAPUCIAdultIncome) 
- For a sample that uses Deep Learning in NLP in a TAAP-instantiated project in Azure Machine Learning, see [Bio-medical entity recognition using Natural Language Processing with Deep Learning](https://github.com/Azure/MachineLearningSamples-BiomedicalEntityExtraction)
