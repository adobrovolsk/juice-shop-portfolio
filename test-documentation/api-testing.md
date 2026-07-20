# Результаты тестирования API

## Environment

- OWASP Juice Shop 20.1.1
- Postman
- Windows 11

| ID | Метод | Endpoint | Проверка | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| API-001 | GET | `/rest/products/search?q=` | Получение списка товаров | Статус `200`, в ответе возвращается список товаров | Получен статус `200`, в body возвращён список товаров | Passed |
| API-002 | GET | `/rest/products/search?q=apple` | Поиск товаров по части названия | Статус `200`, возвращаются товары, содержащие `apple` в названии | Получен статус `200`, найдены `Apple Juice`, `Apple Pomace` и `Pineapple Juice` | Passed |
| API-003 | POST | `/rest/user/login` | Авторизация с неверными данными | Статус `401`, авторизация не выполняется | Получен статус `401` и сообщение `Invalid email or password.`, авторизация не выполнена | Passed |
