# Coastal Ocean coordination meeting minutes

10th Mar 2025.

Participants: Ana Aguiar, Matt Martin, Jeff Polton, Susan Kay, Segolene Berthou, Christopher Stokes (Kit), Richard Renshaw, Oliver Lambert-Brown, Mike Bell, Kate Lindeque (work experience student).

Apologies: Andy Saulter.

----------

## Agenda :

1. Review actions from previous meeting [on 9th Dec 2024](https://github.com/JMMP-Group/CO_coordination/blob/main/meetings/minutes_9Dec2024.md).
2. Review the list of other more general issues
   - Summary on CO10 requirements and progress.
5. AOB
   - Next meeting to take place on the 9th of Jun 2025

----------

## Actions from previous meeting:

- 6.1: Jon Tinker reported on the AMM15-PS47 trials with the Met Office (direct) forcing instead of ECMWF's (bulk formulae), showing improvements in temperature profiles, ICES NBT Abs Bias (Mod-Obs) Seasonal Means are reduced (all experiments used ORCA12 LBCs and are coupled with WWIII, ICES bottom water temperature used if profile depth is greater than 30m); biases are a couple of degrees. Bottom temperature and sea level anomaly improves across the domain, except in some coastal locations. Impact on tides will be assesed next, with help from Oliver. Jeff suggested comparing the experiments with physics-only free experiments. No comparison with multi-model ensemble yet, Results for AMM7 are expected to be similar.
   -_Action closed._
 
- 6.2: Mike reported that the wave coupling and wetting & drying issue was solved. Juan split the flux limiting of the Eulerian velocities from the Stokes drift. When running the model with constant temperatures and salinities these are now conserved properly, and the experiment has run for 2 months. Mike is confident that the solution works well and the code changes will now be passed to OFRD (James While in first instance) who can run longer trials to ensure robustness. Mike reported that the code changes were made in NEMOv4.0.4, will be merged to NEMOv4.2.4 (gitlab) as a bug fix and incorporated in NEMOv5 (by Daley). Jon Tinker will attend a CMEMS meeting at the end of Mar and will discuss offline who can present an overview of this issue then. Wetting & Drying should go operational at PS48.
  -_Action closed._
  - New Action: Kit to check with Juan what WWIII version and grid he used when testing and inform James While about this to ensure compatibility.

- 6.3: Reply from Renaud Person was not helpful. Can BGC (purely tracer advection) run with a longer time-step? This is a question for ERSEM and FABM people (TOP module). Susan and Ana will ask PML/FABM contacts and NEMO system team (Mike: Is Oliver still working? Ask team in Paris).  
   -_Carry forward._

- 6.4: Documentation revised, it's stated on CO9 branch that the default is to use TEOS-10. 
  -_Action closed._

## CO10 development updates and requirements list:

- Jeff reported a CO10 release, NEMOv4.2.2 running under Canary project but moving on to NEMOv5 which will be the final version in CO10 (for OFRD) and this would align with GOSI10 @NEMOv5. 
- List of requirements for CO10 based on use cases (issue#16, https://github.com/JMMP-Group/CO_coordination/issues/16). Matthew Martin reviewed use cases and success criteria for various applications, including atmospheric model surface boundary layer, search and rescue, subsurface temperature and salinity profiles, sea surface height, and marine ecosystem stress indicators. Jeffrey Polton discussed the importance of these use cases for guiding model development and funding.
- Jon Tinker reported that there's presently an ongoing oil spill in the North Sea; guidance on surface curents is using CMEMS data (not Met Office's output yet).
- Jon Tinker proposed presenting trial results at upcoming meetings for feedback. 
- Matthew Martin suggested including this presentation in the agenda for the next coordination meeting.
- New Action: add Jon Tinker's trial results as a recurrent item to the agenda of following meetings.

## AOB
- Meeting finished at 16:00 as meeting room was booked by others.

## Conclusion
The meeting focused on updates and improvements in temperature profiles, wave coupling, and wetting/drying issues, coordination among teams, and future plans for Nemo version updates and use case assessments. Participants emphasized the importance of effective communication and coordination to ensure robust and consistent model performance.

## New actions:

7.1 Kit to check with Juan what WWIII version and grid he used when testing and confirm that his is the correct one to be implemented in the R&D suite for later implementation in PS48. Also to inform James While about the outcome once confirmed.
7.2 Ana and Susan to find out answer/who can answer question regarding time-step for BGC.
7.3 Ana/Matt to add a short presentation by Jon Tinker on PS48 trial results to the agenda of the next meeting.
