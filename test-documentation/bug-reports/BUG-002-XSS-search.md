# BUG-002: Выполнение JavaScript-кода через поле поиска

## Summary

В поле поиска товара возможно выполнение JavaScript-кода в браузере.

## Environment

- OWASP Juice Shop 20.1.1
- Windows 11
- Google Chrome

## Steps to reproduce

1. Открыть главную страницу приложения.
2. Открыть строку поиска.
3. Ввести:

   `<iframe src="javascript:alert('xss')">`

4. Нажать Enter.

## Actual result

В браузере выполняется JavaScript-код и появляется всплывающее окно с текстом «xss».

## Expected result

Введённые данные отображаются как обычный текст либо отклоняются. JavaScript-код не выполняется.

## Severity/Priority

- **Severity:** Critical
- **Priority:** High
