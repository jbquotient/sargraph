# sargraph

## Purpose
The purpose of this software is to Utilize information gathered from sysstat (sa, sar) to generate graphs of system utilization without requiring a full blown monitoring tool.  PNGs are generated from sar data and configuration relevant to the system in question.

## Requirements
- GnuPlot
- Sysstat
- Manual configuration
-- mkdir /var/spool/sargraphs
-- chown root:wheel /var/spool/sargraphs
-- chmod ug+rwx /var/spool/sargraphs
-- chmod g+s /var/spool/sargraphs
-- cp sar-gnuplot* /usr/local/libexec/
-- add to crontab: */15 * * * * /usr/local/libexec/sar-gnuplot-cron current > /var/spool/sargraphs/sar-gnuplot-current.log 2>&1
-- add to crontab: 1 0 * * * /usr/local/libexec/sar-gnuplot-cron yesterday > /var/spool/sargraphs/sar-gnuplot-yesterday.log 2>&1

## TODO
- Make configuration automatic (at present you have a lot to do by hand)
-- Maybe use dmidecode to pull relevant information (total CPU, disks, etc.)
