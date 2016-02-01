# sargraph
## Purpose
The purpose of this software is to Utilize information gathered from sysstat (sa, sar) to generate graphs of system utilization without requiring a full blown monitoring tool.  PNGs are generated from sar data and configuration relevant to the system in question.
## Requirements
- GnuPlot
- Sysstat
## TODO
- Make configuration automatic (at present you have a lot to do by hand)
-- Maybe use dmidecode to pull relevant information (total CPU, disks, etc.)
