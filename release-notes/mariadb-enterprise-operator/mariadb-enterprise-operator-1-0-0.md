# MariaDB Enterprise Operator 1.0.0

**Release date**: 23 April 2025

We are excited to announce the **General Availability of MariaDB Enterprise Operator 1.0.0** — delivering enterprise-grade automation for managing MariaDB Enterprise workloads on Kubernetes and Red Hat OpenShift.

This first stable release brings all the capabilities of the Community Operator, and extends them with powerful features tailored for enterprise customers, including certified OpenShift support, UBI based images, enhanced TLS security, and official support for MariaDB Enterprise Server and MaxScale Enterprise.

### MariaDB Enterprise Support

Provisioning and lifecycle management of MariaDB Enterprise products:

* MariaDB Enterprise Server 10.5, 10.6 and 11.4
* MaxScale Enterprise 25.01

### Advanced TLS and Security Enhancements

* [Certificate Lifetime Flexibility](https://app.gitbook.com/s/kuTXWg0NDbRx6XUeYpGD/mariadb-enterprise-operator/tls#certificate-lifetime-configuration): Fully configurable certificate validity
* [Customizable Private Key Algorithms](https://app.gitbook.com/s/kuTXWg0NDbRx6XUeYpGD/mariadb-enterprise-operator/tls#private-key-configuration): Support for RSA and ECDSA with configurable key lengths
* [Advanced TLS Modes (Galera Enterprise)](https://app.gitbook.com/s/kuTXWg0NDbRx6XUeYpGD/mariadb-enterprise-operator/tls#galera-enterprise-ssl-modes): Additional TLS enforcement modes exclusive to Enterprise
* Support for configuring multiple [TLS versions](https://app.gitbook.com/s/kuTXWg0NDbRx6XUeYpGD/mariadb-enterprise-operator/tls#tls-version-configuration)

### Certified OpenShift Compatibility

* Officially certified through [Red Hat’s Operator Certification Program](https://connect.redhat.com/en/partner-with-us/red-hat-openshift-certification)
* Joint MariaDB + Red Hat support for OpenShift-related issues
* Listed in the [Red Hat Ecosystem Catalog](https://catalog.redhat.com/software/container-stacks/detail/65789bcbe17f1b31944acb1d)
* Available in the [OpenShift console ](https://app.gitbook.com/s/kuTXWg0NDbRx6XUeYpGD/mariadb-enterprise-operator/mariadb-enterprise-operator-installation/openshift#openshift-console)via the certified catalog

### UBI-Based Images

Docker Images Based on [Red Hat UBI](https://catalog.redhat.com/software/base-images), certified and supported by Red Hat, with the following advantages:

* Immutability: Secure and stable by design, minimizing risks from mutable layers.
* Small size: Uses UBI minimal and micro variants for faster builds, smaller images, and quicker pulls.
* Security and compliance: CVE scanning and patching ensure industry-standard compliance.
* Enterprise-grade support: Maintained and supported by Red Hat for reliable updates and long-term stability.

MariaDB Enterprise Operator 1.0.0 is a major release, providing a secure, scalable, and OpenShift-certified solution to manage MariaDB Enterprise workloads. Refer to the [documentation](https://app.gitbook.com/s/kuTXWg0NDbRx6XUeYpGD/mariadb-enterprise-operator) for detailed information.

The current release has been tested with the following versions:

| Platform/Component        | Version  |
| ------------------------- | -------- |
| Platform/Component        | Version  |
| Kubernetes                | v1.32    |
| OpenShift                 | v4.18.1  |
| MariaDB Enterprise Server | 11.4.5-3 |
| MaxScale Enterprise       | 25.01.2  |

{% @marketo/form formid="4316" formId="4316" %}
