# Building an EAP XP server for the Cloud

In order to provision an EAP XP server for the Cloud, you have first to integrate the [EAP Maven plugin](https://github.com/jbossas/eap-maven-plugin/)
into the pom.xml file of your project.

The "package" goal of the plugin allows you to:

* Provision an EAP XP server tailored to your needs.
* Incorporate custom content (keystores, properties files, ...).
* Execute CLI scripts to configure the EAP XP server.
* Deploy your application in the provisioned server.

The generated server is then ready to be installed inside a Docker Image to be deployed in your cluster.

# Provisioning with the cloud feature-pack

The cloud feature-pack is to be provisioned along with the EAP XP Galleon feature-pack. This is configured in the ``feature-packs`` configuration option 
of the EAP Maven plugin.

For example:

```xml
<feature-packs>
  <feature-pack>
    <location>org.jboss.eap.xp:wildfly-galleon-pack</location>
  </feature-pack>
  <feature-pack>
    <location>org.jboss.eap.xp.cloud:eap-xp-cloud-galleon-pack</location>
  </feature-pack>
</feature-packs>
```

# Specifics of the eap-xp-cloud-galleon-pack

When using the cloud galleon feature-pack, the following content will get provisioned:
* Server [startup scripts](launch.md).
* [Automatic adjustment](layers.md) of EAP XP Galleon layers to cope with the cloud execution environment.
* Automatic provisioning of the health subsystem allowing for server state monitoring (Liveness and Readiness probes).
* Automatic routing of server logs to the console