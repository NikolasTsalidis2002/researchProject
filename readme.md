# Autoformalization of Sustainability Goals and Reasoning in Lean

## 📌 Overview
This project aims to **determine whether companies comply with EU sustainability directives** by formalizing sustainability requirements and company disclosures in **Lean**, a proof assistant.  

We build a pipeline that goes from **textual reports and regulations** → to **structured facts** → to **formal proofs of compliance**.  
The final output is a **compliance argument** that can show:
- ✅ Conclusive compliance  
- ⚠️ Conditional compliance (based on assumptions)  
- ❌ Non-compliance or violations  

---

## 🎯 Motivation
Current corporate sustainability reporting (e.g. under the EU’s **CSRD** and **ESRS standards**) is often complex, ambiguous, and hard to verify.  
Our approach makes compliance **transparent, verifiable, and explainable** by:
1. Extracting **facts** from company reports, news, and disclosures.  
2. Matching them to **precise EU sustainability requirements**.  
3. Building **formal Lean proofs** that show whether facts satisfy requirements.  
4. Producing a **structured compliance argument** stakeholders (auditors, regulators) can trust.

---

## 🛠 Project Workflow
1. **Requirement Extraction**  
   - Identify relevant EU sustainability requirements (e.g. ESRS E1 on climate, ESRS S1 on workforce).  
   - Formalize them into precise logical rules.  

2. **Company Statement Extraction**  
   - Extract factual claims from company reports (e.g. Novo Nordisk 2024 Annual Report).  
   - Translate them into predicate logic (e.g. `ReducedEmissions(NovoNordisk, 10%, 2023)`).  

3. **Proof of Correctness**  
   - Build **proof trees** to verify company claims.  
   - Each claim is decomposed step by step until the leaves are **axioms** (universally accepted truths, e.g. “1 liter diesel → 2.68 kg CO₂”).  
   - Example:
     ```
     Claim: "Emissions in 2023 = X tons CO₂e"
       ↳ Derived from: Σ (activity data × emission factors)
         ↳ Activity data: fuel use, electricity, mileage
         ↳ Emission factors: diesel = 2.68 kg CO₂/liter, grid = 0.112 kg CO₂/kWh
         ↳ Axioms: physical chemistry, government energy stats
     ```

4. **Lean Formalization**  
   - Encode facts and requirements in Lean.  
   - Write proofs that show whether company facts ⟹ requirements.  
   - Capture **compliance arguments** (conclusive, potential, or violations).  

---

## 📂 Pilot Tasks
- Pick one industry (pharmaceuticals, starting with Novo Nordisk).  
- Extract 3 facts and match them with ESRS requirements.  
- Formalize facts + requirements in predicate logic.  
- Write manual Lean proofs of compliance.  
- Identify challenges for automation.  

---

## 📈 Extensions (Thesis-Level Work)
- Automate fact extraction with LLMs.  
- Expand to other industries (e.g. shipping, energy, governance).  
- Handle **timed requirements** (e.g. “by 2030”, “within 1 year”).  
- Integrate argumentation frameworks (e.g. SACM, GSN, LKIF).  

---

## 📑 Example Sources
- **Company Reports**  
  - [Novo Nordisk Corporate Governance Report 2024](https://annualreport.novonordisk.com/2024/_assets/downloads/novo-nordisk-corporate-governance-report-2024.pdf)  
  - [Leo Pharma Sustainability Report 2022](https://www.leo-pharma.com/-/media/corporatecommunications/leo-pharma-com/files/annual-reports/leo-pharma-sustainability-report-2022.pdf)  
  - [Maersk Annual Report 2024](https://investor.maersk.com/static-files/31bf05a1-6f0c-4fbd-a3c7-3f58e044f668)

- **EU Regulations**  
  - [EU Regulation (EU) 2023/2772 – ESRS Set 1](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX%3A02023R2772-20231222)  
  - [EFRAG ESRS Overview](https://xbrl.efrag.org/e-esrs/esrs-set1-2023.html)  

- **Argumentation Standards**  
  - [SACM](https://www.omg.org/spec/SACM/)  
  - [GSN](https://scsc.uk/gsn)  
  - [LKIF](https://github.com/RinkeHoekstra/lkif-core)  

---

## ✅ Expected Outcome
A **proof-of-concept system** where:
- EU sustainability requirements are formalized in Lean.  
- Company disclosures (e.g. Novo Nordisk) are translated into logical facts.  
- Lean proofs determine whether disclosures satisfy EU requirements.  
- Arguments are structured and transparent down to **axioms anyone can verify**.

---
