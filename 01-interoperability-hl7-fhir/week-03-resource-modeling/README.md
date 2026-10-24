# Week 3: FHIR R5 Resource Structures & Clinical Vocabularies

Hands-on build artifacts developed during HL7 International's **Break the Code** cohort, demonstrating FHIR R5 schema structures, element cardinality, and reference linking.

### Artifacts Implemented
* **`patient-001.json`**: Base Patient resource adhering to FHIR R5 schemas, including official name arrays and demographic birth date elements.
* **`observation-connected.json`**: Clinical observation resource linked directly to `Patient/patient-001` via structural reference, bound to LOINC (`29463-7`) and UCUM units (`kg`).

### Key Standards Covered
* **Schema Specification:** HL7 FHIR Release 5 (R5)
* **Terminology:** LOINC for observation concepts, UCUM for quantities
* **Semantic Interoperability:** Resource-to-resource referencing via `subject.reference`
