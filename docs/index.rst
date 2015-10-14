Cyl.me API documentation
========================


- All responses emitted in JSON format
- API implements HATEOAS
- In all requests when authorization needed token must be provided
- Authorization between applications must be implemented using tokens
- Tokens have different ttl and scope. We have tokens for admins and tokens for users.

+----------------------------------+-------------------------------------------+
| Answer type                      | Response                                  |
+==================================+===========================================+
| successful answer                | status: ok                                |
|                                  | response: data                            |
+----------------------------------+-------------------------------------------+
| conditionally successful answer  | status: ok                                |
|                                  | response: { error: "error description",   |
|                                  |             code:  "error code" }         |
+----------------------------------+-------------------------------------------+
| unsuccessful response answer     | status: notOk                             |
|                                  | error: "error description"                |
|                                  | code:  "error code"                       |
+----------------------------------+-------------------------------------------+

All answers are successful except following cases: invalid token, error occurred
 internally in API (for example:database error)


Table of error codes

+-----------+--------------------------------------------+
| Code      | Description                                |
+===========+============================================+
| 1         | Token not specified                        |
| 2         | Token invalid                              |
+-----------+--------------------------------------------+


Contents
--------

.. toctree::
   :maxdepth: 2
   
   users
   points
   pointtypes
   tasks
   news
   im
   skills
   categories
   token
   invitations
   eventtype
   votes
   scopes


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
