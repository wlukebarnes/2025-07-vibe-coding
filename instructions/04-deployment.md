## app.yml

https://docs.databricks.com/aws/en/dev-tools/databricks-apps/app-runtime , but use my configurations and not the link's

this app will be deployed on databricks. within /app, create a databricks `app.yml` using the documentation, but use this WAREHOUSE_ID from my rules 4b9b953939869799.

the command section should be like how i always run it, Note, env vars should ONLY include catalog, schema, table_prefix, and databricks_warehouse_id, databricks_server_hostname. make sure theyre capitalized. they should be of this type:

-   name: {name of env var}
-   value: {value of env var}

## databricks.yml

Create a `databricks.yml` file in the /app folder with the following structure:

-   `bundle` section with the app name
-   `workspace` section specifying:
    -   `root_path`: The deployment path in Databricks workspace (/Workspace/Shared/wlukebarnes/20250605demos)
    -   `host`: The Databricks host URL
-   `permissions` section with level: CAN_MANAGE for group_name: users
-   `targets` section with default workspace configuration

The file should be placed in the root of the project, and will be used to deploy the code as an asset bundle to the specified workspace path. The host should be set to "e2-demo-field-eng.cloud.databricks.com" as specified in the environment.

Note: The actual app configuration (name, warehouse ID, etc.) will be handled by the Databricks notebook that creates the app infrastructure, rather than in this YAML file.

### Deploy.sh

Create a `deploy.sh` file in the root of the project that deploys the bundle using the service principal whose secrets are in /app/.env. it should load the whole /app/.env to environment vars in this script.
