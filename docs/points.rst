Points
======

Points list
-----------

/points/

Response

+------------+------------+-----------------+
| Parameter  | Type       | Description     |
+============+============+=================+
| points     | integer    | Id              |
+------------+------------+-----------------+
| Nested in points(look point's info)       |
+------------+------------+-----------------+

HATEOAS

+---------------------------------+-----------------------+
| /point/?page=1..10              | Link to next data set |
+---------------------------------+-----------------------+


Point's information
-------------------

/points/{point_id}/

+------------+------------+
| method     | GET        |
+------------+------------+
| Auth       | NO         |
+------------+------------+


Parameters

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| point_id          | integer    | Point's ID                |
+-------------------+------------+---------------------------+

.. _point-information:

Response

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| id                | integer    | Id                        |
+-------------------+------------+---------------------------+
| user_id           | integer    | User Id                   |
+-------------------+------------+---------------------------+
| lat               | float      | Latitude                  |
+-------------------+------------+---------------------------+
| lng               | float      | Longitude                 |
+-------------------+------------+---------------------------+
| address           | string     | Address                   |
+-------------------+------------+---------------------------+


New point
---------

/points/

+------------+------------+
| method     | POST       |
+------------+------------+
| Auth       | YES        |
+------------+------------+


Input vars

+-------------------+------------+------------+---------------------------+
| Parameter         | Required   | Type       | Description               |
+===================+============+============+===========================+
| lat               | *          | float      | Latitude                  |
+-------------------+------------+------------+---------------------------+
| lng               | *          | float      | Longitude                 |
+-------------------+------------+------------+---------------------------+
| address           | *          | string     | Address                   |
+-------------------+------------+------------+---------------------------+

Response

+-------------------+------------+-----------------------------+
| Parameter         | Type       | Description                 |
+===================+============+=============================+
| id                | integer    | Id newly added point        |
+-------------------+------------+-----------------------------+



Edit point
----------

/points/{point_id}/

+------------+------------+
| method     | PUT        |
+------------+------------+
| Auth       | YES        |
+------------+------------+


Input vars

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| Look point-information_ input vars                         |
+-------------------+------------+---------------------------+


Parameters

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| point_id          | integer    | Point's ID                |
+-------------------+------------+---------------------------+

Response

+-------------------+------------+-----------------------------+
| Parameter         | Type       | Description                 |
+===================+============+=============================+
| result            | 1                                        |
+-------------------+------------+-----------------------------+


Remove point
------------

/points/{point_id}/

+------------+------------+
| method     | DELETE     |
+------------+------------+
| Auth       | YES        |
+------------+------------+

Parameters

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| point_id          | integer    | Point's ID                |
+-------------------+------------+---------------------------+

Response

+-------------------+------------+-----------------------------+
| Parameter         | Type       | Description                 |
+===================+============+=============================+
| result            | 1                                        |
+-------------------+------------+-----------------------------+



Add comment
-----------

/points/{point_id}/comments/

+------------+------------+
| method     | POST       |
+------------+------------+
| Auth       | YES        |
+------------+------------+

Parameters

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| point_id          | integer    | Point's ID                |
+-------------------+------------+---------------------------+


Input vars

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| user_id           | integer    | User Id                   |
+-------------------+------------+---------------------------+
| comment           | string     | Comment                   |
+-------------------+------------+---------------------------+

Response

+-------------------+------------+-----------------------------+
| Parameter         | Type       | Description                 |
+===================+============+=============================+
| result            | 1                                        |
+-------------------+------------+-----------------------------+



Add like
--------

/points/{point_id}/likes/

+------------+------------+
| method     | POST       |
+------------+------------+
| Auth       | YES        |
+------------+------------+

Parameters

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| point_id          | integer    | Point's ID                |
+-------------------+------------+---------------------------+


Input vars

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| user_id           | integer    | User Id                   |
+-------------------+------------+---------------------------+

Response

+-------------------+------------+-----------------------------+
| Parameter         | Type       | Description                 |
+===================+============+=============================+
| result            | 1                                        |
+-------------------+------------+-----------------------------+



Remove like
-----------

/points/{point_id}/likes/

+------------+------------+
| method     | DELETE     |
+------------+------------+
| Auth       | YES        |
+------------+------------+

Parameters

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| point_id          | integer    | Point's ID                |
+-------------------+------------+---------------------------+


Input vars

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| user_id           | integer    | User Id                   |
+-------------------+------------+---------------------------+


Add point to favourite
----------------------

Coming soon...
