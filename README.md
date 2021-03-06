# Hall A Analyzer Hands-On Tutorial
This is a small replay and analysis setup for demonstration of
the [Hall A C++ Analyzer Podd](https://github.com/JeffersonLab/analyzer)
at the June 2017 Hall A & C Analysis
[Workshop](https://redmine.jlab.org/projects/podd/wiki/Workshop2017) at JLab.

## Prerequisites
It is assumed that you have both ROOT and the analyzer set up.
Example raw data files are included in the virtual machine image
distributed at the workshop. To run this tutorial outside of the
virtual machine, appropriate files need to be linked or copied from
JLab SciComp disks (/cache, /volatile, /work) or restored from tape.

## Setup
Put data files or links to them in local directories, then update the
included setup.sh accordingly. Run setup.sh to define the required
environment variables `DB_DIR`, `DATA_DIR` and `OUT_DIR`.

## Replay
To run the example replay, do

```bash
cd replay
analyzer
analyzer [0] .x replay.C
```

## Analysis
Some simple analysis scripts have been provided. Open the .root file
for a run you're interested with the analyzer, then run the script.
Example

```bash
cd replay
analyzer $OUT_DIR/gmp_23062.root
analyzer [0] .x plotR.C
...
```

## More Information
Please see the the [presentation](http://hallaweb.jlab.org/data_reduc/AnaWork2017/Podd-Anawrk2017-2017-06-26.pdf)
given at the workshop.
