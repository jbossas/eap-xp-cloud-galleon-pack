# Galleon layers defined by the XP cloud feature-pack

## cloud-default-mp-config

A layer that allows to provision the configuration that used to be present in the default server located in EAP XP 4 s2i builder image.

NB: When provisioning this layer, all the server JBoss Modules modules, even not in use by the server configuration, are installed.

# WildFly Galleon layers adjusted by the cloud feature-pack

All the [adjustments](https://github.com/jbossas/eap-cloud-galleon-pack/blob/main/doc/layers.md) defined in the [EAP cloud galleon pack](https://github.com/jbossas/eap-cloud-galleon-pack) apply to EAP XP.
