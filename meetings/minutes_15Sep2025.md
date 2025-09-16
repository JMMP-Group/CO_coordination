# Coastal Ocean coordination meeting minutes

15th September 2025.

Participants: Ana Aguiar, Matt Martin, Richard Renshaw, Kit Stokes, Oliver Lambert-Brown, Jeff Polton, Segolene Berthou, Jonathan Tinker

Apologies: Susan Kay, Andy Saulter

----------

## Agenda :
1. Review actions from previous meeting, [minutes_09Jun2025](https://github.com/JMMP-Group/CO_coordination/blob/main/meetings/minutes_09Jun2025.md)
2. Discuss the formulation for atmospheric forcing used in amm15 research vs operation
   -  How to/who should run first trials with NWP to detect issues earlier on
   - Merge of CO9_tides with FOAM_package branch to reduce conflicts at fcm_make stage?
   - Creation of a UKMO/CO on NEMO GitLab to facilitate the porting/exchange of model developments between JMMP-CO and UKMO/CO work (managed by OM team)
3. General info
   - Recommendation to run Dave Storkey's script for namelists comparison for every NEMO upgrade
   - Improvements to CO research workflow (Oliver)
  
----------

## Actions from previous meeting
   - 7.2 Ana and Susan to find out about the use of the new NEMO5 time-stepping for BGC. [Update 18/06/2025, AA]: Renauld Person confirmed that the BGC and NEMO can run with different time-steps and he has successfully run experiments at NEMOv5 with RK3, using different time-steps for NEMO and PISCES. Closed.
      - Next step is to try coupling ERSEM to NEMO5 to test RK3 with different time-steps (work by PML).
   - 8.1 Richard and Segolene to contact Jeff for advice on how to use NAARC (take a cut out) to generate a bespoke config for UKCI. Closed.
      - Richard and Segolene had a discussion with Jeff and Jason. No final decision made but NOC will work on this in collaboration with Met Office (Alice Richards and Richard Renshaw).

## Surface forcing 
CO9p2 initial trials revealed an issue in that several points along the coast reached unrealistically high SSTs (up to 80 deg C). Could these issues have been detected earlier on with earlier testing of a new CO configuration with NWP forcing? Now there's a NWP dataset shared with NOC and CO10 could be tested with NWP forcing ahead of handover for ~2 years; this dataset needs updating as it dates from pre-CPLNWP; (ideally) the testing period should overlap with tests from previous configuration. Trials with ERA5 can be run for a longer period and would be the best (stable dataset) for a baseline comparison with the previous configuration. We could potentially extend trialling to coupled mode, pending resources; Julia Rulent has successfully run REP-configuration, wave-ocean coupled on ARCHER. In CHAMFER there's scope to run trials with ~25 yrs Met Office forcing hindcast as an alternative to ERA5 (Segolene is currently working on the licence as CEH also needs this); GLORYS5 (up to 2014) -> GLORYS6 to provide lateral ocean boundary conditions. These would inform early tests for UKV.
   - CO10 trials will not be run within the next three years, which gives enough time to prepare: 1) long-enough new LBCs from the non-defence ORCA12 system, and 2) SBCs from CPLNWP to produce a new surface forcing dataset. Important for accurate validation and operational readiness.
   - Revisit bulk versus direct forcing as the mismatch between atmosphere and SST in coastal points was at the origin of some of the problems in CO9p2. This was addressed by applying UKMO_Haney relaxation near the coast. The original UKMO_Haney relaxation is undocumented; implementation in CO9p2 has been described and reviewed on [utils#744](https://eur01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fcode.metoffice.gov.uk%2Ftrac%2Futils%2Fticket%2F774%23comment%3A21&data=05%7C02%7Cana.aguiar%40metoffice.gov.uk%7C13e3ab44ee4b487f0d5408ddf42fee83%7C17f1816120d7474687fd50fe3e3b6619%7C0%7C0%7C638935208987444490%7CUnknown%7CTWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D%7C0%7C%7C%7C&sdata=Zb9Oe0MNjC%2BxxEz9kJBt6qdXQ3sVPkQ%2BaV%2F1zNDFxCA%3D&reserved=0)
   - Coupled works best with a direct flux formulation but in a forced configuration it is not clear whether or not direct fluxes or bulk formulation is the best choice for a forced configuration.
   - Jon noted that amm7 uses direct because when trying bulk with ECMWF forcing that impacted the BGC; amm7 and amm15 use direct forcing, unlike other regional model,

## CO9 branches merge conflicts
Proposal to create a new branch to simplify merging further changes to CO9p2 without affecting the global system. "CO9p2_tides" branch has all the consolidated Met Office developments/CO9 branches, could be merged with FOAM_package to create a single CO9p2 branch. See new Action.

## JMMP_CO GitHub updates and NEMO GitLab UKMO/CO
Oliver proposed a process to automate syncing of JMMP_CO updates to a UKMO/CO group hosted at NEMO GitLab.
There was discussion on whether to have different projects for each configuration or opt for the same struture as GOSI. Any changes would have to pass SETTE tests and follow a merge request process. Details to be agreed - see new action.

## General info
These items were just for general knowledge.

----------

## New/open actions:
  - 9.1 Matt to arrange a meeting with James While and Juan Castillo to discuss creation of a new CO9pq branch, merging all CO9p2 branches, and FOAM_package, to avoid future conflict merges for CO9p2.
  - 9.2 Oliver and Ana will share a proposition for a GitLab UKMO/CO repository structure, to be reviewed at the next meeting. 
  - 9.3 Ana to send out an agenda ~1 week ahead of the next meeting, 8 Dec 2025
     - Add an item on CO files licensing to the agenda of the next meeting: "Software licences and copyright (ancillary files and validation tools)"
