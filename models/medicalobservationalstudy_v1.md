# [MedicalObservationalStudy](https://schema.org/MedicalObservationalStudy)
> [!NOTE] 
> A schema.org [MedicalObservationalStudy](https://schema.org/MedicalObservationalStudy) has a study design, two or more study subjects aka "cohorts" and one or more health condition outcomes.
> With these ingredients a MedicalObservationalStudy is able to describe [Population-Level Estimation](https://ohdsi.github.io/TheBookOfOhdsi/PopulationLevelEstimation.html) much as it is represented and explained in the Book of OHDSI.

> [!CAUTION]  
> There is one caveat. The MedicalObservationalStudy lacks the granularity to describe a population-level estimation study in detail. Specifically, it doesn't capture much of the logic that goes into the construction of study subjects and their health outcomes. 

> [!TIP]  
> Instead, think of the MedicalObservationalStudy and this template as you complete it as an ***implementation guide***. It will circumscribe the (meta)data you need to perform the study. It will guide data preparation. As such, it is one of a class of tools that provides a [Bridge2AI](https://commonfund.nih.gov/bridge2ai).

> [!IMPORTANT] 
> As MedicalObservationalStudy research plans are developed and completed across the several APHRC DSWB GitHub repositories, they will be included in a catalog. The catalog will be searchable by keyword and as a knowledge graph.
## A. StudyDesign
> [!TIP]
> In schema.org a study design takes an enumeration called [MedicalObservationalStudyDesign](https://schema.org/MedicalObservationalStudyDesign). Here we are proposing a different enumeration -- one that corresponds to the [several types of population-level estimation](https://ohdsi.github.io/TheBookOfOhdsi/PopulationLevelEstimation.html) detailed in the Book of OHDSI:
> - cohort method design aka emulated clinical trial
> - self-controlled cohort design
> - case-control design
> - case-crossover design
> - self-controlled case series design
```
<

Specify here...

>
```
## B. [StudySubject](https://schema.org/studySubject)
> [!TIP] 
> In the OHDSI research paradigm in a study design that performs emulated clinical trial population-level estimation, a StudySubject maps to a target cohort and one or more comparator cohorts. So be sure to specify at least two StudySubjects. In other population-level estimation designs a StudySubject may map to control cohorts and/or a nesting cohort.
> 
> StudySubjects (aka "cohorts" in the OHDSI data analysis workbench) may consist of one or more of the following clinical and/or population health entities:
> - MedicalConditions
> - Interventions
> - MedicalRiskFactors

### 1. [MedicalCondition](https://schema.org/MedicalCondition)
> [!TIP]
> In the OMOP CDM, a schema.org MedicalCondition maps to a [condition_occurrence](https://ohdsi.github.io/CommonDataModel/cdm54.html#condition_occurrence "test"). 
```
<

Specify here...

>
```
### 2. Intervention
> [!TIP]
> In schema.org there are several types of intervention:
> - Substances
> - Public health medical guidelines
> - LifestyleModifications

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
### 3. [MedicalRiskFactor](https://schema.org/MedicalRiskFactor)
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
## C. Health Condition
> [!TIP]
> In a schema.org MedicalObservationalStudy a study subject may have one or more health condition outcomes. In the OHDSI research paradigm these health conditions correspond to outcome cohorts. In this paradigm entry events for outcome cohorts typically come from the OMOP CDM [condition_occurrence](https://ohdsi.github.io/CommonDataModel/cdm54.html#condition_occurrence) domain.
```
<

Specify here...

>
```



