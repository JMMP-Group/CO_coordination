# Coastal Ocean coordination meeting minutes

8th December 2025

Participants: Ana Aguiar, Matt Martin, Jeff Polton, Richard Renshaw, Jonathan Tinker, Kit Stokes, Segolene Berthou, Oliver :ambert-Brown

Apologies: Andy Saulter, Susan Kay.

----------

## Agenda :
1.	Review actions from previous meeting (on 15th September 2025).
2.	Discuss licensing of model ancillary files.
5.	AOB
   - Review of NOC/Met Office collaboration.

----------

## Actions from previous meeting:

- 9.1 Matt to arrange a meeting with James While and Juan Castillo to discuss creation of a new CO9pq branch, merging all CO9p2 branches, and FOAM_package, to avoid future conflict merges for CO9p2.
   - Segolene said that Juan had merged all his CO9 branches into one branch.
   - Matt agreed that it has been completed for Juan's branches, but it isn't clear about merging in the FOAM_package branch, and whether that is a good idea given it is used by the global FOAM system too.
   - Matt will check with James about whether this is desirable.

- 9.2 Oliver and Ana will share a proposition for a GitLab UKMO/CO repository structure, to be reviewed at the next meeting.
   - a meeting was held, organised by Daley about the GitLab NEMO repository structure and working practices.
   - Jeff agreed NOC will be moving towards using the central NEMO Gitlab repo, along the lines of what Daley proposed, when developing new configs, e.g. CO10. Oliver is leading this initial development for CO10, currently in a private repository.
   - Progress in this direction will be discussed and reviewed at future CO coordination meetings.
   - Existing/old NEMO configs within the Met Office will be moved to Github (from the existing fcm repos), while any new developments will happen in Gitlab.

New action. Review working practice of CO10 development at future CO coordination meetings.

- 9.3 Ana to send out an agenda ~1 week ahead of the next meeting, 8 Dec 2025
Add an item on CO files licensing to the agenda of the next meeting: "Software licences and copyright (ancillary files and validation tools)"
   - Action closed.

## Licensing ancillary files:

Oliver and Jeff have been discussing the ownership and licensing of ancillary files using the creative commons licence.
This is in progress, and Oliver will complete a list of files and their licensing and pass to Jeff for review.

New action. Oliver will complete list of NEMO ancillary files and their licences, and pass to Jeff for review.

## AOB:

Matt asked about the definition of the vertical coordinates in AMM7. Jeff clarified that AMM7 uses multi-envelope coordinates which AMM15 does not use.

Ana noted request from Jerome Chanut to access data from s coordinate model (AMM15) to look at vertical modes for a PhD student.
Some data is being prepared from Jon Tinker's area.

Jeff noted the recent high-level meeting to review the NOC/Met Office relationship and the
need to input ideas for improving that on the CO side, including on machine learning.


## Open and new actions:

- 9.1 Matt to check that the CO9p2 branches are now in a good state (no further merging needed).
- 10.1 Ana/Matt to add agenda item to future CO coordination meetings to review the working practices for CO10 development in the NEMO Gitlab repository.
- 10.2 Oliver to complete list of NEMO ancillary files and their licences, and pass to Jeff for review.
