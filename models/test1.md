# [MedicalObservationalStudy](https://schema.org/MedicalObservationalStudy)
> [!TIP] 
> A schema.org MedicalObservationalStudy has a study design, one or more study subjects and one or more health condition outcomes.
> A MedicalObservationalStudy conducts [Population-Level Estimation](https://ohdsi.github.io/TheBookOfOhdsi/PopulationLevelEstimation.html) in the Book of OHDSI.
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
> In the OHDSI research paradigm in a study design that performs emulated clinical trial population-level estimation, a StudySubject maps to a target cohort and one or more comparator cohorts. So be sure to specify at least two StudySubjects. In other populatiom-level estimation designs a StudySubject may map to control cohorts and/or a nesting cohort.
> 
> Target, comparator, control and nesting cohorts have OMOP CDM entry events that fall into one or more clinical domains, depending on ...

### 1. [MedicalCondition](https://schema.org/MedicalCondition)
> [!TIP]
> In the OMOP CDM, a schema.org MedicalCondition maps to a [condition_occurrence](https://ohdsi.github.io/CommonDataModel/cdm54.html#condition_occurrence "test").
```
<

Specify here...

>
```
### 2. Intervention...
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
> A MedicalGuideline schema.org type may have an authority, a legal status and one or more studies. Studies may both support and contraindicate a MedicalGuideline under various circumstances. A MedicalGuideline has a geography and a temporal coverage. In the OMOP CDM a MedicalGuideline maps to an [exposure_occurrence](https://www.ohdsi.org/wp-content/uploads/2023/10/19-zollovenecek-BriefReport.pdf). The exposure_occurrence is a new clinical table that takes concepts from a new social determinants of health vocabulary table
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
> A schema.org MedicalProcedure may be a DiagnosticProcedure, a Palliative Procedure, a PhysicalExam, a SurgicalProcedure and/or TherapeuticProcedure for MedicalTherapy or PsychologicalTreatment. In the OMOP CDM, a schema.org MedicalProcedure maps to an [procedure_occurrence](https://ohdsi.github.io/CommonDataModel/cdm54.html#procedure_occurrence) as a rule.
```
<

Specify here...

>
```
### 3. [MedicalRiskFactor](https://schema.org/MedicalRiskFactor)
> [!TIP]
> A MedicalRiskFactor may figure into target and comparator cohorts too. In schema.org a MedicalRiskFactor is anything that increases a person's likelihood of developing or contracting a disease, medical condition, or complication. These risk factors may be external or internal. External risk factors includes the physical environment (specific external exposome) and social determinants of health (general external exposome). Internal risk factors include the internal exposome (biomarkers), gene/environment interactions and the genome. Given its "richness", a MedicalRiskFactor can be mapped to one of several domains in the OMOP CDM including the [exposure_occurrence](https://www.ohdsi.org/wp-content/uploads/2023/10/19-zollovenecek-BriefReport.pdf) and the result from one or more [measurement](https://ohdsi.github.io/CommonDataModel/cdm54.html#measurement) occurrences.
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



