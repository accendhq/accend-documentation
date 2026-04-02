# ACCOUNT

Returns a financial account value from an Accend statement.

Syntax\
`=ACCEND.ACCOUNT(statement_ref, account_key)`

Parameters\
`statement_ref`: A statement dropdown label created through the Accend task pane, or a raw `statement_id`.\
`account_key`: The chart-of-accounts key to retrieve, such as `total_revenue` or `net_income`.

Returns\
The account value for the requested line item. Depending on the account, this may be a number, text, boolean, date, or blank.

Example\
`=ACCEND.ACCOUNT(B2, "total_revenue")`

Notes\
Use a statement dropdown created in the task pane when possible. If the requested account does not exist, the function returns `#N/A`.
