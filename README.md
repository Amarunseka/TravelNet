# 🌍 TravelNet — Социальная сеть для путешественников

## 📌 Нефункциональные требования

### 🔒 Надёжность
- Доступность системы: **99.9%**
- Развёртывание: на **нескольких территориально распределённых серверах**
- База данных:
  - Поддержка **автоматической репликации**
- Обязательные компоненты:
  - **Мониторинг** и **алертинг**
  - **Система аудита**
  - **Балансировка нагрузки** на все узлы системы

### 🚀 Масштабируемость
- Поддержка **горизонтального масштабирования** при росте количества пользователей
- Возможность расширения как для **веб**, так и для **мобильных клиентов**

### ⚡ Производительность
- Подход: **Low-latency UI**
- Архитектура с прицелом на **высокую долю операций чтения (High Read/Write ratio)**

### 🔐 Безопасность
- Работа только по протоколу **HTTPS**
- **Модуль авторизации**
- **Личный кабинет пользователя** с разграничением доступа

---

## ✅ Функциональные требования

- 📱 Просмотр ленты постов (`GET`)
- 🔍 Просмотр отдельного поста (`GET`)
- ✍️ Размещение / редактирование / удаление постов (`POST/DELETE`)
- 💬 Комментарии и лайки (`POST`)
- ❤️ Подписка на любимые направления и авторов (`POST/DELETE`)
- 🔎 Поиск и фильтрация по различным параметрам (`GET`)

---

## 📈 Расчёт нагрузки

> При 10 000 000 активных пользователей в день  
> И в среднем **5 действий на пользователя**  
> Общая нагрузка ≈ **580 RPS**

| Подсистема                                 | Доля нагрузки | Примерная RPS |
|--------------------------------------------|---------------|----------------|
| 📱 Просмотр ленты постов                   | 40%           | ~232 RPS       |
| 🔍 Просмотр отдельного поста               | 20%           | ~116 RPS       |
| ✍️ Размещение / редактирование / удаление  | 5%            | ~29 RPS        |
| 💬 Комментарии и лайки                     | 20%           | ~116 RPS       |
| ❤️ Подписки                                | 5%            | ~29 RPS        |
| 🔎 Поиск и фильтрация                      | 10%           | ~58 RPS        |

---

## 🧠 Примечание

> Цифры округлены для предварительного планирования.  
> При проектировании необходимо учитывать **нагрузочные пики**, **автоматическое масштабирование**, и **резервные мощности**.

---
