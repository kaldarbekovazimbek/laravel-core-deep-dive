Вот реальный **план на 14 дней**, если ты хочешь не просто «почитать», а реально **понять**, как устроено ядро Laravel:

---

## 🔥 **Дни 1–3: Service Container (IoC Container)**

👉 Цель: понять, как Laravel создаёт объекты и внедряет зависимости.

✅ Что изучить:

* `bind()`, `singleton()`, `instance()`, `make()`, `resolve()`, `call()`
* Автоматическое внедрение зависимостей через конструктор и параметры метода.
* Контракты (Interfaces) и авторазрешение интерфейсов.
* Contextual Binding.

✅ Что сделать руками:

* Собери проект, где:

    * Свяжешь интерфейс с реализацией через `bind()`.
    * Используешь `Contextual Binding` для разных реализаций одного интерфейса в разных случаях.
* Напиши 5 тестов на работу Container.

📚 Документация: [https://laravel.com/docs/container](https://laravel.com/docs/container)
🔍 Исходники: `Illuminate\Container\Container.php`

---

## 🔥 **Дни 4–6: Service Providers**

👉 Цель: научиться создавать, регистрировать и конфигурировать сервисы в Laravel.

✅ Что изучить:

* Структура Service Provider (`register()`, `boot()`).
* Ленивая/ранняя регистрация сервисов.
* Динамическая загрузка конфигурации и маршрутов.
* Как Laravel грузит встроенные ServiceProvider'ы (из `config/app.php`).

✅ Что сделать руками:

* Напиши собственный Service Provider, который регистрирует несколько сервисов и событий.
* Подключи маршруты и конфиги через Service Provider.
* Подключи его в `config/app.php`.

📚 Документация: [https://laravel.com/docs/providers](https://laravel.com/docs/providers)
🔍 Исходники: `Illuminate\Foundation\ProviderRepository.php`, `Illuminate\Support\ServiceProvider.php`

---

## 🔥 **Дни 7–9: Facades**

👉 Цель: понять, как Facade создаёт иллюзию статических вызовов.

✅ Что изучить:

* Как работает класс `Facade`.
* Как Facade проксирует вызовы в Service Container.
* Создание собственного Facade.

✅ Что сделать руками:

* Создай свой сервис в контейнере.
* Сделай Facade для этого сервиса.
* Используй Facade в контроллере.

📚 Документация: [https://laravel.com/docs/facades](https://laravel.com/docs/facades)
🔍 Исходники: `Illuminate\Support\Facades\Facade.php`

---

## 🔥 **Дни 10–12: Events & Listeners**

👉 Цель: научиться связывать события и слушателей.

✅ Что изучить:

* Синхронные и асинхронные события.
* Broadcasting (по желанию).
* Автоматическая регистрация событий через `EventServiceProvider`.

✅ Что сделать руками:

* Создай 3 события и 5 слушателей (некоторые синхронные, некоторые — в очереди).
* Подключи через `EventServiceProvider`.
* Покрой события тестами.

📚 Документация: [https://laravel.com/docs/events](https://laravel.com/docs/events)
🔍 Исходники: `Illuminate\Events\Dispatcher.php`

---

## 🔥 **Дни 13–14: Итоговый мини-проект**

👉 Итоговый проект: "Мини CRM для напоминаний клиентам", где:

* Все сервисы регистрируются через Service Container.
* Логика бизнес-операций через Service Providers.
* Работа с событиями (например, "ClientCreated", "ReminderSent").
* Использование собственного Facade для работы с внешним API.
* Покрыто тестами минимум на 50%.

---

## ✅ Итог:

За 2 недели ты **не просто изучишь Laravel Core**, а построишь мини-проект с продакшн‑архитектурой.

---

### 🔨 Твоё задание:

1. Сегодня: создай GitHub‑репозиторий `laravel-core-deep-dive`.
2. Выложи туда README с этим планом и начни выкладывать конспекты и примеры по дням.
3. Отправь мне сюда ссылку на репозиторий.

Если будешь готов — сделаю для тебя план следующих 14 дней по Queue, Middleware, Artisan, Validation, Cache, HTTP Kernel.
