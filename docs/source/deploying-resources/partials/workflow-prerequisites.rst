Overview
--------

This workflow describes deploying cloud resources, consisting of:

- A 'domain' containing a network and security group
- A gateway node with internet access
- 2 to 8 compute nodes with internet access

Prerequisites
-------------

This document presumes the following situation:

- The appropriate cloud tool is installed and configured with access details
- There is enough availability in the upstream cloud region of your account to deploy these resources 
- A suitable CentOS 7 source image is available in the cloud provider for basing nodes off of 

