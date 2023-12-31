# Ansible is used for: 
        - Configuration managemnet
        - Deployment
        - cloud provisioning and orchestration (but not recommended)
we can do cloud provisioning and orchestration as well but not recommended (recommended for terraform)

# Advantages over shell:
        - error handling in shell is not effective
        - shell script is not easy to read and write
        - for 1000 servers how can we configure
        - how to store sensitive info in shell script
        

# Ansible features:
        - Platform independent
        - Scalable - can connect at a time many servers
        - Idempotence (If you run a program multiple times if it exists it will skip otherwise it will take action)
        providing same result irrespective no of executions
        - Error handling
        - Readable and maintainable
        - valut
        - Rich modules (in ansible we have many module to use directly no need to write)
        - Agent less



# PULL: (CHEF)
Node should connect the server by agent installation
Node should download configuatrion periodically, say every 30 mins
Even there is no chnage in configuartion, agent connects to server that gets unnecessary traffic

# PUSH: (ANSIBLE)

No need to install agent in client/ node machines
Server can connect directly all the nodes
when there is a change in configuartion then only it will conenct server and can push directly to the node
Ansible use ssh authentication to connect the nodes


# commands
# ansible -i inventory WEB --list-hosts
# ansible -i inventory DB --list-hosts
# ansible -i inventory ungrouped --list-hosts
# ansible -i inventory all --list-hosts
# ansible -i inventory project --list-hosts


# Ansible command priority

#1 Terminal
#2 tasks
#3 files
#4 prompt
#5 playbook
#6 inventory
#7 roles

# Datatypes (07-datatypes.yaml)

String, boolean, map, array

# loops

