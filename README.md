# Example of port forwarding configuration

This is the first attemp to deployment and configure port forwarding.

## Assumptions

This document assumes a following packages installed on the local host:
* Docker > 12.0
* Ansible > 2
* Virtual Box > 5

## Nodes
This infraestructure are composed by three nodes.
* Node A: This machine has running a nginx docker.
* Node R: There is a machine with internet and private network connectivity.
* Node Inet: It represents any machine with internet connection.

## Up infrastructure
For start all machines on environment

    $- vagrant up

Check if all vagrant are created correctly

    $- vagrant status
        Current machine states:

        nodoA                     running (virtualbox)
        nodoR                     running (virtualbox)
        inet                      running (virtualbox)














