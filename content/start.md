title=Tamaya in 5 minutes
type=page
status=published
~~~~~~

Tamaya in 5 minutes - a short introduction
------------------------------------------

Apache Tamaya (incubating) provides a flexible and powerful
configuration solution
for Java developers using Java SE as well as for more complex
usage scenarios like cloud or Java EE. It provides a modern
type-safe property based Configuration API combined with a
powerful environment model and a flexible SPI.

Features
--------

* Unified Configuration API
* Pluggable Configuration Backends
* Enforceable Configuration Policies
* Configuration Validation and Documentation
* Seemless Enterprise Integration

Documentation
-------------

* [Use Cases and Requirements](usecases.html)
* [High Level Design](highleveldesign.html)
* [API](api.html)
* [Core](core.html)
* [Extensions](extensions.html)

---

Quickstart
----------

Using Apache Tamaya is simple:

1. Add `{config.tamaya_mvn_group_id}:tamaya-core:${config.tamaya_version}` to your dependencies.
2. Add your config to `META-INF/javaconfiguration.properties`
3. Access your configuration by `ConfigurationProvider.getConfiguration()` and use it.
4. Look at the [extension modules](extensions.html) to customize your setup!
5. Enjoy!


Rationale
---------

Configuration is one of the most prominent cross-cutting concerns similar to logging. Most of us already have been
writing similar code again and again in each of our projects. Sometimes in a similar way but mostly always slightly
different, but certainly with high coupling to your configuration backends. Given your code is reused or integrated
some how, or deployed by some customers, struggling starts: not supported backends, different policies, missing
combination and validation mechanisms and so on. Tamaya solves all this by defining a common API and backend SPI.
Your code is decoupled from the configuration backend. There is no difference if your code is deployed on your dev box
or in a clustered Docker environment in production, it stays the same!
