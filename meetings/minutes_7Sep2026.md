# Coastal Ocean coordination meeting minutes

8th September 2026

Participants: Ana Aguiar, Matt Martin, Jeff Polton, Richard Renshaw, Kit Stokes, Segolene Berthou, Oliver Lambert-Brown, Jonathan Tinker (first 20 min), James While (first 30 min)

Apologies: Susan Kay, Andy Saulter.

----
## Agenda

- Review actions from previous meeting 8th of Jun: we missed this at the meeting but the table of Actions will be updated.
- Update on PS48 (CO9p2) trials/issues (Jon Tinker, James While)
- AOB


## Copilot generated notes

### 1. Bottom Stress Diagnostics for Sediment Applications

A requirement was raised for bottom stress diagnostics at a fixed height above the seabed to support sediment transport and suspended particulate matter studies. See https://github.com/JMMP-Group/CO_coordination/issues/25

Current NEMO outputs provide bottom stress associated with the model's lowest layer, which varies in thickness spatially. This makes direct application to sediment transport studies challenging.

Discussion focused on:

- The scientific need for diagnostics at fixed heights (e.g. 5–10 m above bed).
- Difficulties in deriving these quantities offline.
- Potential future NEMO developments to provide such diagnostics directly.
- Possible value for future ecosystem and coastal applications.

No immediate implementation was agreed, but the requirement was recognised as scientifically important.

---

### 2. Evaluation and Validation Activities

Ongoing evaluation work associated with current developments includes:

- Operational performance statistics.
- Sea surface temperature validation.
- Current velocity validation.
- HF radar comparisons.
- Forecast skill assessments.
- Class-4 style verification metrics.

The objective is to provide robust evidence supporting future operational deployment.

---

### 3. Sea-Level Assimilation Investigation

A significant effort had been devoted to investigating an apparent issue with sea-level data assimilation.

The investigation concluded that:

- The perceived problem was primarily related to plotting and file-selection issues.
- No fundamental fault was identified in the assimilation system.
- The work nevertheless highlighted useful differences in boundary-condition handling between operational and development systems.

The issue is therefore considered resolved, while lessons learned from the investigation will be retained.

---

### 4. Wave Coupling and Boundary Conditions

Participants reviewed concerns regarding whether ocean-wave coupling was functioning correctly.

Following detailed investigation, it was concluded that:

- Model coupling had been operating correctly.
- Confusion arose from diagnostics, file outputs and metadata interpretation.
- Some coupling controls were no longer exposed in executables while remaining active within the model system.
- Existing metadata could be improved to make coupled configurations easier to identify.

The group agreed that better diagnostics and documentation would reduce the likelihood of similar confusion in future.

---

## Operational Update: PS48 / AMM15

### Current Status

Progress towards PS48 delivery continues, including:

- Trial reruns where required.
- Present-day spin-up activities.
- Preparation of handover materials.

The project remains on a challenging but achievable schedule. The QUID for Copernicus is due in November.

### Planned Handover

Initial delivery will provide:

- Operational model configuration.
- Restart capability.
- Seven-day forecasting.

A subsequent update will extend forecasting capability to ten days once supporting infrastructure becomes available.

### Major Scientific and Technical Changes

Key developments include:

- CO9.2 scientific updates.
- Revised sea-level configuration.
- Wetting and drying capability.
- New wave grids.
- Forecast extension from 7 to 10 days.
- Baltic boundary-condition changes.
- Updated atmospheric forcing strategy using MOGREPS control forecasts.

Overall confidence in AMM15 performance was reported as positive.

---

## Future Regional Modelling Strategy

Discussion focused on emerging requirements for future regional ocean modelling systems.

Questions under consideration include:

- Appropriate future model resolution.
- Potential domain expansion.
- Long-term role of AMM15.
- Requirements for higher-resolution coastal modelling.
- Integration of future regional systems into wider operational services.

A dedicated workshop is planned to gather modelling requirements and guide future priorities.

---

## AGRIF and Nested Modelling

AGRIF nesting was discussed as a potentially important strategic capability.

Potential applications include:

- High-resolution coastal domains.
- Baltic Sea extensions.
- Fjords and estuarine environments.
- Future Copernicus and national modelling services.

### Potential Benefits

- Higher resolution in targeted regions.
- Improved representation of coastal processes.
- Reduced computational cost relative to global refinement.
- Greater flexibility for future model evolution.

### Key Challenges

- Data assimilation integration.
- Coupling complexity.
- Boundary-condition treatment.
- Tidal representation.
- Operational resource requirements.

The group agreed that AGRIF remains a promising area for further investigation.

---

## NEMO 5 Development Update

Progress on NEMO 5 testing was reported.

Highlights include:

- Successful AMM15 test configurations.
- Stable operation with longer model timesteps.
- No major validation concerns identified so far.
- Preparation for migration to new development infrastructure.

Current activity focuses primarily on platform and infrastructure changes rather than major scientific modifications.

---

## Ensemble Development

Progress was reported on the development of regional ocean ensembles.

Current activities include:

- AMM7 ensemble development.
- AMM15 ensemble development.
- Ensemble boundary-condition forcing.
- Observation perturbation approaches.
- Stochastic physics experimentation.

The long-term objective is to strengthen uncertainty estimation and support future data assimilation methods.

---

## Future Funding Opportunities

Discussion highlighted emerging national capability funding opportunities.

Potential areas of interest include:

- AGRIF development.
- Regional modelling advances.
- High-resolution coastal prediction.
- Future operational ocean forecasting capabilities.

Further discussions will continue outside the coordination meeting and may feed into future programme proposals.

---

# Follow-Up Actions

| Actions from 6th of Jun 2026 | Owner |
|----------|--------|
| Obtain clarification from Andy Clark on whether licensing and attribution for new ancillary files should be included as metadata or separate files, and communicate the outcome. - _Andy C will review this late Sep 2026._ | Ana |
| Follow up with Ben Fitzpatrick regarding software licensing for shared workflows and update the group when guidance is available. - _Waiting for a decision._ | Ana |
| Finalise and communicate the chosen name for the extended AMM7 configuration (**EAMM7**), ensuring consistency across files and documentation. | Richard Renshaw |
| Complete and submit the final project proposal and business case for the Environment Agency water-level forecasting improvements, including contract management and costing details. | Kit |
| Review whether satellite observations (e.g. SWOT, Sentinel-3) should be reintroduced into the long-term plans for the Environment Agency project and considered for Phase 2 developments. | Kit |

## Medium Priority

- Explore approaches for fixed-height bottom stress diagnostics.
- Continue NEMO 5 testing and documentation.
- Advance ensemble development activities.

## Strategic Actions

- Develop future regional ocean-modelling requirements.
- Explore opportunities for future funding proposals.
