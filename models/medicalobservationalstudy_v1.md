# [MedicalObservationalStudy](https://schema.org/MedicalObservationalStudy)
> [!NOTE] 
> A schema.org [MedicalObservationalStudy](https://schema.org/MedicalObservationalStudy) has a study design, two or more study subjects aka "cohorts" and one or more health condition outcomes.
> With these ingredients a MedicalObservationalStudy is able to describe [Population-Level Estimation](https://ohdsi.github.io/TheBookOfOhdsi/PopulationLevelEstimation.html) much as it is represented and explained in the Book of OHDSI.

---
## Purpose and Objectives

The primary objective of this template is to guide users in documenting Medical Observational Studies consistently across DSWB pathfinders. By standardizing metadata and study elements, this template ensures that:

> 1. **Study Documentation**: Critical study components are clearly defined, making studies easily understood and replicable.
> 2. **FAIR Principles**: Documentation aligns with the FAIR (Findable, Accessible, Interoperable, and Reusable) principles to support data sharing and reusability.
> 3. **Cataloging and Discoverability**: Completed study documentation will be included in a searchable catalog, enhancing the discoverability of studies by keywords and facilitating a knowledge graph structure for interconnected research data.

---

> [!CAUTION]  
> There is one caveat. The MedicalObservationalStudy lacks the granularity to describe a population-level estimation study in detail. Specifically, it doesn't capture much of the logic that goes into the construction of study subjects and their health outcomes. 

> [!TIP]  
> Instead, think of the MedicalObservationalStudy and this template as you complete it as an ***implementation guide***. It will circumscribe the (meta)data you need to perform the study. It will guide data preparation. As such, it is one of a class of tools that provides a [Bridge2AI](https://commonfund.nih.gov/bridge2ai).

> [!IMPORTANT] 
> As MedicalObservationalStudy research plans are developed and completed across the several APHRC DSWB GitHub repositories, they will be included in a catalog. The catalog will be searchable by keyword and as a knowledge graph.

---


## Table of Contents
1. [General Properties](#1-general-properties)  
   1.1 [Research Questions](#11-research-questions)  
   1.2 [Study Location](#12-studylocation)  
   1.3 [Funding](#12-studylocation)  
   1.4 [Status](#14-status)  
   1.5 [Outcomes of Interest](#15--outcomes-of-interest)  
2. [Study Design](#2-studydesign)  
3. [Study Subject](#3-studysubject)  
   3.1 [Medical Condition](#31-medicalcondition)  
   3.2 [Intervention](#32-intervention)  
       a. [Substance](#substance)  
       b. [Medical Guideline](#medical-guideline)  
       c. [Lifestyle Modification](#lifestyle-modification)  
       d. [Medical Procedure](#medical-procedure)  
   3.3 [Medical Risk Factor](#medical-risk-factor)  
4. [Health Condition](#health-condition)


---
## 1. General Properties
> [!NOTE] 
> The **General Properties** section includes foundational attributes that apply across the entire study. These properties set the context and goals of the study, allowing readers to understand the study's scope and purpose before exploring specific study elements.

---

### 1.1 Research Questions
> [!NOTE]  
> List the primary research question(s) guiding the study. These questions frame the study’s objectives, influence study design choices, and clarify the outcomes of interest.


```
<

Specify here...

>
```
#### 1.2 [StudyLocation](https://schema.org/studyLocation)
> [!TIP]  
> Study location refers to the geographical area where the research is being conducted. This is important for understanding the context of the study, particularly in population health studies where location may influence outcomes.

```
<

Specify here...

>
```
#### 1.3 [Funding](https://schema.org/sponsor)
> [!TIP]  
> A Grant that directly or indirectly provide funding or sponsorship for this item. See also ownershipFundingInfo.

```
<

Specify here...

>
```
#### 1.4 [Status](https://schema.org/status)
> [!TIP]  
> The status of the study provides important context regarding its current state, such as whether it is in progress, completed, or suspended. This property is critical for tracking the timeline and overall progress of the study.
```
<

Specify here...

>
```
#### 1.5  Outcomes of Interest
> [!TIP]  
> Define the primary and secondary outcomes that the study seeks to evaluate. These outcomes align with the research questions and help to guide data analysis.

```
<

Specify here...

>

```
## 2. StudyDesign
> [!TIP]
> In schema.org a study design takes an enumeration called [MedicalObservationalStudyDesign](https://schema.org/MedicalObservationalStudyDesign). Here we are proposing a different enumeration -- one that corresponds to the [several types of population-level estimation](https://ohdsi.github.io/TheBookOfOhdsi/PopulationLevelEstimation.html) detailed in the Book of OHDSI:

> - **Cohort Method Design** *(emulated clinical trial)*: Compares exposure-based cohorts to estimate specific outcomes.
> - **Self-Controlled Cohort Design**: Compares timepoints within the same cohort to assess exposure-related risks.
> - **Case-Control Design**: Contrasts cases (with outcome) and controls (without outcome).
> - **Case-Crossover Design**: Assesses exposure risk by comparing periods within subjects.
> - **Self-Controlled Case Series Design**: Evaluates risks by comparing individual time periods.
```
<

Specify here...

>
```
## 3. [StudySubject](https://schema.org/studySubject)
> [!TIP] 
> In the OHDSI research paradigm in a study design that performs emulated clinical trial population-level estimation, a StudySubject maps to a target cohort and one or more comparator cohorts. So be sure to specify at least two StudySubjects. In other population-level estimation designs a StudySubject may map to control cohorts and/or a nesting cohort.
> 
> StudySubjects (aka "cohorts" in the OHDSI data analysis workbench) may consist of one or more of the following clinical and/or population health entities:

* **3.1. [Medical Conditions](#1-medicalcondition)**
* **3.2. [Interventions](#2-intervention)**
* **3.3. [Medical Risk Factors](#3-medicalriskfactor)**

### 3.1 [MedicalCondition](https://schema.org/MedicalCondition)
> [!TIP]
> In the OMOP CDM, a schema.org MedicalCondition maps to a [condition_occurrence](https://ohdsi.github.io/CommonDataModel/cdm54.html#condition_occurrence "test"). 
```
<

Specify here...

>
```
### 3.2 Intervention
> [!TIP]
> In schema.org there are several types of intervention:
* [a. Substances](#a-substance)
* [b. Public Health Medical Guidelines](#b-medicalguideline)
* [c. Lifestyle Modifications](#c-lifestylemodification)
* [d. Medical Procedures](#d-medicalprocedure)

#### a. [Substance](https://schema.org/Substance)
> [!TIP]
> A schema.org Substance may be a drug and/or a dietary supplement. In the OMOP CDM, a schema.org Substance maps to a [drug_exposure](https://ohdsi.github.io/CommonDataModel/cdm54.html#drug_exposure).
```
<

Specify here...

>
```
#### b. [MedicalGuideline](https://schema.org/MedicalGuideline)
> [!TIP]
> A MedicalGuideline schema.org type may have an authority, a legal status and one or more studies. Studies may both support and contraindicate a MedicalGuideline under various circumstances. A MedicalGuideline has a geography and a temporal coverage. In the OMOP CDM a MedicalGuideline maps to an [exposure_occurrence](https://www.ohdsi.org/wp-content/uploads/2023/10/19-zollovenecek-BriefReport.pdf) aka **external_exposure**. The external_exposure is a new clinical table that takes concepts from a new social determinants of health vocabulary table.
```
<

Specify here...

>
```
#### c. [LifeStyleModification](https://schema.org/LifestyleModification)
> [!TIP]
> A schema.org LifeStyleModification may be a diet and/or a physical activity regimen. In the OMOP CDM, a schema.org LifeStyleModification maps to an [observation](https://ohdsi.github.io/CommonDataModel/cdm54.html#observation).
```
<

Specify here...

>
```
#### d. [MedicalProcedure](https://schema.org/MedicalProcedure)
> [!TIP]
> A schema.org MedicalProcedure may be a DiagnosticProcedure, a Palliative Procedure, a PhysicalExam, a SurgicalProcedure and/or TherapeuticProcedure for MedicalTherapy or PsychologicalTreatment. In the OMOP CDM, a schema.org MedicalProcedure maps to a [procedure_occurrence](https://ohdsi.github.io/CommonDataModel/cdm54.html#procedure_occurrence) as a rule.
```
<

Specify here...

>
```
### 3.3 [MedicalRiskFactor](https://schema.org/MedicalRiskFactor)
> [!TIP]
> A MedicalRiskFactor may figure into study subjects too. In schema.org a MedicalRiskFactor is "anything that increases a person's likelihood of developing or contracting a disease, medical condition, or complication". These risk factors may be external or internal. External risk factors includes the physical environment (sometimes called the "specific external exposome") and social determinants of health (sometimes called the "general external exposome"). Internal risk factors include the internal exposome, gene/environment interactions and the genome.
>
> ![The Exposome](https://ars.els-cdn.com/content/image/1-s2.0-S0098299721000467-gr1_lrg.jpg)
>
>  Given its "richness", a MedicalRiskFactor can be mapped to one of several domains in the OMOP CDM including the [exposure_occurrence](https://www.ohdsi.org/wp-content/uploads/2023/10/19-zollovenecek-BriefReport.pdf) aka **external_exposure** and the result from one or more [measurement](https://ohdsi.github.io/CommonDataModel/cdm54.html#measurement) occurrences. Measurements provide a window into the so-called "internal exposome".
```
<

Specify here...

>
```
## 4. Health Condition
> [!TIP]
> In a schema.org MedicalObservationalStudy a study subject may have one or more health condition outcomes. In the OHDSI research paradigm these health conditions correspond to outcome cohorts. In this paradigm entry events for outcome cohorts typically come from the OMOP CDM [condition_occurrence](https://ohdsi.github.io/CommonDataModel/cdm54.html#condition_occurrence) domain.
```
<

Specify here...

>
```

