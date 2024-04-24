# Configuration files and enviroment variables

HarperDB is configured through a **YAML** file called  **harperdb-config.yaml** located in the HarperDB root directory; by default this is a directory named **hdb** located in the home
directory of the current user.

## Configuration file and usage

To change configuration values we need to 
edit **harperdb-config.yaml** file and save
any changes. This file can be located in the **hdb** directory.S

**HarperDB needs to be restarted for changes to take effect**

Some important sections in this file are:

- `http sessionAffinity`: This section is used to improve the efficiency and fairness of thread utilization by routing multiple requests from the same client to the same thread.

- `clustering`: This section configures the clustering engine, which is used to replicate data between instances of HarperDB

Alternately, configuration can be changed via environment and/or command line variables or via the API


## Enviroment Variables

This are the important variables from HarperDB:

- `TC_AGREEMENT`: This variable is used to agree to the terms and conditions
- `HDB_ADMIN_USERNAME`: This variable is used to set the admin username
- `HDB_ADMIN_PASSWORD`: This variable is used to set the admin password
- `ROOTPATH`: This variable is used to set the root path
- `OPERATIONSAPI_NETWORK_PORT`: This variable is used to set the network port

These environment variables can be used to automate HarperDB installations

