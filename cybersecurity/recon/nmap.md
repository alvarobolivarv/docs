# Nmap
This documentation is created as a cheatsheet reminder not replacing original documentation.

## General scan
Scan `-p-` (all ports) `--open` (only open ports) `-v` `-n` (not use DNS) `-oG` (output in grepable format).
`nmap -p- --open -T5 -v -n 10.10.10.197 -oG open-ports.txt`

## Agil scan
Scan `-p-` (all ports) `-sS` (using tcp syn technique) `--min-rate 5000` (send speed of 5000 packets per second) `--open` (only open ports) `-vvv` (level 3 verbosity) `-Pn` (skip host discovery)
`$ nmap -p- -sS --min-rate 5000 --open -vvv -n -Pn`



