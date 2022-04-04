# Organization setup

## Entity types
Organization can customize the entity types to match their business vocabulary. (e.g. Company, Division, Business unit, etc.)
### Validations
- System should have one and only one entity type marked as *root*.
- Entity type cannot be deleted if an entity is created with this type under the organization structure.
- Entity type marked as *leaf* cannot have child entities. 
- Entity type code and title should be unique.
- Entity types can be configured to allow child entities of specific entity types.
- Allowed entity type configuration cannot be removed if atleast one entity has been created with the relation.
