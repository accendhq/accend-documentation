# STMT.ATTR

Returns metadata about an Accend statement.

Syntax\
`=ACCEND.STMT.ATTR(statement_ref, attribute)`

Parameters\
`statement_ref`: A statement dropdown label created through the Accend task pane, or a raw `statement_id`.\
`attribute`: The statement attribute to return.

Supported attributes\
`period_length`\
`start_period`\
`end_period`\
`period_type`\
`data_type`\
`status`

Returns\
The requested statement attribute.

Example\
`=ACCEND.STMT.ATTR(B2, "period_length")`

Notes\
Use a statement dropdown created through the task pane for the most reliable results.
