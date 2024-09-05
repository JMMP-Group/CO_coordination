# Coastal Ocean coordination meeting minutes

2nd September 2024.

Participants: Ana Aguiar, Matt Martin, Jeff Polton, Richard Renshaw, Jonathan Tinker, Susan Kay, Andy Saulter.

Apologies: Segolene Berthou, Mike Bell.

----------

## Agenda :
1.	Review actions from previous meeting (on 2rd June 2024).
1.	Review the list of other more general issues:
   - Requirements and progress with future model configurations.
   - CO10 requirements and progress.
   - Review near-bed temperature biases.
1.	Gen2 benchmarks: what version(s) of NEMO will CO configurations use in late 2027?
1.	CO manager vacancy
1.	AOB
   - JMMP workshop online 7-11 Oct 2024
   - Next meeting to take place on the 9th Dec 2024

----------

## Actions from previous meeting:
- 3.2 Jeff: Run further testing of AMM7 so that it can be released at 4.0.4 (to match version in AMM15).
   - GloSea6 forced AMM7 is now working (work by NOC and Dale at PML).
   - CO9 AMM7 config now exists, and NOC/PML testing that it performs ok.
   - Dale is now including FABM/ERSEM in this configuration.
   - Action closed.
   - New action: Jeff to forward information about the CO9-AMM7 configuration to Matt, Jon and others so it could be bought into Met Office systems with DA.

- 3.8 All: Add labels (can generate new ones) to issues, to facilitate grouping related issues through use of filter.
   - Most issues have labels now but not all.
   - Jeff said he finds the milestones useful, particularly for indentifying priorities.
   - It was suggested that GO and CO labels ought to be done consistently.
   - Carry the action forward.

- 4.1 Segolene: Ask Juan if we still need to check whether NEMO can provide an output field with flags about whether a cell is wet/dry. (follows from previous Action 2.3)
   - Ana had talked to Juan and Segolene but didn't have an update on this action so carry the action forward.
   - Ana mentioned an issue raised by Juan about the wave coupling.
   - There was a discussion between Andy and Jeff about behaviour of wave model in very shallow waters, i.e.  in the wetting-and-drying cells.
   - Jon mentioned that Mike and Juan have discussed this and some more tests are now being run.
   - Jeff said he would benefit from more information about the issue so he could better contribute to the discussion.
   - New action: Ana/Segolene to raise an issue in the issue log on the wetting/drying behaviour of the waves.

- 4.2 Matt: Send James's doc on dealing with LBCs to Jeff and, if necessary, arrange a meeting with James, Jon, Jeff and others from NOC (Ryan Patmore/Sarah Wakelin) so that James presents what he has done with the Atlantic and Baltic SSH BCs and the MDT.
   - Matt said that James has written a document describing what he's done on this issue.
   - He will forward James's document to Jeff and Richard for input.
   - If a meeting is still needed, then Matt will organise it.
   - Carry the action forward.

## CO10 development updates:

- Jeff provided a useful email update on progress with AMM developments before the meeting.

## Near bed temperatures:

- Jon briefly mentioned results from his experiments.
   - Using Met Office fluxes improved things, but still working on investigations.
   - Using ICES profile data for assessment which has a lot of data not in EN4.
   - It would be useful for Jon and Matt to discuss the latest with this and what to do next.
   - Jeff suggested an Ocean Ice Tea with external people involved to have a focussed discussion on this issue, including Ryan.
   - New action: Jon to organise seminar (or smaller meeting(s) if preferred) to describe the issue, results and discuss with Met Office and NOC people.

## Gen2 benchmarks: what version(s) of NEMO will CO configurations use in late 2027?:

- NEMOv5 will be used for global benchmarks. CO won't be used for benchmarks.
- CO9 is NEMOv4.0.4 and CO10 at NEMOv4.2 is being used in projects now with preliminary testing of tides being done in NEMOv5.
- Jeff will think about possible motivations to excite activity of jumping to NEMOv5 in CO10.
- Matt said from a DA perspective that we don't want to develop versions at NEMOv4.2 and NEMOv5 (e.g. for shelf and global).

## CO configuration manager:

- Ana said that the external recruitment campaign was unsuccessful and asked if anyone had suggestions for moving forward.
- Andy/Richard said that ongoing waves or shelf seas climate recruitment campaigns might have suitable candidates.

## Open and new actions:

- 3.8. All: Add labels (can generate new ones) to issues, to facilitate grouping related issues through use of filter.
- 4.1 Segolene: Ask Juan if we still need to check whether NEMO can provide an output field with flags about whether a cell is wet/dry.
- 4.2 Matt: Send James's doc on dealing with LBCs to Jeff and, if necessary, arrange a meeting with James, Jon, Jeff and others from NOC (Ryan Patmore/Sarah Wakelin) so that James presents what he has done with the Atlantic and Baltic SSH BCs and the MDT.
- 5.1. Jeff to forward information about the CO9-AMM7 configuration to Matt, Jon and others so it could be bought into Met Office systems with DA.
- 5.2. Ana/Segolene to raise an issue in the issue log on the wetting/drying behaviour of the waves.
- 5.3. Jon to organise seminar (or smaller meeting(s) if preferred) to describe the issue, results and discuss with Met Office and NOC people.
