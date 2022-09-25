# Assets lifecycle

## Maintenance methodology
Drives assets lifecycle approach. 
Approach defines 
- what - what work (tasks)
- when - how often
- how - task orders
- where - one or more locations
- who - labor or craft

Sample methodologies 

### Total productive maintenance (TPM)
- Top-down-approach
- Primary GOAL - Zero unplanned downtime.
- Continuous improvement
- Success measure is OEE - overall equipment effectiveness

`OEE = Availability X Performance Rate X Quality Rate`

OEE addresses the six major equipment losses encountered on the equipment 
- breakdowns
- set-up and conversion
- start-up losses
- idling and minor stoppages
- design speed loss
- defect and rework losses

### Reliability centered maintenance (RCM)
- Bottom-up-approach
- Structured maintenance approach
- Primary GOAL - Understand consequence of failure and work on reducing it.
- Success measure: MTBF - mean time between failures (measure of reliability of equipment).



## Maintenance stages
### Plan
- Accumulate budget
- schedule for asset acquisition
- specifications
- entry
- item master setup asset strcture and configurations

### Acquire
- procure from vendor
    - vendor management
    - purchase request
    - purchase order
    - receiving
    - invoicing
- interdepartment transfer
- construct
- contract management
    - Lease contracts & payment schedules
    - warranty contract
    - purchase contracts

### Commissioning
- Locations where assets operates
- Assigned to employee, project of business unit
- status is tracked thought out its lifecycle
- contracts, maintenance schedules, job and safety plans are associated with locations or assets or both.

### Maintain

- condition based automatically generated preventive and predictive maintenance work
- corrective or emergency maintenance at repair facilities (depot maintenance)
- spareparts and consumable inventory items (impacts inventory balance triggers reordering process)
- cost rollups

### Retire
- disposed off, auctions, donated, returned to leasing company
- One of tracking assets that have reached end of life is by creating location that represents vendor or type of disposition (e.g.) All assets are in decommisioned state in these locations. e.g.
    - vendor A Returns
    - Scrapped 
    - Donated to A


## Asset Status
### Not ready 
 - Default status for new assets
 - PM on these assets do no create any workorders
 - Non preventive maintenace workorders can be created -such as inspection, installation, etc

Synonyms
- Installed
- Commissioned

### Operating
- PM schedules can generate workorders
- Repair workorders

Synonym
- Active
- Limited use
- Commissioned
- PM
- Workorders

### Decommissioned
- do not appear in search
- can be move to locations

synonyms
- Broken
- Inactive
- Missing
- sealed
- out of service


## Rotating assets
- Rotating assets 
    - interchangeable (PC monitors, pumps, etc)
    - Has Inventory item number - used track assets as a group (total number)
    - can be moved and tracked across locations, sites
    - Has issue cost
    - current balance
    - multiple instances can be used
    - requires to have an item created and added to storeroom
- non rotating assets
    - cannot be moved in or out of storerooms
