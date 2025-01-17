CSU_RadarTools README
---------------------
Python tools for polarimetric radar retrievals.

This codebase was developed at Colorado State University by numerous people,
including Brenda Dolan, Brody Fuchs, Kyle Wiens, Rob Cifelli, Larry Carey, Timothy Lang,
and others.

Currently, fuzzy-logic-based hydrometeor identification, blended rainfall,
DSD retrievals, and liquid/ice mass calculations are supported. There is also an 
algorithm that uses a finite impulse response (FIR) filter to process differential phase
and calculate specific differential phase.
Finally, there are some tools to do rudimentary QC on the data.

These are supplied as standalone functions that take polarimetric radar data
as arguments. Scalars and arrays are supported as function inputs. The main exception
is csu_kdp.calc_kdp_bringi() which requires individual rays, sweeps, or volumes of 
radar data. 

CSU_RadarTools Installation
---------------------------
To install:
`python setup.py install`
(you may need to have sudo privileges, depending on your setup)

To access, use the following in your analysis code:
```
from csu_radartools import (csu_fhc, csu_liquid_ice_mass, csu_blended_rain, csu_dsd, 
                            csu_kdp, csu_misc)
```

For help information do help on individual modules. There is also a demonstration IPython notebook in the notebooks directory that covers all the modules. 

CSU_RadarTools is known to work under Python 2.7 and 3.4. Other Python versions are untested.
