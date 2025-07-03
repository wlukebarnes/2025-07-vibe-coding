https://docs.databricks.com/aws/en/dev-tools/python-sql-connector#:~:text=from%20databricks.,as%20connection%3A

Add a sql-warehouse service to the fastapi app that connects to a databricks SQL warehouse using m2m auth like in the link.
Note, you will need to construct the HTTP_PATH yourself from the warehouse id
add a query on the homepage to 'SELECT CURRENT_TIMESTAMP()' from the warehouse to test it

update requirements.txt accordingly with databricks-sdk and databricks-sql-connector.
