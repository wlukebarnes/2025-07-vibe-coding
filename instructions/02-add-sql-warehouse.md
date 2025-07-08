https://docs.databricks.com/aws/en/dev-tools/python-sql-connector#:~:text=from%20databricks.,as%20connection%3A

Add a sql-warehouse service to the fastapi app that connects to a databricks SQL warehouse using m2m auth like in the link.
Note, you will need to construct the HTTP_PATH yourself from the warehouse id
add a button on the homepage that queries 'SELECT CURRENT_TIMESTAMP()' from the warehouse to test it, then displays the result in the UI.

use DATABRICKS_HOST and the DATABRICKS_WAREHOUSE_ID to construct the warehouse's endpoint, instead of SERVER_HOSTNAME which the docs use.

update requirements.txt accordingly with databricks-sdk and databricks-sql-connector.
