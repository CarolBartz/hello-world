##################
Fields and Metrics
##################

Usage data presented through this API are presented through Fields and Metrics. A Field is simply some attribute of a set of usage while a Metric is a calculated value against the given Fields.

For example, user `John` could have used `two` products in `January`. In this example, `John` and `January` are the Fields `userName` and `usageMonth` respectively while `two` is the metric `uniqueProducts` given the specified `userName` and `usageMonth`.

Conceptually, Metrics are measures calculated over the grouping of Fields.


=================== ============= ========== ==================================== =======
Name                Field/Metric  Data Type  Description                          Example
=================== ============= ========== ==================================== =======
productLineCode     Field         string     Product line code (PLC)              ACD
productName         Field         string     Product name                         Autocad
productVersion      Field         string     Product version                      2018
productFeatureCode  Field         string     Product feature code                 85730ACD_2018_0F
userName            Field         string     Username (NT ID or email)            john42
usageTimestamp*     Field         string     Datetime of usage                    2014-01-18T06:12:23Z
usageDate           Field         string     Date of usage                        2014-01-18
usageMonth          Field         string     Usage month of usage (day always 01) 2014-01-01
contractYear        Field         integer    Contract year the usage falls under  1
machineName         Field         string     Machine name (Desktop only)          MyMachine
licenseServerName   Field         string     License server machine name          MyLicSvr
usageType           Field         string     License type (Normal or Borrowed)    Borrowed
chargeCategory      Field         string     Charging type (see below)            FREE
usageCategory       Field         string     Usage type (see below)               DESKTOP_PRODUCT
tokenPool           Field         string     Token pool for usage (CY or MY)      CY
transactionDate*    Field         string     Adjustment date (Adj/Cons only)      2014-01-18
reasonType          Field         string     Adjustment reason (Adj/Cons only)    Off network
reasonComment*      Field         string     Adjustment comment (Adj/Cons only)   ACD promotion
chargedItemId*      Field         string     ID for transaction/session           RXHKL8CZRMES
jobStatus*          Field         string     Job status (Cloud Service only)      Success
customFieldX        Field         string     User provided custom field (X: 1-10) GEO
uniqueProducts      Metric        integer    Distinct count of products           42
uniqueUsers         Metric        integer    Distinct count of users              56533
tokensConsumed      Metric        integer    Sum of tokens consumed               62617
usageMinutes        Metric        integer    Sum of duration used in minutes      63521
useCount            Metric        integer    Count of charged events              761
=================== ============= ========== ==================================== =======

\*These fields are transactional/session level details.

***************
Charge Category
***************

===============  ================================================================================
Value                                   Description
===============  ================================================================================
CASUAL           Usage not charged due to being under the chargeable contractual duration for use
INCREMENTAL      Usage charged a differential rate due to existing charged use for a similar/lesser product
CHARGED          Charged usage
FREE             Free usage for sessions after charging has already occurred for that day
===============  ================================================================================


**************
Usage Category
**************

==================  ================================================================================
Value                                   Description
==================  ================================================================================
DESKTOP_PRODUCT     Desktop products such as Autocad and Revit
CLOUD_PRODUCT       Cloud products such as Collaboration for Revit and Fusion360
CLOUD_SERVICE       Cloud services such as Rendering and Photo-to-3D
MANUAL_ADJUSTMENT   Direct adjustments to token balance
MANUAL_CONSUMPTION  Manually entered product consumption amounts (such as for Off-Network usage)
==================  ================================================================================
