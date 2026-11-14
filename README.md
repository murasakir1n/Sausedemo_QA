# 🧪 QA Portfolio: Тестирование интернет-магазина SauceDemo

Репозиторий содержит примеры тестовой документации, созданной в рамках ручного функционального и UI-тестирования учебного веб-приложения [SauceDemo](https://saucedemo.com).

---

## 🛠 Окружение и инструменты
* **Объект тестирования:** Web-приложение Swag Labs (`saucedemo.com`)
* **ОС и браузер:** macOS 26.6.2, Google Chrome 157
* **Формат документации:** Markdown
* **Инструменты:** Chrome DevTools, Git / GitHub

---

## 📂 Структура репозитория

```text
Sausedemo_QA/
├── manual_testing/
│   ├── bug-reports/      # Отчеты о найденных дефектах (8 шт.)
│   │   └── attachments/  # Скриншоты и видеозаписи воспроизведения
│   ├── checklists/       # Чек-листы для проверки основных модулей (3 шт.)
│   └── test-cases/       # Подробные тест-кейсы (4 шт.)
└── README.md
```

---

## ✅ Чек-листы (Checklists)
Проверки разделены по функциональным модулям и покрывают все доступные роли пользователей (`standard_user`, `problem_user`, `performance_glitch_user`, `error_user`, `visual_user`).

| Модуль | Описание проверок | Файл |
| :--- | :--- | :--- |
| **Авторизация (Login)** | Валидация полей, вход под разными ролями, сообщения об ошибках | [checklist-login.md](manual_testing/checklists/checklist-login.md) |
| **Каталог (Catalog)** | Отображение карточек, сортировка, переход в товар, UI-элементы | [checklist-catalog.md](manual_testing/checklists/checklist-catalog.md) |
| **Корзина (Cart)** | Добавление и удаление товаров, счетчик корзины, переход к оплате | [checklist-cart.md](manual_testing/checklists/checklist-cart.md) |

---

## 📋 Тест-кейсы (Test Cases)
Примеры детально проработанных сценариев (позитивных и негативных) с шагами, тестовыми данными и постусловиями.

| ID | Название сценария | Тип | Статус | Файл |
| :--- | :--- | :--- | :--- | :--- |
| **TC-01** | Успешное оформление заказа. | Positive | `Pass` | [tc-01.md](manual_testing/test-cases/tc-01.md) |
| **TC-02** | Сортировка товаров в каталоге по возрастанию цены | Positive | `Pass` | [tc-02.md](manual_testing/test-cases/tc-02.md) |
| **TC-03** | Оформление заказа с пустым обязательным полем Zip/Postal Code | Negative | `Pass` | [tc-03.md](manual_testing/test-cases/tc-03.md) |
| **TC-04** | Проверка карточки товара на соответствие с товаром из каталога. | Positive | `Fail` | [tc-04.md](manual_testing/test-cases/tc-04.md) |

---

## 🐞 Баг-репорты (Bug Reports)
В ходе тестирования было выявлено **8 дефектов** различной серьезности. Каждый отчет снабжен шагами воспроизведения, ожидаемым/фактическим результатом и медиафайлами (скриншотами или видео `.mp4`).

| ID | Заголовок дефекта | Роль пользователя | Файл |
| :--- | :--- | :--- | :--- |
| **BUG-01** | Длительная задержка при авторизации в системе | `performance_glitch_user` | [bug-01-slow-login.md](manual_testing/bug-reports/bug-01-slow-login.md) |
| **BUG-02** | Кнопка Remove не работает | `problem_user`/`error_user` | [bug-02-remove-not-working.md](manual_testing/bug-reports/bug-02-remove-not-working.md) |
| **BUG-03** | Цена в корзине не совпадают с каталогом. | `visual_user` | [bug-03-catalog-cart-mismatch.md](manual_testing/bug-reports/bug-03-catalog-cart-mismatch.md) |
| **BUG-04** | Не меняется порядок товаров при выборе сортировки в каталоге у problem_user и error_user. | `problem_user` / `error_user` | [bug-04-sort-incorrect-work.md](manual_testing/bug-reports/bug-04-sort-incorrect-work.md) |
| **BUG-05** | Переход в карточку товара открывает не тот товар. | `problem_user` | [bug-05-product-title-error.md](manual_testing/bug-reports/bug-05-product-title-error.md) |
| **BUG-06** | Картинка товара не соответствует названию товара. | `problem_user` / `visual_user` | [bug-06-product-image-mismatch.md](manual_testing/bug-reports/bug-06-product-image-mismatch.md) |
| **BUG-07** | Кнопки не выровнены. | `visual_user` | [bug-07-buttons-not-aligned.md](manual_testing/bug-reports/bug-07-buttons-not-aligned.md) |
| **BUG-08** | Иконка корзины не на нужном месте. | `visual_user` | [bug-08-cart-not-in-place.md](manual_testing/bug-reports/bug-08-cart-not-in-place.md) |
