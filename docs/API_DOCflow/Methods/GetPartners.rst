#############################################################
**Отримання списку партнерів-контрагентів**
#############################################################

Для роботи з цим методом користувач повинен бути `авторизованим <https://wiki.edi-n.com/uk/latest/API_DOCflow/Methods/Authorization.html>`__ .

+--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+
|                       **Метод запиту**                       |                                                **HTTP GET**                                                |
+==============================================================+============================================================================================================+
| **Content-Type**                                             | application/json (тіло запиту/відповіді в json форматі в тілі HTTP запиту)                                 |
+--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+
| **URL запиту**                                               | https://doc.edi-n.com/bdoc/partners                                                                        |
+--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+
| **Параметри, що передаються в URL (разом з адресою методу)** | В рядку заголовка (Header) "Set-Cookie" обов'язково передається **SID** - токен, отриманий при авторизації |
|                                                              |                                                                                                            |
|                                                              | **Опціональні url-параметри (фільтр)**                                                                     |
|                                                              |                                                                                                            |
|                                                              | **search_pattern** - код ЕДРПОУ *або* назва компанії                                                       |
|                                                              |                                                                                                            |
|                                                              | **limit** - ліміт вибірки (за замовчанням=20)                                                              |
|                                                              |                                                                                                            |
|                                                              | **offset** - зміщення відносно верхньої межі вибірки (за замовчанням=0)                                    |
|                                                              |                                                                                                            |
|                                                              | **is_registered** - відмітка про те, що контрагент зареєстрований на платформі DOCflow; 1 - так, 0 - ні    |
+--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+

**JSON-параметри в тілі HTTP запиту/відповіді**
*******************************************************************

``REQUEST``

В цьому методі json-тіло **запиту** відсутнє (інші дані передавати не потрібно).

``RESPONSE``

Опис json-параметрів **відповіді** метода API (об'єкт **Partner**)

Таблиця 3 - Опис параметрів об'єкта **Partner**

.. csv-table:: 
  :file: for_csv/Partner.csv
  :widths:  1, 12, 41
  :header-rows: 1
  :stub-columns: 0

--------------

**Приклади**
*****************

**При використанні методу json-тіло запиту відсутнє (дані передавати не потрібно)**

--------------

Приклад тіла **відповіді** (json): 

.. code:: ruby

  [
    {
      "partnerId": 762,
      "accountId": 8,
      "code": "3260408077",
      "name": "Arsen",
      "contactPerson": "Arsen contact-person",
      "contactEmail": "007Arsen@gmail.com",
      "contactPhone": "123244",
      "comment": "fdf",
      "invitationDate": 1566223863,
      "status": 2,
      "contractStatus": 0,
      "companyId": 0
    },
    {
      "partnerId": 766,
      "accountId": 8,
      "code": "12345678",
      "name": "Физычна особа",
      "contactEmail": "sahabekfdsov@meta.ua",
      "invitationDate": 1566222958,
      "status": 2,
      "contractStatus": 1,
      "companyId": 6
    },
  ]


