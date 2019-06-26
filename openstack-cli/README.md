Openstack documentation

Here is the documentation on openstack-cli image docker usage.

To be logged on your openstack account, you have multiple ways.

You can do a source file with your environment variables.

You can use -v to choose the storage volume of the container.

You can charge the container with the -e option to show the environment variables or the charge your own one.

Use -e and a file who containt your varibles, or use --env to enter manualy your variables.

As exemple:

docker run -it -v asforgecom/openstack-cli -e openrc.sh openstack-cli /bin/bash 

or 

docker run -it -v asforgecom/openstack-cli --env Var1=value1 --env VAR2=value2 openstack-cli /bin/bash

You have to charge the container in /bin/bash mode to interact with it.

