# Week 4: HAPI FHIR REST API Operations & US Core Profiles

Hands-on RESTful API interactions executed against the public HAPI FHIR R4 server during HL7 International's **Break the Code** cohort. Demonstrates creation, retrieval, and deletion of US Core 6.1.0 compliant resources.

---

## Technical Artifacts Implemented

* **`patient-post-payload.json`**: Initial request payload for a fictional Patient adhering to the US Core 6.1.0 Patient profile.

---

## RESTful Transaction Log

| HTTP Operation | Endpoint | Payload / Parameters | Expected Status | Server Result |
| :--- | :--- | :--- | :--- | :--- |
| **`POST`** | `/Patient` | `patient-post-payload.json` | `201 Created` | `201 Created` (ID: `293525`) |
| **`GET`** | `/Patient/{id}` | `id = 293525` | `200 OK` | `200 OK` |
| **`DELETE`** | `/Patient/{id}` | `id = 293525` | `200 / 204` | `200 OK` (`OperationOutcome: Delete succeeded`) |

---

## Core Technical Concepts

* **US Core 6.1.0 Profile Compliance:** Enforces USCDI v3 element definitions including mandatory profile declarations inside `meta.profile`.
* **Server-Assigned Identifiers:** Demonstrates omitting client-side `id` values during `POST` operations to allow backend REST servers to govern primary key assignment (`293525`).
* **RESTful Lifecycle Management:** Validating end-to-end CRUD state transitions across public FHIR server endpoints.
