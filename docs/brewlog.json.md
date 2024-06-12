The schema defines the following types:

## BrewLogType 

Recording of the data in real brews.

**BrewLogType** is an object with these properties:

|Name|Required|Type|Description|
|--|--|--|--|
| **description** |  | string|  |
| **original_gravity** |  | [GravityType](measureable_units.json.md#gravitytype)| measured original gravity |
| **final_gravity** |  | [GravityType](measureable_units.json.md#gravitytype)| measured final gravity |
| **unadjusted_ph** |  | [AcidityType](measureable_units.json.md#aciditytype)| measured pH |
| **mash_ph** |  | [AcidityType](measureable_units.json.md#aciditytype)| measured pH |
| **before_boil_ph** |  | [AcidityType](measureable_units.json.md#aciditytype)| measured pH |
| **after_boil_ph** |  | [AcidityType](measureable_units.json.md#aciditytype)| measured pH |
| **mash** |  | [MashLogType](.md#mashlogtype)|  |
| **fermentation** |  | [FermentationLogType](#fermentationlogtype)|  |



## MashLogType 

Recording of the data in real brews.

**MashLogType** is an object with these properties:

|Name|Required|Type|Description|
|--|--|--|--|
| **measured_gravity** |  | Array of [GravityLogType](#gravitylogtype)| a list of measured gravity |

## FermentationLogType 

Recording of the data in real brews.

**FermentationLogType** is an object with these properties:

|Name|Required|Type|Description|
|--|--|--|--|
| **measured_gravity** |  | Array of [GravityLogType](#gravitylogtype)| a list of measured gravity  |
| **measured_ph** |  | Array of [pHLogType](#phlogtype)|  a list of measured pH |


## GravityLogType
Recording of the gravity in real brews.

**GravityLogType** is an object with these properties:

|Name|Required|Type|Description|
|--|--|--|--|
| **time** | ✅   | [TimeType](measureable_units.json.md#timetype) | Time since the start of the stage(Mash/Fermentation). |
| **gravity** | ✅ | [GravityType](measureable_units.json.md#gravitytype)| measured gravity |


## pHLogType
Recording of the pH in real brews.

**pHLogType** is an object with these properties:

|Name|Required|Type|Description|
|--|--|--|--|
| **time** | ✅   | [TimeType](measureable_units.json.md#timetype) | Time since the start of the stage(Mash/Fermentation). |
| **ph** | ✅ | [AcidityType](measureable_units.json.md#aciditytype)| measured pH |
