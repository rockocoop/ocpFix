# ocpFix
project that fixes a cluster deployed without proper cluster hostname



Fixes a cluster where the parameter openshift_master_cluster_hostname was not defined during deployment.

To use do the following:

1. Locate the inventory file that was used when deploying the cluster
2. Update the file with the parameter openshift_master_cluster_hostname
3. Add the following parameters under all:vars

  currentContext: <value of the missing parameter with "-" instead of "." in the value>

  apiPort: <master API port>

4. Run!
