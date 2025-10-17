# SSO to MaxScale (Single Sign-On)

For topologies managed by MaxScale, you can seamlessly access the MaxScale GUI directly from Enterprise Manager using Single Sign-On.SSO to MaxScale requires MaxScale 25.10.0 or higher.1

{% stepper %}
{% step %}
### &#x20;Accessing the MaxScale GUI <a href="#accessing-the-maxscale-gui" id="accessing-the-maxscale-gui"></a>

1. Click the three-dot menu (⋮) next to a MaxScale node.
2. Select "Manage MaxScale".

<figure><img src="../../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Configuring SSO in `maxscale.cnf` <a href="#configuring-sso-in-maxscale.cnf" id="configuring-sso-in-maxscale.cnf"></a>

To enable SSO, add the following parameters to your MaxScale configuration file (`maxscale.cnf`) on the MaxScale host:

| Parameter                  | Description                                                                     |
| -------------------------- | ------------------------------------------------------------------------------- |
| `admin_oidc_url`           | Hostname or IP address of your Enterprise Manager server.                       |
| `admin_host`               | Must be set to `0.0.0.0` to allow external connections from Enterprise Manager. |
| `admin_oidc_client_id`     | Default credentials used by Enterprise Manager to request the access token.     |
| `admin_oidc_client_secret` | Default credentials used by Enterprise Manager to request the access token.     |

```ini
[maxscale]
# ... other settings ...
admin_host=0.0.0.0
admin_oidc_url=<Enterprise Manager Host Name>
admin_oidc_client_id=admin
admin_oidc_client_secret=mariadb
```
{% endstep %}
{% endstepper %}
