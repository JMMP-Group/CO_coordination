# Coastal Ocean coordination meeting minutes

9th January 2026

Participants: Ana Aguiar, Matt Martin, Jeff Polton, Jonathan Tinker, Segolene Berthou, Oliver Lambert-Brown, Susan Kay, Richard Renshaw, Andy Saulter

Apologies: Kit Stokes

----------

## Agenda :
1. Review actions from previous meeting (on 8th December 2025).
2. Update on PS48 (CO9p2) trials/issues (Jon Tinker)
3. Update on plans for (Oliver/Ana)
   * UKMO/CO Gitlab repository (see Oliver's slide in attachment) - NEMO v4.2.2 and above (CO10+)
   * CO on Met Office GitHub  - versions up to NEMO v4.0.4 (CO9p2-)
4. AOB
 
----------

## Actions from previous meeting:

- 9.1 Matt to check that the CO9p2 branches are now in a good state (no further merging needed).
For branches in the Met Office, to include Haney relaxation. _Action closed_

- 10.1 Review working practice of CO10 development at future CO coordination meetings. _Action closed_

- 10.2 Ancillary files list - Action remains open/Ongoing.

## Update from Jon Tinker, PS48:

JT: Mar 2023 issue (negative SSH in points just outside river input points) has not reoccurred over a year of trials, after Pete Sykes patched the innovations files and short-stepped the model (20 sec time-step) to by-pass the problematic days; the trial is continuing, and has completed without further problems. 
MDT issues: Main issue is that ORCA12 (and CMEMS GLO-MFC/other CMEMS models) removes an offset from the satellite based MDT, which changes the mean sea level. We don’t want to do this in CO9p2, as WAD may be more sensitive to arbitrary changes to the mean sea level.
CO9p2 could have an offset applied at the boundaries so that their MDT is consistent with the raw satellite MDT product, rather than adding an offset to the MDT, or an offset added to the MDT. Comparing model with and without the MDT offset, there is a difference in currents and tide, but it is small – this is evidence to make the case for a common MDT reference in CMEMS products. Current solution (for output to CMEMS) is to add an offset afterwards as a post-processing step; @PS48 the LBCs are from public ORCA12, which as an offset MDT, so an offset has to be added to the these LBCs – at a later date, the public ORCA12 MDT could also be replaced with the raw satellite based MDT.
Another issues is that the bathymetry that Enda created uses the mean sea level as reference whereas NEMO uses the geoid as reference; ideally the two would be consistent but that requires an update of the bathymetry - to be done sometime in the future. MM wrote a document with details on the MDT issue.
JT: Euler option required to fix 25h mean bug.
JT: cold coastal SSTs in the operational system are due to using the wrong land-sea mask and stash code... Research suite was correct.

SB: Can remove SSH offset from LBCs but not advisable to do so in the restart files because that leads to significant issues (large temperature oscillations within a day) along the coastline.

OLB: FOAM R&D with or without DA (free run) runs without further instability when the bathymetry file is edited to "fill in" problematic cells This happened for 2 grid cells aligned horizontally near a river mouth, in the west coast of Denmark; these cells were dugout for river runoff and are 10m deep with 50 levels. The fix was to reduce these cells to 10 levels, now 2m deep. There are other dugout points across the domain, but over 14 months in FOAM suite and 10 years ocean-only hindcast these have not caused issues.

AS: Decision wrt stability of the model (CO9p2 as is for PS48) must be made by the end of Mar 2026, not acceptable to trigger instabilities more than 1-2 per year.

## Oliver presented plans for UKMO/CO (see slide attached)

Developers can fork from the main and should keep their fork up to date with bug fixes and developments from the main.

MM: CO9p2 was handed over a long time ago, and new bug fixes (very common) plus namelist changes (rare) or DA developments have been added since then.
AS: Process sounds similar to WWIII development: The 'main' is rarely updated and gets tagged when a new package of changes gets merged; there's a 'develop branch' (would get pull requests with light review).
MM: How would the developments work? Create a branch of CO11, then develop for DA and eventually merge back to CO11 and potentially tag that commit as a new version e.g. CO11.2.
JP: amm7 and amm15 configurations at each releases? If not, then flag/add disclaimer that one of them has not been released yet. We will have to discuss this/revisit procedure for release (at these meetings) closer to time.

## AOB:

AS: We have a business case for a new generation of coastal models for surge, 2D barotropic models. To be decided which resources/teams will be involved as part of the CO programme.

---
## Open and new actions:

- 10.2 Oliver to complete list of NEMO ancillary files and their licences, and pass to Jeff for review.