# Coastal Ocean coordination meeting minutes

9th December 2024.

Participants: Ana Aguiar, Matt Martin, Jeff Polton, Susan Kay, Segolene Berthou, Christopher Stokes.

Apologies: Andy Saulter, Jonathan Tinker, Richard Renshaw.

----------

## Agenda :

1. Review actions from previous meeting (on 2nd Sep 2024).
2. Review the list of other more general issues
   - Summary on CO10 requirements and progress.
   - Update on near-bed temperature biases.
3. Gen2 benchmarks: motivations for jumping to NEMOv5 in CO10 (late 2027)
4. Oliver Lambert-Brown (Foundation Scientist) recruited for the post of Coastal Ocean modeller (CO manager) starts on 2nd of Jan, Ocean Modelling team. Oliver has completed a Master of Maths (2022) and a Master of Research Climate and Atmospheric Science (2024), University of Leeds. They do not have numerical modelling experience but in their MRes project, co-supervised by Diego Bruciaferri, they analysed NEMO output.
5. AOB
   - NEMO Hackathon 16-20 Jun 2025, Exeter // NEMO system team meeting
   - Next meeting to take place on the 10 Mar 2025

----------

## Actions from previous meeting:

- 3.8. All: Add labels (can generate new ones) to issues, to facilitate grouping related issues through use of filter.
   - Issues have some labels which will be reviewed as per need. 
   -_Action closed._
- 4.1 Segolene: Ask Juan if we still need to check whether NEMO can provide an output field with flags about whether a cell is wet/dry.
   - Juan worked out how to determine if a cell is wet/dry and this has been helpful for debugging. 
   - _Action closed._
- 4.2 Matt: Send James's doc on dealing with LBCs to Jeff and, if necessary, arrange a meeting with James, Jon, Jeff and others from NOC (Ryan Patmore/Sarah Wakelin) so that James presents what he has done with the Atlantic and Baltic SSH BCs and the MDT.
   - Matt sent a document with information for dealing with LBCs to Jeff who then forwarded this to people at NOC. 
   - _Action closed._
- 5.1. Jeff to forward information about the CO9-AMM7 configuration to Matt, Jon and others so it could be bought into Met Office systems with DA.
   - Jeff shared information about the [CO9-AMM7](https://github.com/JMMP-Group/CO_AMM7/tree/CO9_AMM7_v4.0.4) configuration with others at the Met Office/OFRD. 
   - _Action closed._
- 5.2. Ana/Segolene to raise an issue in the issue log on the wetting/drying behaviour of the waves.
   - Issue#20 was raised to document the problem with wetting/drying when coupling with waves. Work is ongoing as problem is not solved.
   - _Action closed._ 
   - New Action: Ana/Segolene to talk to Jon Tinker and draft a work plan to address this issue, bringing together limited resources from different teams. Under guidance, Oliver may be able to help with runs coupled mode as a way to learn about the code. People in Jon Tinker's team should be able to help and this may be relevant to Copernicus. Julia (NOC) may be able to offer some support too.
- 5.3. Jon to organise seminar (or smaller meeting(s) if preferred) to describe the issue, results and discuss with Met Office and NOC people.
   - Jon gave an OIT where he presented some of this work but we would like to have a summary here before deciding to close this action.
   - Close this action, but open new action: Jon to update this group on the current status of the bottom temperature issue.

## CO10 development updates:

- Jeff has a working version of CO10 (with NEMOv4.2) but currently has no plans/staff/project to do the porting to NEMOv5. This could be supported by Oliver and we should discuss it after Oliver has gained some experience with NEMO and Rose/Cylc.

## Gen2 benchmarks: what version(s) of NEMO will CO configurations use in late 2027?:

- This may motivate the upgrade of CO10 to NEMOv5, depending on whether there's a need to accelerate the turnaround time of the CO configuration
- Susan asked if it's possible to run BGC with a different time-step and if there are restrictions on MLF or RK3

## CO configuration manager:

Ana to ask Jonathan Tinker to invite Oliver to CO9 dev meetings.

## AOB

Ana mentioned the NEMO hackathon which will be held at the Met Office in June 2025 which will be led by Jeff Polton and Katherine Hutchinson is helping to organise. She encouraged people working on CO aspects to attend.

Susan asked for clarification/recommendations about the equation of state (EOS-80 or TEOS-10) to use in AMM15 and AMM7.
Matt and Jeff agreed that CO9 uses TEOS-10. Some experiments using the same system were run with EOS-80 at NOC due to different boundary conditions being available, but the version to be used at the Met Office is with TEOS-10.
New action: Matt and Jeff to clarify in any CO9 documentation and Github issues that TEOS-10 will be used. 
There will be work next FY to implement CO9-AMM7 in the Met Office rose suites, including the DA and the BGC.


## Open and new actions:

- 6.1. Jon to update this group on the current status of the bottom temperature issue.
- 6.2 Ana, Segolene and Jon to propose a way forward to address the issue with the waves and wetting-and-drying now that Juan has less time to devote to it. Oliver to try to help with this in coupled mode as a way to learn how to run experiments. Julia (NOC) could also offer some support.
- 6.3 Ana to check if, at NEMOv5, BGC can run with a different time-step (from physics) and if there are any restrictions on time-stepping scheme: MLF or RK3.
- 6.4 Matt and Jeff to clarify in any CO9 documentation and Github issues that TEOS-10 will be used.
