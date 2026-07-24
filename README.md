# Python Selenium Autotests

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Pytest](https://img.shields.io/badge/Pytest-tested-green)
![Selenium](https://img.shields.io/badge/Selenium-4.x-brightgreen)
![GitHub Actions](https://img.shields.io/badge/CI-GitHub%20Actions-success)

Учебный проект по автоматизации UI-тестирования интернет-магазина с использованием **Python**, **Selenium WebDriver** и **Pytest**.

## Стек

- Python
- Selenium WebDriver
- Pytest
- Page Object Model (POM)
- Allure Report
- GitHub Actions

## Что реализовано

- Page Object Model
- Явные ожидания (Explicit Waits)
- Параметризация тестов
- Фикстуры Pytest
- Проверка позитивных и негативных сценариев
- Запуск тестов на разных языках сайта
- Автоматический запуск тестов через GitHub Actions
- Генерация Allure-отчётов

## Структура проекта

```
pages/          # Page Objects
tests/          # UI-тесты
conftest.py     # фикстуры Pytest
pytest.ini      # настройки Pytest
requirements.txt
```

## Установка

```bash
git clone https://github.com/kate-belova/python_selenium_autotests.git
cd python_selenium_autotests

python -m venv .venv

# Windows
.venv\Scripts\activate

# Linux/macOS
source .venv/bin/activate

uv sync
```

## Запуск тестов

Все тесты:

```bash
pytest
```

По маркеру:

```bash
pytest -m smoke
pytest -m regression
```

Запуск в браузере Chrome:

```bash
pytest --browser_name=chrome
```

Запуск на другом языке сайта:

```bash
pytest --language=fr
```

## Отчёт Allure

```bash
allure serve allure-results
```

## CI

При каждом push и pull request тесты автоматически запускаются в GitHub Actions.
