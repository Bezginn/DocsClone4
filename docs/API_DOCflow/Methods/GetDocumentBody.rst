#############################################################
**Отримання тіла документа**
#############################################################

Для роботи з цим методом користувач повинен бути `авторизованим <https://wiki.edi-n.com/uk/latest/API_DOCflow/Methods/Authorization.html>`__ .

+--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+
|                       **Метод запиту**                       |                                                **HTTP GET**                                                |
+==============================================================+============================================================================================================+
| **Content-Type**                                             | application/json (тіло запиту/відповіді в json форматі в тілі HTTP запиту)                                 |
+--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+
| **URL запиту**                                               | **https://doc.edi-n.com/bdoc/store/package/document/body**?package_id=58&document_id=53&body_id=53         |
+--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+
| **Параметри, що передаються в URL (разом з адресою методу)** | В рядку заголовка (Header) "Set-Cookie" обов'язково передається **SID** - токен, отриманий при авторизації |
|                                                              |                                                                                                            |
|                                                              | **Обов'язкові url-параметри:**                                                                             |
|                                                              |                                                                                                            |
|                                                              | **package_id** - ID комплекту документів                                                                   |
|                                                              |                                                                                                            |
|                                                              | **document_id** - ID документа                                                                             |
|                                                              |                                                                                                            |
|                                                              | **body_id** - ID тіла документа                                                                            |
+--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+

**JSON-параметри в тілі HTTP запиту/відповіді**
*******************************************************************

``REQUEST``

В цьому методі json-тіло **запиту** відсутнє (інші дані передавати не потрібно).

``RESPONSE``

У **відповідь** передається документ в вигляді набору байт.

--------------

**Приклади**
*****************

**При використанні методу json-тіло запиту відсутнє (дані передавати не потрібно)**

--------------

У **відповідь** передається документ в вигляді набору байт.


