Cyl.me API documentation
========================


API for

All responses emitted in JSON format
API implements HATEOAS
In all requests when authorization needed token must be provided
Authorization between applications must be implemented using tokens


+----------------------------------+-------------------------------------------+
| successful answer                | status: ok                                |
|                                  | response: data                            |
+----------------------------------+-------------------------------------------+
| conditionally successful answer  | status: ok                                |
|                                  | response: { error : "error description" } |
+----------------------------------+-------------------------------------------+
| unsuccessful response answer     | status: notOk                             |
|                                  | error: "error description"                |
+----------------------------------+-------------------------------------------+

All answers are successful except following cases: invalid token, error occurred
 internally in API (for example:database error)

Contents
--------

.. toctree::
   :maxdepth: 2
   
   points
   users
   token


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
