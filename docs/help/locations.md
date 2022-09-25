# Locations

## Why
- A location is defined as a place where assets are operated, are stored, or are repaired
- Use the Locations application to specify and to track locations for assets.
- Use locations to track movement of assets from place to place. (Locations typically are static areas while assets might move to various locations)


## When

When to create a location? (instead of a site or storeroom)
- Does this location require work to be done against it? Are work orders or PM's written against it? If yes, then create a location.
- Is your location a physical geographical area with boundaries? If this is a far stretching area made up of multiple towns or business segments maybe this should be considered an organization or a site rather than a location.
- Can the location be considered a storeroom where items are received, stored, issued from, transferred to/from? If so, maybe this entity should defined as a storeroom. If the storeroom however requires that work is done there (work orders, PMs etc.) then maybe this entity requires a storeroom record as well as a standard location record created for it.
-  Do the various locations have some connection to each other? Is there for example a business park that is defined as a site, that is made up of various buildings that are as defined as parent locations? Are these buildings then segmented into various offices and rooms that are also defined as locations? Are those rooms segmented even further into cubes where work might be done? This is important for you to understand to help build your location hierarchies.

## Types of locations
- **Operating**: where work happens
- **Transit**: When assets are being moved from one location to another. E.g. Courier, Labor carrying asset to service location, etc.
- **External**: When asset is in repair facility, or returned to Vendor, or being salvaged or donated
- **Receiving area**: Area where assets are stored pending inspection before moving to storeroom.
