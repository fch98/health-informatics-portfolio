# Week 3: FHIR R5 Resource Structures & Clinical Vocabularies

Hands-on build artifacts developed during HL7 International's **Break the Code** cohort, demonstrating FHIR R5 schema structures, element cardinality, structural referencing, and standard terminology bindings.

---

## Artifacts Implemented

* **`patient-001.json`**: Base `Patient` resource adhering to FHIR R5 schemas, implementing official name array structures (`HumanName`) and demographic birth date primitives.
* **`observation-connected.json`**: Clinical `Observation` resource linked directly to `Patient/patient-001` via a structural reference (`subject.reference`), capturing vital sign metrics.

---

## Core Technical Concepts & Standards

### 1. Resource Modeling & Structural Cardinality
* **Atomic Units of Exchange:** Resources serve as the discrete building blocks of FHIR, encapsulating distinct clinical concepts.
* **Cardinality Constraints:** 
  * `Patient.name` (`0..*`): A patient may have zero, one, or multiple names (legal, maiden, nickname).
  * `Patient.birthDate` (`0..1`): A patient can only have at most one birth date.
  * `Observation.status` (`1..1`): Mandatory status code (e.g., `final`) required for valid clinical processing.

### 2. Semantic Interoperability & Dual-Vocabulary Architecture
* **LOINC (`http://loinc.org`):** Applied to define the clinical measurement or test question (`29463-7` for *Body Weight*).
* **SNOMED CT (`http://snomed.info/sct`):** Utilized for clinical findings, body sites, and qualitative observation values.
* **UCUM (`http://unitsofmeasure.org`):** Standardized unit serialization (`kg`) inside `valueQuantity` to ensure automated computational comparability across clinical systems.

### 3. Resource-to-Resource Referencing
* Connected via `subject: { "reference": "Patient/patient-001" }`, preserving relational integrity across distributed healthcare endpoints without duplicating demographic payloads.
