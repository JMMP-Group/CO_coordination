# Coastal Ocean coordination meeting minutes

3rd June 2024.

Participants: Ana Aguiar, Matt Martin, Jeff Polton, Susan Kay, Jonathan Tinker, Segolene Berthou, Andy Saulter.

Apologies: Richard Renshaw, Mike Bell.

----------

## Agenda :
1. Review actions from previous meeting.
1. Brief review of progress with CO9 integration (CO9 project, progress overview https://github.com/JMMP-Group/CO_coordination/issues/17)
   - People to add a progress update on their issues before the meeting.
1. Review the list of other more general issues: requirements and progress with future model configurations.
   - CO10 requirements and progress.
   - Review near-bed temperature biases.
1. AOB
   - Next meeting to take place on the 2nd Sep 2024.
----------

## Actions from previous meeting:
- 2.2 Matt to reopen the CO9 AMM15 model issue to mention issue with nn_it000. _Closed_
   - Daley has found a bug and provided a fixed for it. James will pull this fix into his branch at some point.
- 2.3 Hedong/Mike to check whether NEMO can provide an output field with flags about whether a cell is wet/dry. _Carry forward_
   - Matt asked if this was still necessary as it was needed for the waves coupling. Segolene will ask Juan.
- 2.6 Matt to ask James to pass back to Jeff the changes he made for TEOS-10. _Closed_
- 3.1 Mike: Organise meeting with Hedong, Matt, James and Ryan Patmore to prioritise Hedong's work on model issues for CO9. _Time expired_
- 3.2 Jeff: Check if AMM7 can be released as 4.0.4 (to match version in AMM15). _Carry forward_
   -  AMM7 has been released at 4.0.2 but not at 4.0.4. AMM15 is using ERSEM with NEMO 4.0.4. In AMM7, FABM is working fine and this workflow has been updated to NEMO 4.0.4 (Susan and Segolene) but Jeff says there's a difference in domain.cfg file and the coordinates file are different from 4.0.2. Participants agreed that AMM7 and AMM15 NEMO versions should be aligned while we are not ready to retire AMM7. There is a requirement for AMM7 at CO9 but a parallel suite number behind AMM15. Doing a release of AMM7 at NEMO 4.0.4 should not be too onerous, needs a bit more testing.
- 3.3 Jeff/Ana: Discuss offline to outline a procedure to feedback/merge all bug fixes back to NEMO trunk. _Closed_
   - Process is to raise issue and provide evidence to support change so that issue can be reviewed before merge request. Process is long but should work OK.
- 3.4 All: To discuss in future meetings whether to run tests with reanalysis and operational (NWP) forcing, to check best choice of settings/parameters (e.g. river input, fluxes formulation). Sarah Wakelin at NOC is the best contact re tests with different forcing (she has been investigating fresh water bias). Similar discussion will take place for GOSI. _Closed_
   - Jon: LBCs constraints: ORCA12-OS output starts in the summer and runs for 1.5 yr before it becomes impossible to share the data due to classification. Is that enough given it starts in stratified conditions? it will allow more or less one year of testing. This isn't ideal, but is OK for now.
   - Segolene: Atmospheric forcing may change through the period of testing as it will cover an interval when the atmospheric model changed, but it was agreed that we can live with this.
   - Matt: Alternative is to run ORCA12 R&D suite to produce longer a time-series of data for a recent period. That needs planning and may not be a viable solution for CO10 development, but could be for future versions.
   - Details to be discussed offline, but it was agreed to go with the 1.5 years of operational ORCA12 output for now.
- 3.5 Matt: Check with James what Baltic LBC version/settings are being used and discuss with Jon and/or Ryan/Jeff whether any changes in the SSH offset are needed. _Superseded by Action 4.1_
   - James applied a correction at the Baltic boundary but first attempt still results in an offset. There are also issues around the coast. Further corrections/changes are required. James has so far used the Mercator boundaries, the problem may change when switching to ORCA12 boundaries. James will summarise what he has done with the Atlantic and Baltic boundaries and the MDT, and arrange a meeting with Jon Tinker and Jeff (and others from NOC) to present it and discuss.
- 3.6 Jeff: Share documentation on CO9p2 with James, Matt and Ana. _Closed_


## Progress with CO9 integration:
- James's changes to the FOAM R&D suite are have been implemented in the  trunk. Further changes are likely to be needed to deal with the issues with the SSH.
- It proved to be too difficult to transform a CO8 restart file to initialise a CO9 run, so this approach has been abandoned. A longer spin-up will be carried out instead.
- Once similar performance has been demonstrated between CO8 and CO9, James will test some DA improvements.

## Update on CO10 development:
- Jeff: CO10 is planned to be at NEMO v5. It is currently being developed at @NEMO 4.2 and making progress. Porting to NEMO 5.0 will be done to test tides ahead of official release of version 5.0 in Sep.
- Matt/Andy pointed out the use cases listed on issue #16 that cover the requirements for the operational system. It would be good if diagnostics based on these use cases could be included in the assessment of CO10.

## General issues (we did not have much time to discuss these):

- Jon: AMM15 near-bed temperature biases. Met Office winds are stronger than ECMWF's, under high wind conditions, but otherwise similar . This could explain the deeper MLD, and earlier break down of stratification, driven by high wind events. Initialisation of stratification happens under low wind conditions, and so happens at the same time in MO and ECMWF experiments. Divergence of MO and ECMWF bottom temperatures appear to happen when profiles show a second thermocline. Other centres runs show better bottom temperature.
- Jeff: Wind farms parametrisations. Several proposals submitted to produce schemes to model mixing due to wind farms. As a group, we need to find solutions for capturing the dynamic effects of this anthropogenic change.

----------

## Open and new actions:
- 3.2 Jeff: Run further testing of AMM7 so that it can be released as 4.0.4 (to match version in AMM15).
- 3.8 All: Add labels (can generate new ones) to issues, to facilitate grouping related issues through use of filter.
- 4.1 Segolene: Ask Juan if we still need to check whether NEMO can provide an output field with flags about whether a cell is wet/dry. (follows from previous Action 2.3)
- 4.2 Matt: Arrange a meeting with James, Jon, Jeff and others from NOC (Ryan Patmore/Sarah Wakelin) so that James presents what he has done with the Atlantic and Baltic SSH BCs and the MDT.
