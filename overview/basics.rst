##########
API Basics
##########

The API allows customers to access 

Typical Workflow
================



Authentication and Scopes
=========================

The CORE API requires the use of 3-legged OAuth2 tokens. See the `OAuth documentation </en/docs/oauth/v2>`_ for more information on authentication, obtaining a bearer token, and scopes.

HTTP GET requests to the API require the ``data:read`` scope.
HTTP POST, PUT, DELETE requests to the API require the ``data:write`` scope.
