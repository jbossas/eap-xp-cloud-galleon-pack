# Server startup

When an EAP XP server provisioned with the cloud feature-pack is started, a set of bash scripts are executed in order to adjust 
the server configuration. These bash scripts are controlled by a set of environment variables that this document describes.

When running an EAP XP server inside the EAP S2I (Source-to-Image) runtime and builder images, you can use [these environment variables](https://github.com/jboss-container-images/openjdk/blob/develop/modules/jvm/api/module.yaml) to configure the Java VM.

EAP S2I runtime and builder images are exposing a set of [environment variables](https://github.com/wildfly/wildfly-cekit-modules/blob/main/jboss/container/wildfly/run/api/module.yaml) to fine tune the server execution.

# Configuring the server

All the [Environment variables](https://github.com/jbossas/eap-cloud-galleon-pack/blob/main/doc/launch.md) defined in the [EAP cloud galleon pack](https://github.com/jbossas/eap-cloud-galleon-pack) apply to EAP XP.

In addition this feature-pack defines:

# Microprofile config

Add a config map as the source of configuration

## Environment variables

[Environment variables.](https://github.com/wildfly/wildfly-cekit-modules/blob/main/jboss/container/wildfly/launch/mp-config/module.yaml)