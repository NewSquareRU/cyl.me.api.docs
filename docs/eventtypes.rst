﻿Event types
===========

Point types list
----------------

/eventtypes/

+------------+------------+
| method     | GET        |
+------------+------------+

Response

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| event_types       | integer    | Id                        |
+-------------------+------------+---------------------------+
| Nested in *event_types*                                    |
+-------------------+------------+---------------------------+
| event_type_id     | integer    | Event type Id             |
+-------------------+------------+---------------------------+
| name              | string     | Event type name           |
+-------------------+------------+---------------------------+

.. code-block:: json

    {
      "status": "ok",
      "response":
        {
            "event_types": [
                {
                    "event_type_id": 1,
                    "name": "Выставка"
                },
                {
                    "event_type_id": 2,
                    "name": "Вечеринка"
                },
            ]
        }
    }

