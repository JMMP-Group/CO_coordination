# Coastal Ocean coordination meeting minutes

8th June 2026

Participants: Ana Aguiar, Matt Martin, Jeff Polton, Richard Renshaw, Kit Stokes, Segolene Berthou, Oliver Lambert-Brown

Apologies: Susan Kay, Jonathan Tinker.

----
## Agenda

- Review actions from previous meeting 9th of Mar: there's only 1 action
- Update on PS48 (CO9p2) trials/issues (Jon Tinker) [10 min]
- Update on work for UKCI (Richard Renshaw) [10 min]
- NEMO-surge: R&D for EA coastal flood forecast improvements programme (Kit Stokes) [10 min]
- AOB


## Copilot generated notes

## 1. Ancillary Files Management and Licensing

Oliver Lambert-Brown, with input from Ryan Patmore and Andy Clark, provided updates on the status of ancillary files, including pending vendor confirmations, the transition of file management to Andy Clark's team, and ongoing clarifications regarding licensing and attribution requirements. Ben Fitzpatrick has been consulted for software licensing guidance.

### Status of Ancillary Files
- Most ancillary files are ready.
- Confirmation has been received for most files, except one related to the Baltic, for which a vendor response is still pending.
- Ryan Patmore (NOC) assisted in obtaining these confirmations.

### Transition of File Management
- Andy Clark's team will eventually take over management of all ancillary files, including ocean files.
- The transition point is tied to clarification around "Momentum" or NGMS.
- The group is awaiting Andy Clark's input on what constitutes NGMS, particularly as the ocean component is currently frozen.

### Licensing and Attribution Clarifications
- Clarification is needed on how licensing and attribution should be handled for ancillary files.
- Older files may require separate licensing files.
- New files should ideally include licensing information as metadata.
- Oliver Lambert-Brown has not yet produced licenses pending further clarification from Andy Clark.

### Software Licensing for Workflows
- Licensing requirements for shared workflows were discussed.
- Ben Fitzpatrick is investigating whether a Momentum licence can be used for certain workflows.
- The group is awaiting his response.
- It was clarified that only research workflows are shared externally, under specific agreements.

---

## 2. UK Climate Information (UKCI) Regional Ocean Configuration Development

Richard Renshaw presented the UKCI project's regional ocean configuration plans, including development of an extended AMM7 domain in collaboration with NOC, project timelines, and discussions on naming the new configuration.

### Project Scope and Timeline
- UKCI will provide historical data and projections under SSP245 and SSP370 emission scenarios.
- The project focuses on regional ocean modelling.
- Data delivery for CCI5 is targeted for 2028.
- Production is planned to begin in November and complete by March.

### Extended AMM7 Domain Development
- NOC and Anthony's team are developing an extended AMM7 domain.
- The domain will fully encompass the AMM15 region.
- Boundary adjustments are being made to improve buffer zones and boundary conditions, particularly in the Baltic.
- Initial unforced experiments have been successful.
- Realistic simulations with atmospheric forcing are planned.

### Naming the New Configuration
Several naming options were discussed:

- EAMM7
- NIEM7
- AMM7E

The group generally favoured **EAMM7** because it preserves lineage and clarity, although some concerns were raised regarding ambiguity and potential confusion with other models.

### Operational Relevance and Longevity
- The group considered whether the technical drivers for the extended domain align with operational requirements.
- Potential operational applications discussed included short-range forecasting and biogeochemistry.
- The conclusion was that the extension is primarily a technical requirement for AMM15 and does not currently have a strong operational science driver.

---

## 3. NEMO Surge Model and Environment Agency Project Proposal

Kit, with contributions from Jeffrey Polton and others, presented a proposed Environment Agency-funded project to improve the NEMO surge model and water-level forecasting system.

### Project Overview and Objectives
- A five-year Environment Agency-funded project.
- Focused on improving flood and water-level forecasting.
- Will enhance the NEMO surge model and associated systems.
- Involves multiple teams and stakeholders.
- The Environment Agency will steer and review project progress.

### Current System Challenges
Identified challenges include:

- Poor forecasting of negative-to-positive surge events.
- Challenges in the Thames Estuary.
- Suboptimal performance in estuaries due to coarse model resolution.
- Issues associated with radiational tides.
- Difficulties representing tidal asymmetry.

### Model Development Work Packages

#### Phase 1
Focus on optimisation of the existing model:

- Tidal tuning
- Bathymetry updates
- Bottom friction tuning
- Wind stress tuning

#### Phase 2
More substantial model developments:

- Upgrade to NEMO version 5
- Higher-resolution testing
- Investigation of coupled systems

### Technical Innovations and Testing

Planned developments include:

- Testing new tidal forcing datasets (FEZ22 and TPXO10)
- Updating bathymetry using newer datasets
- Refining bottom friction using sediment maps
- Evaluating spatially and temporally varying wind stress from wave models
- Investigating AGRIF for flexible resolution and improved reproducibility

### Project Timeline and Next Steps
- The project proposal and business case are currently being finalised.
- The timeline is partly driven by large tidal events expected in the early 2030s.
- Phase 1 developments should be tested and ready for integration between April and June next year.
- Phase 2 developments are expected to be specified by 2028 and implemented by 2030.

---

## 4. Ensemble Forecasting and Data Assimilation Considerations

Matthew Martin and Kit discussed ensemble forecasting and data assimilation within the project.

### Ensemble Spread and Uncertainty
- The project contains a dedicated uncertainty work package.
- The Environment Agency is interested in improved prediction intervals and greater use of ensemble forecasts.
- Matthew Martin highlighted ongoing work involving:
  - Stochastic physics
  - Spatially correlated bottom-friction uncertainty
  - Ensemble generation techniques

### Future Data Assimilation Plans
- Data assimilation is not currently included in the proposal.
- Potential future developments may involve:
  - Satellite-derived sea surface height observations
  - SWOT observations
  - Other satellite data sources
- Jeffrey Polton stressed the importance of preparing for future data assimilation integration.

---

## 5. Coupled System and Bottom Friction Enhancements

Segolene and Kit discussed future enhancements involving bottom friction parameterisations and coupled systems.

### Wave-Induced Bottom Friction
- Wave-induced bottom friction is under consideration.
- Current bottom-friction parameterisations are heavily tuned.
- A sediment-based, time-varying approach could improve physical realism.
- Integration with wave-model outputs may provide additional benefits.

### Coupled System Testing
- Plans exist to test a fully coupled atmosphere-ocean-wave system within AMM15.
- Objectives include:
  - Optimising model interactions
  - Improving water-level forecasts
  - Improving wave forecasts
- The team acknowledged significant tuning complexity and further technical development requirements.

---

# Follow-Up Actions

| Action | Owner |
|----------|--------|
| Obtain clarification from Andy Clark on whether licensing and attribution for new ancillary files should be included as metadata or separate files, and communicate the outcome. | Ana |
| Follow up with Ben Fitzpatrick regarding software licensing for shared workflows and update the group when guidance is available. | Ana |
| Finalise and communicate the chosen name for the extended AMM7 configuration (**EAMM7**), ensuring consistency across files and documentation. | Richard Renshaw |
| Complete and submit the final project proposal and business case for the Environment Agency water-level forecasting improvements, including contract management and costing details. | Kit |
| Review whether satellite observations (e.g. SWOT, Sentinel-3) should be reintroduced into the long-term plans for the Environment Agency project and considered for Phase 2 developments. | Kit |