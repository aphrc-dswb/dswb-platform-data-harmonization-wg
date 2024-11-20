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
       a. [Substance](#a-substance)  
       b. [Medical Guideline](#b-medicalguideline)  
       c. [Lifestyle Modification](#c-lifestylemodification)  
       d. [Medical Procedure](#d-medicalprocedure)  
   3.3 [Medical Risk Factor](#33-medicalriskfactor)  
4. [Health Condition](#4-health-condition)


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

* **3.1. [Medical Conditions](#31-medicalcondition)**
* **3.2. [Interventions](#32-intervention)**
* **3.3. [Medical Risk Factors](#31-medicalcondition)**

### 3.1 [MedicalCondition](https://schema.org/MedicalCondition)
> [!TIP]
> Generally speaking, your source variable is a way to measure a concept. For the sake of standardization, our schema.org MedicalCondition measures a concept in a coding system called [SNOMED-CT](https://en.wikipedia.org/wiki/SNOMED_CT). In SNOMED-CT these medical conditions can be found in one of its many (14) hierarchical lists.
>
> ![The SNOMED-CT hierarchies](https://confluence.ihtsdotools.org/download/attachments/26837115/SNOMEDOverview.png?version=4&modificationDate=1682084993000&api=v2)
> 
> [This list](https://athena.ohdsi.org/search-terms/terms?conceptClass=Disorder&conceptClass=Clinical+Finding&domain=Condition&vocabulary=SNOMED&invalidReason=Valid&page=1&pageSize=15&query=) is 100,000 concepts long and includes symptoms, signs, tests results and disorders. Identify your source variable with a concept from this list. If the concept for your source variable is not on this list, our platform is able to grow it. You can catch up with [David on Discord](https://discord.com/channels/1283751225958862859/1305477082146410558) to this end.
> 
> When it comes to the OMOP CDM and OHDSI your medical condition source variable maps to a [condition_occurrence](https://ohdsi.github.io/CommonDataModel/cdm54.html#condition_occurrence). A record in the OMOP CDM condition_occurrence table captures condition occurrence information, including the SNOMED-CT condition concept ID, the start and end date of the condition, and the source of the condition information.
```
<

Specify one or more medical condition as triple here...

(variable name, concept_id, provenance)
(variable name, concept_id, provenance)

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
> A schema.org Substance may be a drug or a dietary supplement. The concept systems we are using here to standardize substances your variables measure include [RxNorm](https://www.nlm.nih.gov/research/umls/rxnorm/overview.html) and [CVX](https://www2a.cdc.gov/vaccines/iis/iisstandards/vaccines.asp?rpt=cvx). RxNorm does NOT include dietery supplements. CVX contains vaccines. There is a gap here we hope to address with supplements.
>
> Let's think about RxNorm. RxNorm describes drugs at various levels of specificity called [TTYs](https://www.nlm.nih.gov/research/umls/rxnorm/docs/appendix5.html). In TTYs RxNorm achieves specificity by constructing concepts that combine a drug's ingredient(s) with one or more other characteristics. The TTY we are standardizing on are concepts that combine ingredients with the drug's dose form group. This combination is called SCDG (Semantic Clinical Drug Group). It has [a list](https://athena.ohdsi.org/search-terms/terms?conceptClass=Clinical+Dose+Group&conceptClass=CVX&conceptClass=Vaccine+Group&vocabulary=RxNorm&vocabulary=CVX&page=1&pageSize=30&query=) that is 18,000 concepts long. SCDG was chosen for standardization in part because it disregards brand which gives these concepts an international flavor. If the concept for your source variable is not on this list, our platform is able to grow it. You can catch up with [David on Discord](https://discord.com/channels/1283751225958862859/1305477082146410558) to this end.
> 
> In the OMOP CDM, a schema.org Substance maps to a [drug_exposure](https://ohdsi.github.io/CommonDataModel/cdm54.html#drug_exposure). A record in the drug_exposure table includes the drug concept ID, the start and end date of the exposure, and the quantity of the drug (which need not be specified).
```
<

Specify one or more Substance as triple here...

(variable name, concept_id, provenance )
(variable name, concept_id, provenance)

>
```
#### b. [MedicalGuideline](https://schema.org/MedicalGuideline)
> [!TIP]
> A MedicalGuideline schema.org type may have an authority, a legal status and one or more studies. Studies may both support and contraindicate a MedicalGuideline under various circumstances. A MedicalGuideline has a geography and a temporal coverage. In the OMOP CDM a MedicalGuideline maps to an [exposure_occurrence](https://www.ohdsi.org/wp-content/uploads/2023/10/19-zollovenecek-BriefReport.pdf) aka **external_exposure**. The external_exposure is a new clinical table that takes concepts from one of two new OHDSI vocabularies that together cover the **external exposome**.
>
> ![The Exposome](https://ars.els-cdn.com/content/image/1-s2.0-S0098299721000467-gr1_lrg.jpg)
>
> A link to a MedicalGuideline list across these two vocabularies is forthcoming. If the concept for your source variable is not on this list, our platform is able to grow it. You can catch up with [David on Discord](https://discord.com/channels/1283751225958862859/1305477082146410558) to this end.
```
<

Specify one of more MedicalGuideline as triple here...

(variable name, concept_id, provenance)
(variable name, concept_id, provenance)

>
```
#### c. [LifeStyleModification](https://schema.org/LifestyleModification)
> [!TIP]
> A schema.org LifeStyleModification may be a diet and/or a physical activity regimen. Concepts for these things can be found in one of the two new OHDSI exposome vocabularies. See above. A link to a list of LifeStyleModification concepts across these two vocabularies in forthcoming. If the concept for your source variable is not on this list, our platform is able to grow it. You can catch up with [David on Discord](https://discord.com/channels/1283751225958862859/1305477082146410558) to this end.
>
> In the OMOP CDM, a schema.org LifeStyleModification maps to an [observation](https://ohdsi.github.io/CommonDataModel/cdm54.html#observation "Lifestyle modifications refer to non-pharmaceutical interventions aimed at improving health outcomes, such as changes in diet, exercise, or smoking cessation").
```
<

Specify one or more LifeStyleModification as triple here...

(variable name, concept_id, provenance)
(variable name, concept_id, provenance)

>
```
#### d. [MedicalProcedure](https://schema.org/MedicalProcedure)
> [!TIP]
> A schema.org MedicalProcedure may be a DiagnosticProcedure, a Palliative Procedure, a PhysicalExam, a SurgicalProcedure and/or TherapeuticProcedure for MedicalTherapy or PsychologicalTreatment. The concept system we are using here to standardize procedures your variables measure is [SNOMED-CT](https://en.wikipedia.org/wiki/SNOMED_CT). In SNOMED-CT these medical procedures can be found in one of its many (14) hierarchical lists.
>
> ![The SNOMED-CT hierarchies](https://confluence.ihtsdotools.org/download/attachments/26837115/SNOMEDOverview.png?version=4&modificationDate=1682084993000&api=v2)
> 
> [This list](https://athena.ohdsi.org/search-terms/terms?conceptClass=Procedure&domain=Procedure&invalidReason=Valid&vocabulary=SNOMED&page=3249&pageSize=15&query=) is 48,000 concepts long.
>
>
> In the OMOP CDM, a schema.org MedicalProcedure maps to a [procedure_occurrence](https://ohdsi.github.io/CommonDataModel/cdm54.html#procedure_occurrence "A medical procedure in OMOP CDM refers to a clinical activity performed for diagnostic or therapeutic purposes. The procedure_occurrence table records data about these procedures") as a rule.
```
<

Specify one or more MedicalProcedure as triple here...

(variable name, concept_id, provenance)
(variable name, concept_id, provenance)

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

Specify one or more Medical Risk Factor as  triple here...

(variable name, concept_id, provenance)
(variable name, concept_id, provenance)

>
```
## 4. Health Condition
> [!TIP]
> In a schema.org MedicalObservationalStudy a study subject may have one or more health  condition outcomes. These outcomes include "diseases, injuries, disabilities, disorders and syndromes". Outcomes are, as a rule, more specific than the medical condition(s) that lead to an intervention. Those conditions -- in addition to "diseases, injuries, disabilities, disorders, syndromes" -- include signs, symptoms and test results. In SNOMED-CT medical conditions are more general and outcomes are more specific. [The list of outcomes](https://athena.ohdsi.org/search-terms/terms?conceptClass=Disorder&conceptClass=Clinical+Finding&domain=Condition&vocabulary=SNOMED&invalidReason=Valid&page=1&pageSize=15&query=) in SNOMED-CT is 88,000 concepts long. If the concept for your source variable is not on this list, our platform is able to grow it. You can catch up with [David on Discord](https://discord.com/channels/1283751225958862859/1305477082146410558) to this end.
>
> In the OHDSI research paradigm these health conditions correspond to outcome cohorts. In this paradigm entry events for outcome cohorts typically come from the OMOP CDM [condition_occurrence](https://ohdsi.github.io/CommonDataModel/cdm54.html#condition_occurrence) domain.
```
<

Specify one or more health condition outcomes as triple here...

(variable name, concept_id, provenance)
(variable name, concept_id, provenance)

>
```
