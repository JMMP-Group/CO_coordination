# Coastal Ocean coordination meeting minutes

11th December 2023.

Participants: Mike Bell, Segolene Berthou, Ana Aguiar, Matt Martin, Jonathan Tinker, Hedong Liu, Jeff Polton, Andy Saulter.

Apologies: Susan Kay, RIchard Renshaw.

----------

## Agenda :
1. Reminder of the objectives of the CO coordination meetings
1.	Review actions from previous meeting (listed in the minutes of the last meeting)
1.	Overview of the GitHub repository for CO coordination, e.g. location of meeting minutes, List of issues for coordination.
1.	Review progress with issues related to CO9 integration, collected into the CO9 project. Ideally people to add a progress update on their issues before the meeting.
1.	Review the list of other more general issues (including assigning owners to them).
1.	AOB: Membership of the group - should it include people doing the development work? Do we need a separate set of meetings for people doing the development work?. What do people think about the structure of the meeting and way of working with GitHub?


## Notes :

All previous actions were completed.

The Github repository and list of issues were described and the overall structure welcomed.

Progress with CO9 integration was reviewed (see issues for detailed updates):
- The AMM15 model implementation has been completed except an outstanding issue when nit000 is not one which is on the list for Hedong to investigate.
- DA technical implementation is almost complete and testing/assessment will follow with focus on wetting-and-drying regions.
- Work has not started yet on the AMM7 version. Jeff noted that this is at a slightly earlier NEMO version (4.0.2) compared to AMM15. Matt mentioned the requirement for future model releases to include AMM7 and AMM15 at the same version to make integration work easier.
- Work on the wave/ocean coupling was discussed. Issue about whether a flag about the cells are wet/dry can be obtained from NEMO was discussed.
- BGC work hasn't yet started, and it was mentioned to clarify with Susan that the version of the model in CO9 is 4.0.4.
- There was the suggestion/question about whether issues should be closed rather than marked as completed?

List of other issues:
- There wasn't much time to review progress with the other issues.

AOB:
- The membership and purpose of the group was discussed, and it was agreed that this set of meetings should be for managers to coordinate the work and for discussing requirements for the model.
- A suggestion for future meetings is to spend less time on CO9 integration and focus a more on discussing requirements and progress with new/future model configurations.
- For CO9 integration work, perhaps a set of working meetings should be organised, to be discussed with Jon Tinker.


## Actions:
   - 2.1 Matt/Ana to check issues before the meetings.
   - 2.2 Matt to reopen the CO9 AMM15 model issue to mention issue with nit000.
   - 2.3 Hedong/mike to check whether NEMO can provide an output field with flags about whether a cell is wet/dry.
   - 2.4 Matt to clarify with Susan that CO9 is 4.0.4.
   - 2.5 Matt to raise an issue to include the requirement that CO10 will include AMM7/AMM15 at the same NEMO revision.
   - 2.6 Matt to ask James to pass back to Jeff the changes he made for TEOS-10.
   - 2.7 Jon to check the issues fit with CO9 plan he has and the timescales.
   - 2.8 Ana/Matt to organise the next meeting and to spend more of the meeting discussing requirements and progress with new model configurations (CO10).
   - 2.9 Ana/Matt to ask Chris Bunney about WWIII ticket system to see whether we can learn how to improve our monitoring/setting up issues from that system.