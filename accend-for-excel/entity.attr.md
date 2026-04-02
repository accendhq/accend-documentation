# ENTITY.ATTR

Returns an attribute for an Accend customer or property.

Syntax\
`=ACCEND.ENTITY.ATTR(entity_id, field)`

Parameters\
`entity_id`: An Accend entity ID such as `sp_cust_...` or `sp_asset_...`.\
`field`: The entity field to return.

Common fields\
`legal_name`\
`currency`\
`dba_name`\
`customer_type`\
`website`\
`address`\
`full_address`\
`property_type`

Returns\
The requested customer or property field.

Example\
`=ACCEND.ENTITY.ATTR("sp_asset_abc123", "full_address")`

Notes\
This function works with both customer and property entity IDs.
