# CareSync ProActive - Patient IoT Discrepancy Analyzer Agent

> **Deliver smarter, real-time care coordination by comparing live IoT data against patient care plans.**

---

## 🩺 Project Overview

CareSync ProActive empowers healthcare teams to detect care plan deviations early and proactively intervene.  
This intelligent agent analyzes incoming IoT device data (e.g., blood pressure monitors, glucose sensors, dialysis machines) and compares it against prescribed patient Care Plan targets.

If discrepancies are found (e.g., a patient’s blood pressure remains elevated despite Care Plan goals), the agent automatically identifies the issue, generates a structured alert, and prioritizes patients needing attention.

This enables proactive interventions, reduces hospital readmission rates, and ultimately helps improve patient outcomes while increasing healthcare revenue.

---

## 📋 Key Functionalities

- **Fetch Patient Information**  
  Retrieves patient profiles from input data Data Cloud using retriever

- **Analyze Care Plans vs IoT Readings**  
  Thoroughly reviews care targets like blood pressure, glucose levels, dialysis compliance, etc., and compares them against daily IoT updates.

- **Detect Discrepancies**  
  Flags patients where actual readings **do not meet** the goals set in the Care Plan.

- **Smart Filtering**  
  Ignores patients who are fully compliant to reduce noise and focus on at-risk individuals.

- **Generate Actionable Summaries**  
  Outputs:
  - Patient ID
  - Brief Patient Summary
  - Specific discrepancy found
  - Analysis of why the Care Plan target was missed

---

## 🛠️ How It Works

1. **Input Sources**
   - Information is either input through the agent or through person account record page and it captures either a specific patient id or about all the patients in the org
   - If Person Account record page deatail page is visited it automatically supplied the patient id to the prompt

2. **Processing Logic**
   - Match patient IDs to their Care Plans and corresponding IoT streams.
   - Compare each Care Plan target with live device readings.
   - Filter out patients meeting all targets.
   - Summarize discrepancies for patients requiring attention.

3. **Output Format**
   - Clean structured response with critical fields.
   - Ready for use inside Salesforce Health Cloud, Slack notifications, or patient management dashboards.

---

## 📦 Repository Contents

| Folder/File | Description |
|:---|:---|
| `force-app/` | Salesforce DX source code (Apex classes, Flows, LWC, Data Cloud config) |
| `Presentation/` | The presentation deck

---

## 🔒 Security and Compliance

- All patient data handled within Salesforce HIPAA-compliant infrastructure.
- Slack and SMS communications routed via secure, auditable channels.
- Data anonymization options available for testing and staging environments.

---

## 📣 Project Sponsored by:
CareSync Labs – Empowering connected healthcare.


