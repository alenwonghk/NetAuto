This playbook will deploy BGP configuration to the Edge Router connecting clients

This file will consume host_var/r1.lab.esxi which contains
 - AS number of the Edge router 
 - Customer information ( AS number, hand-off subnets, Client prefixes, Circuit ID and Custumer ID)
     * stored as a list of dictionary. An item of the list represent a circuit for a customer
 
these will be translated into BGP configuration on the edge router, storing in temp/r1.lab.exsi
file r1.lab.exsi will then be copied to r1's flash as candidate.cfg and will merge with running-config and consequently stored in startup-config
 
to avoid prompts from file opearation, "file prompt quiet" will be applied beforehand the merge operation on R1. "file prompt alert" will be applied after the file operations

pre-requisite: SCP will need to be enabled and authorization need to be added
ip scp server enable
aaa authorization exec default local none 