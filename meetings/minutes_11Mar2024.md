# Coastal Ocean coordination meeting minutes

11th March 2023.

Participants: Mike Bell, Ana Aguiar, Matt Martin, Richard Renshaw, Jeff Polton, Andy Saulter, Breo Gomez, Susan Kay

Apologies: Jonathan Tinker, Hedong Liu, Segolene Berthou.

----------

## Agenda :
1. Review actions from previous meeting.
1. Brief review of progress with CO9 integration (CO9 project, progress overview https://github.com/JMMP-Group/CO_coordination/issues/17)
   - People to add a progress update on their issues before the meeting.
1. Review the list of other more general issues: requirements and progress with future model configurations.
   - Review and discuss amm15 "known issues".
   - CO10 requirements and progress.
1. AOB

----------

## Actions from previous meeting:
   - 2.1 Matt/Ana to check issues before the meetings. _Closed_
   - 2.2 Matt to reopen the CO9 AMM15 model issue to mention issue with nn_it000. _Carry forward_
   - 2.3 Hedong/Mike to check whether NEMO can provide an output field with flags about whether a cell is wet/dry. _Carry forward_
   - 2.4 Matt to clarify with Susan that CO9 is 4.0.4. _Closed_
   - 2.5 Matt to raise an issue to include the requirement that CO10 will include AMM7/AMM15 at the same NEMO revision. _Closed_
   - 2.6 Matt to ask James to pass back to Jeff the changes he made for TEOS-10. _Carry forward_
   - 2.7 Jon to check the issues fit with CO9 plan he has and the timescales. _Closed_
   - 2.8 Andy/Ana/Matt to discuss with Jon about working meetings on CO9 integration. _Closed_
   - 2.9 Ana/Matt to organise the next meeting in about 3 months and to spend more of the meeting discussing requirements and progress with new model configurations (CO10). _Closed_
   - 2.10 Ana/Matt to ask Chris Bunney about WWIII ticket system to see whether we can learn how to improve our monitoring/setting up issues from that system. _Closed_

## Notes:

Previous actions reviewed as above: several could be closed but others were carried forward.

Regarding changes for TEOS-10, Matt talked to James but changes have yet to be passed to Jeff.
Matt said that WWIII ticket system follows similar practice to NEMOVAR. Post-meeting, Andy shared a link to a diagram of [a Gitflow](https://i0.wp.com/solidfish.com/blogs/git/gitwf.jpg?w=1140).

Mike told the meeting that Hedong will be leaving the Met Office in May.

Mike suggested a meeting to prioritise Hedong's work regarding: the issue with ni_it000 values giving different results; output diagnostics for wetting/drying cells; conversion of CO8 restarts to CO9 restarts; upgrading CO9 AMM7 to the same NEMOVAR version as AMM15 (v4.0.4).
Jeff suggested including Ryan Patmore in these discussions so he could also provide some support/advice on modelling issues.

## Progress with CO9 integration:

- Matt asked if there was a tool to convert CO8 restarts to CO9 (change in variables and new bathymetry leads to changes in vertical coordinates).
- AMM15 CO9 and CO8 have been run for a few months by James and the overall statistics look similar between the twom but there are some biases remaining in SSH and off-shelf deep temperatures.
- James is investigating these biases, but it is possibly due to the initial conditions coming from a long model-only run which have biases.
- AMM15 spin-up with DA using CO9 will take a long time and tit might be better to convert fully spun-up (with DA) CO8 restarts to CO9.
- James to share results with Jeff and Ryan Patmore (NOC-Liverpool) to get help investigating the bias or support to produce a restarts conversion tool (based on existing tool for GO config?).
- James's changes to the FOAM R&D suite are ready to be reviewed and Matt/James will decide with Ana/Mike who's best placed to review James' changes.

## General issues:

- [River inputs](https://github.com/JMMP-Group/CO_coordination/issues/4): Ana mentioned that Segolene's team plans to develop a river product from the operational forecast (probably a mix of global (Europe) and regional (UK) for OOFS; For developing/testing the configuration, reanalysis products are available and Sarah Wakelin has done work to assess these, [ESSD - GloFAS-ERA5 operational global river discharge reanalysis 1979-present](https://essd.copernicus.org/articles/12/2043/2020/) dataset is good for Europe but JRA's river discharge is better for the Global ocean. CO10 development tests will be forced by ERA5 and run with associated GloFAS.
- [Baltic LBCs (Copernicus)](https://github.com/JMMP-Group/CO_coordination/issues/3): Jeff mentioned that CO9 includes an option to apply a pre-defined offset to the Baltic LBCs to account for differences in Atlantic and Baltic LBC SSH values. Richard Renshaw said that for reanalysis they tuned this value, and that new versions of Baltic reanalysis resulted in the need to change the value.
there is a difference in SSH between the Baltic and the Atlantic boundary Matt to check with James what version of Baltic LBCs and settings are in use.

----------

## Open and new actions:
 - 2.2 Matt to reopen the CO9 AMM15 model issue to mention issue with nn_it000.
- 2.3 Hedong/Mike to check whether NEMO can provide an output field with flags about whether a cell is wet/dry.
- 2.6 Matt to ask James to pass back to Jeff the changes he made for TEOS-10.
- 3.1 Mike: Organise meeting with Hedong, Matt, James and Ryan Patmore to prioritise Hedong's work on model issues for CO9.
- 3.2 Jeff: Check if AMM7 can be released as 4.0.4 (to match version in AMM15).
- 3.3 Jeff/Ana: Discuss offline to outline a procedure to feedback/merge all bug fixes back to NEMO trunk.
- 3.4 All: To discuss in future meetings whether to run tests with reanalysis and operational (NWP) forcing, to check best choice of settings/parameters (e.g. river input, fluxes formulation). Sarah Wakelin at NOC is the best contact re tests with different forcing (she has been investigating fresh water bias). Similar discussion will take place for GOSI.
- 3.5 Matt: Check with James what Baltic LBC version/settings are being used and discuss with Jon and/or Ryan/Jeff whether any changes in the SSH offset are needed.
- 3.6 Jeff: Share documentation on CO9p2 with James, Matt and Ana.
- 3.7 Ana/Matt to organise next meeting in about 3 months. Prioritise, at the next meeting:
   - Discuss CO10 requirements and progress
   - Review near-bed temperature biases
- 3.8 All: Add labels (can generate new ones) to issues, to facilitate grouping related issues through use of filter.
