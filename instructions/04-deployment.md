## app.yaml

https://docs.databricks.com/aws/en/dev-tools/databricks-apps/app-runtime , but use my configurations and not the link's

this app will be deployed on databricks. create a databricks `app.yaml` using the documentation, but use this DATABRICKS_WAREHOUSE_ID: fcb81010db67a28c. Use the docs to determine the command section, this is a flask app.

for the env section, Note, env vars should ONLY include CATALOG, TABLE_PREFIX, DATABRICKS_WAREHOUSE_ID, DATABRICKS_HOST. Get the values from example.env and add them here. they should be of this type:

-   name: {name of env var}
-   value: {value of env var}

<!--  Today we will use another method to deploy the app. Ignore this comment.

## databricks.yaml

Create a `databricks.yml` file in the root of the project with the following structure:

-   `bundle` section with the app name
-   `workspace` section specifying:
    -   `root_path`: The deployment path in Databricks workspace (/Workspace/Shared/wlukebarnes/20250605demos)
    -   `host`: The Databricks host URL
-   `permissions` section with level: CAN_MANAGE for group_name: users
-   `targets` section with default workspace configuration

The file should be placed in the root of the project, and will be used to deploy the code as an asset bundle to the specified workspace path. The host should be set to "e2-demo-west.cloud.databricks.com" as specified in the environment.

Note: The actual app configuration (name, warehouse ID, etc.) will be handled by the Databricks notebook that creates the app infrastructure, rather than in this YAML file.

### Deploy.sh

Create a `deploy.sh` file in the root of the project that deploys the bundle using the service principal whose secrets are in .env. it should load the whole .env to environment vars in this script. -->
