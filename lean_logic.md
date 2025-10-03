# Novo Nordisk Facts vs ESRS Requirements

## Fact 1 – Net Zero Commitment
- **Report Claim**: Novo Nordisk commits to *net zero by 2045* and *33% Scope 3 reduction by 2033*.  
- **Requirement (ESRS E1 – Climate Change: Transition Plan, Targets)**:  
  Companies must disclose climate transition plans with **long-term net zero targets** and **interim Scope 3 reduction targets**.  
- **Predicate Logic**:
  - `NetZeroCommitment(NovoNordisk, 2045)`
  - `Scope3ReductionTarget(NovoNordisk, 33, 2033)`
  - `∀c. NetZeroCommitment(c, y) → y ≤ 2050`
  - `∀c. Scope3ReductionTarget(c, p, y) → (p ≥ 30 ∧ y ≤ 2035)`


## Fact 2 – Renewable Energy Use
- **Report Claim**: Novo Nordisk discloses renewable energy use, but breakdown is *partial*.  
- **Requirement (ESRS E1 – Energy Mix)**:  
  Companies must disclose **energy mix** and **share of renewables**.  
- **Predicate Logic**:
  - `UsesRenewableEnergy(NovoNordisk, 100, 2020)`
  - `∀c, y. UsesRenewableEnergy(c, p, y) → p ≥ 90`
  - *Note*: Status is ⚠️ Partial → means disclosure incomplete.


## Fact 3 – Workforce Disclosures
- **Report Claim**: Novo Nordisk discloses **diversity, pay equity, health & safety, and training** for its workforce.  
- **Requirement (ESRS S1 – Own Workforce)**:  
  Companies must disclose information on **DE&I, pay equity, health & safety, and training**.  
- **Predicate Logic**:
  - `WorkforceDisclosure(NovoNordisk, {DEI, PayEquity, Safety, Training}, 2024)`
  - `∀c, y. WorkforceDisclosure(c, items, y) → {DEI, PayEquity, Safety, Training} ⊆ items`
