#############################################################
**Зміна статусу процесу узгодження**
#############################################################

Для роботи з цим методом користувач повинен бути `авторизованим <https://wiki.edi-n.com/uk/latest/API_DOCflow/Methods/Authorization.html>`__ .

+--------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+
|                       **Метод запиту**                       |                                            **HTTP OPTIONS**                                            |
+==============================================================+========================================================================================================+
| **Content-Type**                                             | application/json (тіло запиту/відповіді в json форматі в тілі HTTP запиту)                             |
+--------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+
| **URL запиту**                                               | **https://doc.edi-n.com/bdoc/agreement_proc**?agreement_proc_id=181&status=2                           |
+--------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+
| **Параметри, що передаються в URL (разом з адресою методу)** | В рядку заголовка (Header) "Set-Cookie" обов'язково передається SID - токен, отриманий при авторизації |
|                                                              |                                                                                                        |
|                                                              | **Обов'язкові url-параметри:**                                                      |
|                                                              |                                                                                                        |
|                                                              | **agreement_proc_id** - ID процесу узгодження                                                          |
|                                                              |                                                                                                        |
|                                                              | **status** - статус (активний = 1, заблокований = 2)                                                   |
|                                                              |                                                                                                        |
+--------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+

**JSON-параметри в тілі HTTP запиту/відповіді**
*******************************************************************

``REQUEST``

В цьому методі json-тіло **запиту** відсутнє (інші дані передавати не потрібно).

``RESPONSE``

У **відповідь** передається код сервера 200 (ok).

--------------

**Приклади**
*****************

**При використанні методу json-тіло запиту відсутнє (дані передавати не потрібно)**

--------------

У **відповідь** передається код сервера 200 (ok).