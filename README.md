# mbxpro-batpro-windows
Set of scripts and wrappers to re-implement Huawei PC Manager's Battery Protection feature in a transparent, independent way.

## How does it work?
Uses RWEverything (http://rweverything.com/) to write directly to the laptop's Embedded Controller registers. RWE has built-in scripting functionality, and I wrap that nicely in Python.

## What has this been tested on?
Huawei Matebook X Pro 2018 (i7 CPU, 16GB RAM, nVidia dGPU)
