# BUG-001: Обход авторизации с помощью SQL-инъекции

## Summary

Пользователь может обойти авторизацию и войти в учётную запись администратора с помощью SQL-инъекции в поле Email.

## Environment

- OWASP Juice Shop 20.1.1
- Windows 11
- Google Chrome

## Steps to reproduce

1. Открыть страницу авторизации.
2. В поле Email ввести `' or 1=1--`.
3. В поле Password ввести любой непустой пароль.
4. Нажать кнопку «Log in».

## Actual result

Авторизация успешно выполняется под учётной записью администратора.

## Expected result

Авторизация не выполняется. Отображается сообщение «Invalid email or password.».

## Severity/Priority

- **Severity:** Critical
- **Priority:** High
