# Organization
Company
- Name
- _IndustryId_

BusinessUnit
- _CompanyId_
- Name
- Address
- _CountryId_
- Location (coordinates)
- Code
- _Type_ (Warehouse, plant, branch)
- _ParentBusinessUnitId_
- MEScore (USP)

# Assets
Product
- Name
- Description

ProductAssets (Impacted products)
- _ProductId_
- _AssetId_ 

Asset
- Name 
- Description
- Parent asset
- PurchaseInformation
    - _VendorId_
    - _ManufacturerId_
    - InstallationDate
    - PurchasePrice
    - ReplacementCost

- Model
- Serial No.
- _BusinessUnitId_
- _Type_ (customizable - e.g. Production, IT, fleet, facilities)
- BusinessImpactScore (1-10)
- Criticality (0-100)
- Risk (0-100)
- EffectiveAge (in years)
- _ProjectId_
- _AssetStatus_ (Not ready | Operating | Decommissioned )
- _GLAccount_

AssetUserAndCustodians
- _AssetId_
- _UserId_
- _GroupId_
- IsPrimary
- IsCustodian (responsible for care of asset)
- IsUser

AssetSpecifications
- _AssetId_
- AttributeName
- AttributeDescription
- AttributeNumericValue
- AttributeGenericValue
- AttributeUnitOfMeasure

SpareParts
- Name
- Description

AssetSpareParts
- _AssetId_
- _SparePartId_
- Quantity
- Remarks

Tags
- Name
- Description
- _TagGroupId_

AssetTags
- _AssetId_
- _TagId_

MaintenanceSchedule
- Name
- Description
- _Type_ (Preventive | On need basis)
- Recurring (No | Yes)
- Frequency (Repeat every)
- FrequencyType (Day|Week|Month|Year)
    - DayOfWeek (SMTWTFS)
    - OccuranceType (fixed day | Occurance - applicable for month and year)
    - DayOfMonth
    - MonthOccuranceInstance (First|Second|Third|Fourth|Last)
    - MonthOccuranceDay (In combination of DayOfWeek) 
    - MonthOfYear (in combination of DayOfMonth)
    
MaintenanceActivity
- Name
- Description
- _Type_ (Mechanical, IT, etc)
- EstimatedTime
- Estimated cost
- Sequence

MaintenanceActivityDocuments
- Name
- Description
- _MaintenanceActivity_
- Filename

AssetMaintenanceInstance
- _AssetId_
- _MaintenanceScheduleID_
- DueDate
- ActualDate
- AssignedTo
- ExecutedBy
- Priority
- State (Created | Approved | Rejected | InProgress | Hold | Completed)
- _ApprovalInstanceId_
- Type (Service request | Incident | Problem | Work order)
AssetMaintenanceInstanceActivities
- _AssetMaintenanceInstanceId_
- _MaintenanceActivity_
- ExecutedBy
- Timestamp
- Notes
- ActualTime
- IsCompleted

AssetMaintenanceInstanceActivityDocuments
- _AssetMaintenanceInstanceActivityId_
- Filename

Material
- Name
- Description
- Cost

AssetMaintenanceInstanceMaterials
- _AssetMaintenanceInstanceId_
- _MaterialId_
- Quantity

Tool
- Name
- Description

AssetMaintenanceInstanceTools
- _AssetMaintenanceInstanceId_
- _ToolId_
- Duration

Workorders
- Type (preventive | Special | corrective )
- _FailureCodeId_

FailureCodes
- Name
- Description

FailureCodeProblem
- _FailureCodeId_
- Name
- Descriptions

FailureCodeProblemCause
- _FailureCodeProblemId_
- Name
- Descriptions

FailureCodeProblemCauseRemedy
- _FailureCodeProblemCauseId_
- Name
- Descriptions

MeterTypes
- Continuous (Cumulative | Miles | Hours | Pieces produced)
- Gauge (Range | Fuel level | temperature | Presure | Oil level)
- Characteristic (Domain values | Clarity | Color | Texture)

Meters
- Name
- Description
- _MeterTypeId_
- UnitOfMeasure

AssetMeters
- _AssetId_
- _MeterId_
- Sequence
- CumulativeValue
- RangeStartValue
- RangeEndValue
- LastReadingDate
- LastReadingInspector

# Contracts
### ContractTypes
- Warranty
- Purchasing
    - Price
    - Purchase
    - Blanket
- Lease rental
- Labor Rate 

### Life cycle
Enter contract > Select properties > Apply terms > Enter lines > Approve > Revise

ContractTypes
- Name
- Description

Contract
- Name
- Description
- Revision
- _ParentContractId_
- _ContractTypeId_
- Status (Draft | Active | Inactive)
- _VendorId_
- _VendorId_
- StartDate
- EndDate
- RenewalDate
- TotalCost
- CustomerTerminationAllowed
- CustomerNotificationPeriod
- VendorTerminationAllowed
- VendorNotificationPeriod
- AcceptancePeriod

ContractTypeTermsAndConditions
- Name
- Description
- Editable
- DefaultOnPO

ContractTermsAndConditions
- _ContractId_
- _ContractTypeTermsAndConditionsId_
- Sequence
- SendToVendor

ContractTypeProperties
- Name
- Description
- DataType (Bool | Numeric | Date)

ContractProperties
- _ContractId_
- _ContractTypePropertyId_
- DefaultValue
- Editable
