# Openstack-cli documentation

Here is the documentation on openstack-cli image docker usage.
It's a container to use openstack-cli. It also contains nano and GIT.

### Table of content

1. [Run with environment variables.](#environment)
2. [Run with volume file.](#volume)
3. [Command options.](#option)

To be logged on your openstack account, you have multiple ways.

# Run with environment variables. <a name="environment"></a>

## First option
Use the -e option with the file who contains your environment variables.

```bash
docker run -it -e openrc.sh openstack-cli /bin/bash
```

Replace 'openrc.sh' by your environment variables file.

## Second option

Use the --env option for each variable.

```bash
docker run -it
--env OS_USERNAME=
--env OS--PASSWORD=
--env OS_PROJECT_ID=
--env OS_PROJECT_NAME=
--env OS_USER_DOMAIN_NAME=
--env OS_PROJECT_DOMAIN_ID=
--env OS_REGION_NAME=
--env OS_INTERFACE=
--env OS_IDENTITY_API_VERSION=
openstack-cli /bin/bash
```

# Run with volume file. <a name="volume"></a>

You can use the -v option to choose the container storage volume.

```bash
docker run -it -v /workdir:openrc.sh openstack-cli /bin/bash 
```

You can change '/workdir' by your workspace in the container.
Replace 'openrc.sh' by your environment variables file.

# Command options. <a name="option"></a>

The --it option alows you to enter in the container.
openstack-cli is the image name.
/bin/bash allows you to have a shell. 

