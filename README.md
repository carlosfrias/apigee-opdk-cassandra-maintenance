Apigee OPDK Cassandra Maintenance Playbook
==========================================

Basic maintenance of an Apigee OPDK Cassandra ring amounts to ensuring that we capture 
data backups and that nodetool is used. This playbook manages basic maintenance of the
Cassandra ring used by an Edge instance.
 
## Usage

Usage of this playbook requires that you install the ansible roles and invoke the
maintenance playbook. This is accomplished with the following steps:

    ansible-galaxy install -f -r requirements.yml
    ansible-playbook maintenance -vv 
    
### Available Tags

Several tags are available to help provide some fine grain control in order to work with
a specific node or set of nodes.

* repair: Performs nodetool repair -pr
* rebuild: Performs nodetool rebuild
* start: Starts apigee-cassandra
* stop: Stops apigee-cassandara
* restart: Restarts apigee-cassandra
* restart_rmp_ms: Restarts routers, message processors and management server
* cache: Update the cache with server facts used during playbook execution.

    
    