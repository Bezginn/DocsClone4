##################################################################################
**Зміна статусу контрагента-партнера (статус: відправлено запрошення)**
##################################################################################

Для роботи з цим методом користувач повинен бути `авторизованим <https://wiki.edi-n.com/uk/latest/API_DOCflow/Methods/Authorization.html>`__ .

+----------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+
|                        **Метод запиту**                        |                                               **HTTP POST**                                                |
+================================================================+============================================================================================================+
| **Content-Type**                                               | application/json (тіло запиту/відповіді в json форматі в тілі HTTP запиту)                                 |
+----------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+
| **URL запиту**                                                 | **https://doc.edi-n.com/bdoc/partner/status**                                                              |
+----------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+
| **Параметри, що передаються в URL (разом з адресою методу)**   | В рядку заголовка (Header) "Set-Cookie" обов'язково передається **SID** - токен, отриманий при авторизації |
+----------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+
| **Обов'язкові параметри, що передаються в тілі запиту (json)** | **partnerId**                                                                                              |
+----------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+

**JSON-параметри в тілі HTTP запиту/відповіді**
*******************************************************************

``REQUEST``

В тілі **запиту** передається масив мінімум з одним параметром id контрагента-партнера (**partnerId**)

``RESPONSE``

У **відповідь** передається код сервера 200 (ok)

--------------

**Приклади**
*****************

Приклад тіла **запиту** (json):

.. code:: ruby

	[
	  561651651,
	  849494984,
	  9849848
	]

--------------

У **відповідь** передається код сервера 200 (ok)
