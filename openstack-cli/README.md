# Openstack-cli documentation

Here is the documentation on openstack-cli image docker usage.
It's a container to use openstack-cli. It also contains nano and git.

### Table of content

1. [Run with environment variables.](#environment)
2. [Run with volume file.](#volume)

To be logged on your openstack account, you have multiple ways.

# Run with environment variables. <a name="environment"></a>

Use the --env option for each variable inside the openrc.sh file.

```bash
docker run -it \
  --env OS_USERNAME= \
  --env OS_PASSWORD= \
  --env OS_TENANT_ID= \
  --env OS_TENANT_NAME= \
  --env OS_REGION_NAME= \
  --env OS_IDENTITY_API_VERSION= \
  --env OS_AUTH_URL= \
  asforge/openstack-cli /bin/bash
```

# Run with volume file. <a name="volume"></a>

You can use the -v option to bind the openrc.sh file locally to your container.

```bash
docker run -it -v ${PWD}/openrc.sh:/openrc.sh asforge/os bash -c "source /openrc.sh; bash"
```
