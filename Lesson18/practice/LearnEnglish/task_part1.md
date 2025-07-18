# Техническое задание: Консольное приложение "Обучение английскому языку"

---

### 1. Общие сведения

* **Название приложения:** "Английский для новичков"
* **Тип приложения:** Консольное (без графического интерфейса)
* **Цель:** Предоставить пользователю простой инструмент для изучения английских слов и фраз через повторение и проверку знаний.
* **Целевая аудитория:** Новички в программировании Python и начинающие изучать английский язык.
* **Используемые технологии:** Python, SQLite.

---

### 2. Функциональные требования

Приложение должно выполнять следующие функции:

#### 2.1. Управление словами

* **Добавление слова:** Пользователь должен иметь возможность добавить новое английское слово и его перевод на русский язык в базу данных.
* **Просмотр слов:** Пользователь должен иметь возможность просмотреть список всех добавленных слов (английское слово - русский перевод).
* **Удаление слова:** Пользователь должен иметь возможность удалить слово из базы данных по его английскому эквиваленту.

#### 2.2. Режим обучения (тест)

* **Начало теста:** Пользователь выбирает начать тест.
* **Вывод слова:** Приложение случайным образом выбирает английское слово из базы данных и выводит его на экран.
* **Ввод перевода:** Пользователь вводит свой вариант перевода слова.
* **Проверка:** Приложение проверяет правильность перевода.
    * Если перевод **правильный**: выводится сообщение о правильности.
    * Если перевод **неправильный**: выводится сообщение о неправильности и правильный перевод.
* **Завершение теста:** Тест продолжается до тех пор, пока пользователь не решит его остановить.

#### 2.3. Основное меню

При запуске приложения пользователь должен видеть главное меню со следующими опциями:

1.  **Добавить слово**
2.  **Посмотреть слова**
3.  **Удалить слово**
4.  **Начать тест**
5.  **Выход**

---

### 3. Технические требования

* **Язык программирования:** Python 3.x
* **База данных:** SQLite (использовать встроенный модуль `sqlite3`).
* **Структура БД:**
    * Таблица: `words`
    * Колонки:
        * `id` 
        * `english_word`
        * `russian_translation` 
* **Взаимодействие с пользователем:** Через стандартный ввод/вывод (функции `input()` и `print()`).
* **Обработка ошибок:** Должна быть минимальная обработка ошибок, например, при некорректном вводе в меню или попытке добавить существующее слово.

---

### 4. Ход выполнения

1.  **Инициализация БД:** При первом запуске приложения должна создаваться база данных `vocabulary.db` и таблица `words`, если они еще не существуют.
2.  **Реализация функций БД:**
    * Функция для добавления записи.
    * Функция для получения всех записей.
    * Функция для удаления записи.
    * Функция для получения случайного слова.
3.  **Реализация логики меню:**
    * Цикл для отображения меню и обработки выбора пользователя.
    * Вызов соответствующих функций в зависимости от выбора.
4.  **Реализация режима теста:**
    * Цикл, который случайным образом выбирает слова, запрашивает перевод и проверяет его.
    * Возможность выйти из теста.

---

### 5. Дополнительно (если останется время)

* Подсчет статистики в тесте (количество правильных/неправильных ответов за сессию).
* Возможность редактировать существующие слова.