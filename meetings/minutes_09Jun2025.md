# Coastal Ocean coordination meeting minutes

9th June 2025.

Participants: Ana Aguiar, Matt Martin, Richard Renshaw, Andy Saulter,
Kit Stokes, Oliver Lambert-Brown, Jeff Polton, Segolene Berthou,
Jonathan Tinker, Susan Kay

----------

## Agenda :

1. Review actions from previous meeting, 10Mar2025
2. Short presentation on PS48 results (Jon Tinker)
3. General issues
4. Summary on CO10 requirements and progress
5. Summary on new amm7 for UKCI requirements (Richard Renshaw)
6. Summary on wind farms parametrisation in NEMO (Segolene Berthou)
7. AOB

----------

## Actions from previous meeting

   - 7.1. Kit spoke to Juan and the WWIII version and grid in the CO9 setup are in line with what is expected. Closed.
   - 7.2. Susan asked PML about using BGC with the time-stepping in NEMO5 but no work is going on about that at the moment. This will be raised at the upcoming NEMO system team meeting. Carry forward.
   - 7.3. Jon prepared a presentation on the PS48 results. Closed.

## Short presentation on PS48 results (Jon Tinker)

Jon gave a presentation on AMM15/7 PS47 trials results.
   - Changes include the use of Met Office lateral and surface boundaries (instead of Mercator Ocean and ECMWF ones),
as well as the inclusion of altimeter assimilation on the shelf.
   - Near-bed temperature biases seemed to be reduced when compared to the ICES data.
   - Overall the PS47 version of the system was improved over the current operational version.

## General issues

Ana mentioned two issues:
   - Porting of the shelf system onto the new Met Office HPC has been completed - no significant difference with the version on the old HPC.
   - It would be helpful to have a clear record of where the ancillary files come from, especially for the AMM7 bathymetry.

## CO10 requirements

These were discussed last time and were not revisited.

## UKCI requirements for new domain

Richard described the need for a larger domain at a similar resolution to AMM7 both as an intermediate resolution between the global 1/4 degree model and the AMM15 configuration to be used for UKCI high resolution regional climate projections, and to allow running of coupled BGC
in those projections at a lower resolution than AMM15.

   - Jeff said that it would be important to call such a configuration something different to AMM7 which was an existing configuration name.
   - Jeff also mentioned the possibility to use (a cut out of) the North Atlantic, Baltic and Arctiv domain (NAARC) that NOC have developed which is at 1/12 degree resolution. This full domain would be too expensive, but a cut out of it is a possibiility.
   - Segolene asked if the Skagerak region was well represented in that model, but that specific region hadn't been assessed in detail yet.
   - Jeff said that another possibility could be to cut out part of the global 1/36 or 1/12 ORCA gridsand add in the required processes, e.g. terrain following coordinates.

## Wind farms parameterisation in NEMO

Segolene described briefly the Equify project which is aiming to include parameterisations
of wind farms in ocean/waves/atmospheric coupled models and looking at impact in runs of a few years.
This work is being done in the AMM15 ocean configuration.

## AOB
None.

## New/open actions:

7.2 Ana and Susan to find out about the use of the new NEMO5 time-stepping for BGC.
