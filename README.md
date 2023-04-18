# spermum_education

# Описание проекта
Данный проект представляет собой систему для ведения образовательной деятельности в группе. Пользователи вступают в группу и получают возможность решать тесты от учителей, которые они могут составить сами или взять готовый. Для учителя будет предоставляться статистика решения составленного теста. Управление позволит переключаться пользователю между группами, что позволит не создавать несколько аккаунтов. Особенностью является чат, в котором и появляются задания.

# Техническое задание
1. Создать базу данных на основе ORM sqlalchemy с таблицами: USERS, GROUPS, USERS_TO_GROUP, MESSAGES, WORKS, WORKS_RESULTS
2. Создание REST-API для моделей GROUPS, WORKS, WORKS_RESULTS
3. `/register` Регистрация пользователей в системе (ученик/учитель)
4. `/profile/<int:user_id>` Просмотр профилей пользователей и изменение своего
5. `/profile` редирект на пункт 4
6. `/chat` По сути основная страница с возможностью взаимодействовать со всеми группами
7. `/works` Для ученика: Список тестов к выполнению. Для учителя: Статистика по всем тестам
8. `/works/<int:work_id>` Для учителя: Статистика выполнения теста учениками. Для ученика: Меню теста (возможность начать прохождение)
9. `/works/completing/<int:work_id>` Прохождение теста для учеников
10. `/works/results/<int:work_id>` Результат прохождения теста учеником
11. `/works/creating` Создание учителем нового теста
12. `/groups` Для учителя: взаимодействие со всеми группами
12. `/groups/<int:group_id>` Для учителя: взаимодействие с группой
13. `/groups/creating` Для учителя: создание новой группы

# Пояснительная записка
### Название проекта 
Портал для ведения образовательной деятельности
### Авторы проекта 
[Карнажицкий Максим Романович](https://github.com/xtern0o), [Мерескин Евгений Дмитриевич](https://github.com/b1tka)
### Описание идеи: 
Идея проекта заключается в создании универсального сервиса для ведения образовательной деятельности. Наш сервис обладает интуитивно понятным управлением и предоставляет возможность учителям самостоятельно создавать тесты для учеников.
Учителя могут создавать группы, в которых ученики смогут задавать вопросы, общаться и получать уведомления о новых тестах, которые создают учителя.
Также учителя контроллировать процесс процесс прохождения тестов и анализировать результаты для более объективной оценки знаний учеников.
### Описание реализации
#### церф

#### Таблица `users`
- Таблица `users` связана с таблицей `groups` связью many-to-many через вспомогательные таблицы `users_to_groups` и `users_to_invites_to_groups`
> В этой таблице хранятся данные о пользователях
#### Таблица `groups`
- Таблица `groups` связана с таблицей `works` связью many-to-many через вспомогательную таблицу `works_to_groups`
> Таблица используется для объединенния пользователей в группу, в которой участники разделяются на учителя и учеников
#### Таблица `messages`
- Таблица `messages` связана с таблицами `users` и `groups` связями one-to-many
> Таблица используется для хранения истории сообщений между пользователями
#### Таблица `works`
- Таблица `works` связана с таблицей `groups` связью many-to-many через вспомогательную таблицу `works_to_groups`
> Таблица используется для хранения тестов
#### Структура
![image](https://user-images.githubusercontent.com/78041040/232835333-4f6f7168-6f1c-4253-bb80-04d810658386.png)
#### [Структура сайта страницы роуты роуминг самый быстрый мобильный мегафон теле йота](https://miro.com/app/board/uXjVMVAiSic=/?share_link_id=654705494043)
### Описание технологий
Flask, socketio, sqlalchemy, random, datetime, python, pycharm, windows10, x86, x64, lenovo ideapad, microsoft mouse мышка)🐁🐁🐁🦇), гтхаб, гуглъхром, дбШема, все, коммит, склайт студио, "тач" бар, бустрап, аштимель), кээсэс, джава скрит, телеграм), гугл табли)

# Презентация (пока черновик)))
![image](https://user-images.githubusercontent.com/78041040/232845802-d53f455a-546e-48f8-92eb-ec21dcd03a34.png)

