# mbxpro-batpro-windows
Set of scripts and wrappers to re-implement Huawei PC Manager's Battery Protection feature in a transparent, independent way.

## How does it work?
Uses RWEverything (http://rweverything.com/) to write directly to the laptop's Embedded Controller registers. RWE has built-in scripting functionality.

## What's included?
A set of RWE scripts that emulate the PC Manager presets. Three demo PowerShell scripts for reading current EC values and setting two of the presets (off and office).

## What has this been tested on?
Huawei Matebook X Pro 2018 (i7 CPU, 16GB RAM, nVidia dGPU)

## EC Registers
Register `0xe4` on the EC stores the low end of the battery charge range. Register `0xe5` stores the high end. Register values are stored as HEX values.

## `rwe_scripts`
`off.rw`
Low: 0%
High: 100%

`family.rw`
Low: 40%
High: 70%

`office.rw`
Low: 70%
High: 90%

`travel.rw`
Low: 95%
High: 100%

`read.rw`
Read the values of the relevant EC registers.

## Things to do
1. Central PowerShell Script
2. Generate RWE scripts with custom threshold values

## Credits
Based on batpro script in the Linux driver here: https://github.com/nekr0z/linux-on-huawei-matebook-13-2019/blob/master/batpro

RWE implementation inspired by https://github.com/maisi/HP-Spectre-x360-Tools
