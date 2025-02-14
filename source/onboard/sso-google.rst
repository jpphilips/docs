Google Single Sign-On
=====================

.. include:: ../_static/badges/ent-pro-cloud-selfhosted.rst
  :start-after: :nosearch:

*Available in legacy Mattermost Enterprise Edition E20*

.. include:: common-sso-google.rst
  :start-after: :nosearch:

Configure Mattermost ``config.json`` for Google Apps SSO
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. include:: ../_static/badges/selfhosted-only.rst
  :start-after: :nosearch:

Instead of using the System Console, you can add the Google settings directly to the ``config.json`` file directly on your Mattermost server.

1. Open ``config.json`` as *root* in a text editor. It’s usually in ``/opt/mattermost/config``, but it might be elsewhere on your system.
2. Locate the ``GoogleSettings`` section, then add or update the following information:

.. code-block:: text

  "Enable": true,
        "Secret": "P-k9R-7E7ayX9LdddddWdXVg",
        "Id": "1022ddddd5846-bkddddd4a1ddddd9d88j1kb6eqc.apps.googleusercontent.com",
        "Scope": "profile openid email",
        "AuthEndpoint": "",
        "TokenEndpoint": "",
        "UserApiEndpoint": "",
        "DiscoveryEndpoint": "https://accounts.google.com/.well-known/openid-configuration",
        "ButtonText": "",
        "ButtonColor": ""
  }

3. Save your changes, then restart your Mattermost server. After the server restarts, users must change their login method before they can log in with Google Apps.
