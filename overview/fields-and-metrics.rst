##################
Fields and Metrics
##################

Usage data presented through this API are presented through Fields and Metrics.


=================== ============= ========== ==================================== =======
Name                Field/Metric  Data Type  Description                          Example
=================== ============= ========== ==================================== =======
reasonType          Field         string     Adjustment reason (Adj/Cons only)    Off network
=================== ============= ========== ==================================== =======

\*These fields are transactional/session level details.

***************
Charge Category
***************

===============  ================================================================================
Value                                   Description
===============  ================================================================================
FREE             Free usage for sessions after charging has already occurred for that day
===============  ================================================================================


**************
Usage Category
**************

==================  ================================================================================
Value                                   Description
==================  ================================================================================
MANUAL_CONSUMPTION  Manually entered product consumption amounts (such as for Off-Network usage)
==================  ================================================================================
