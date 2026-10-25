# HL7 International: Break the Code

This directory documents hands-on technical competencies, data modeling artifacts, and implementation milestones completed during the **HL7 International Break the Code** cohort. The program emphasizes real-world healthcare interoperability using HL7 Fast Healthcare Interoperability Resources (FHIR Release 5).

---

## Technical Scope & Focus Areas

* **FHIR Resource Foundations:** Structuring core clinical entities (Patient, Observation, Condition, Encounter) adhering strictly to FHIR R5 schemas.
* **Semantic Interoperability & Controlled Vocabularies:** Binding standardized coding systems to clinical data elements:
  * **LOINC** for laboratory tests, clinical metrics, and diagnostic observations.
  * **SNOMED CT** for qualitative clinical findings, problems, and anatomical sites.
  * **UCUM** for automated, unified unit-of-measure serialization.
* **Resource Cardinality & Modeling Rules:** Enforcing element multiplicity (`0..1`, `1..1`, `0..*`) and managing complex reusable data structures (e.g., `HumanName`, `CodeableConcept`).
* **Relational Data Linking:** Implementing relative reference integrity across disparate resources (e.g., `Observation.subject.reference -> Patient/patient-001`).
* **API Interactions (Upcoming Weeks):** Interacting with public and sandbox FHIR servers (e.g., HAPI FHIR) using standard RESTful operations (`GET`, `POST`, `PUT`, `DELETE`).

---

## Cohort Build Progression

| Build Module | Focus Domain | Key Artifacts | Status |
| :--- | :--- | :--- | :--- |
| **Week 1–2** | Foundations & Healthcare Interoperability Landscape | Environment setup, standard organizational models | Complete |
| [**Week 3: Resource Modeling**](./week-03-resource-modeling/) | R5 Schemas, Cardinality & Terminology Mapping | `patient-001.json`, `a1c-001.json` | Complete |
| **Week 4: API Interactions** | RESTful Operations & HAPI Server Integration | Swagger/Postman payloads, API transaction logs | In Progress |
| **Week 5–11** | Advanced Workflows, Search Paradigms & Implementation | Implementation guides, bundle construction | Upcoming |

---

## Directory Architecture

```text
hl7-break-the-code/
├── README.md                      # Program overview and technical competency summary
├── week-03-resource-modeling/     # FHIR R5 Patient & Observation JSON schemas
│   ├── patient-001.json
│   ├── a1c-001.json
│   └── README.md
└── week-04-api-interactions/      # HAPI FHIR REST API execution scripts & logs
