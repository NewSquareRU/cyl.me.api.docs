﻿Categories
==========

Categories list
---------------

/categories/

+------------+------------+
| method     | GET        |
+------------+------------+


Response

+-------------------+------------+---------------------------+
| Parameter         | Type       | Description               |
+===================+============+===========================+
| categories        | array      |                           |
+-------------------+------------+---------------------------+
| Nested in *categories*                                     |
+-------------------+------------+---------------------------+
| category_id       | integer    | Category Id               |
+-------------------+------------+---------------------------+
| name              | string     | Category name             |
+-------------------+------------+---------------------------+

.. code-block:: json

    {
      "status": "ok",
      "response":
        {
            "categories": [
                {
                    "category_id": 1,
                    "name": "Настольные игры"
                },
                {
                    "category_id": 2,
                    "name": "Немецкий язык"
                },
            ]
        }
    }
