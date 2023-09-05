Requests Restish Auth
=====================

This package lets you shell-out to `restish`_ for negotiating a bearer token
with an OIDC provider, and use that token for authenticating requests.

.. _restish: https://rest.sh


Installation
------------

::

    pip install requests-restish-auth

Usage
-----

.. code-block:: python

    import requests
    from restish_auth import RestishAuth

    auth = RestishAuth("my-restish-api-name")
    response = requests.get("https://my-api-endpoint.com/", auth=auth)

Changelog
---------

* 0.3 (2023-09-05): Compatibility with Restish 0.18's new config location. For
  older versions of restish, use previous versions of
  ``requests-restish-auth``.

* 0.2 (2022-09-16): Load token lazily.

* 0.1 (2022-09-14): Initial version.
