##########
API Basics
##########

The Consumption Reporting (CORE) API allows customers to access their usage collected as part of a Token Flex contract arrangement in order to integrate with their own internal reporting solutions.
By using the CORE API's, a customer can automate internal charge-back reports and build custom reporting solutions specific their individual needs.

Typical Workflow
================



Authentication and Scopes
=========================

The CORE API requires the use of 3-legged OAuth2 tokens. See the `OAuth documentation </en/docs/oauth/v2>`_ for more information on authentication, obtaining a bearer token, and scopes.

HTTP GET requests to the CORE API require the ``data:read`` scope.
HTTP POST, PUT, DELETE requests to the CORE API require the ``data:write`` scope.
