Роли пользователей
==================

*   **Создатель проекта** - Может создавать проект, может добавлять людей в проект, может создавать задачи, может редактировать задачи, может изменять статус задачи (все права внутри проекта)
    
*   **Член проекта редактор (исполнитель)** - Может просматривать список задач в проект, может просматривать карточку задачи, может редактировать задачи, может изменять статус задачи, может оставлять комментарии в задаче.
    
*   **Член проекта просмотр** - Может просматривать список задач в проект, может просматривать карточку задачи, не может ничего редактировать
    

Любой из пользователей может создавать свой проект.

Любой из пользователей может получить роль “Создатель проекта“, в рамках своего созданного проекта.

USER STORY
==========

*   Я, как пользователь (Любой), хочу авторизоваться, чтобы получить доступ к функционалу
    
*   Я, как пользователь (Любой), хочу просматривать список задач на сегодня, чтобы знать, что я должен выполнить сегодня
    
*   Я, как пользователь (Любой), хочу получать уведомления по напоминаниям из задач, чтобы не забывать о них
    
*   Я, как пользователь (Любой), хочу просматривать настраивать свой профиль, чтобы менять Имя, Фамилию, пароль
    
*   Я, как пользователь (Любой,) хочу просматривать список достижений, чтобы иметь мотивацию для выполнения задач
    
*   Я, как пользователь (Любой), хочу просматривать свое расписание в ВУЗе, чтобы оценивать свое время
    
*   Я, как пользователь (Любой), хочу изменять тему интерфейса (светлая/темная), чтобы работать в удобных условиях.
    
*   Я, как пользователь (Любой), хочу видеть диаграмму прогресса выполнения задач в проекте, чтобы оценивать эффективность работы.
    
*   Я, как пользователь (Любой), хочу включать/отключать уведомления для задач и комментариев, чтобы регулировать количество получаемой информации.
    
*   Я, как пользователь (Создатель проекта), хочу создать проект, чтобы добавлять в него других пользователей
    
*   Я, как пользователь (Создатель проекта), хочу создать проект, чтобы заводить в нем задачи для других пользователь
    
*   Я, как пользователь (Создатель проекта), хочу создать задачу, чтобы назначить на нее исполнителя
    
*   Я, как пользователь (Создатель проекта), хочу создавать задачу, чтобы устанавливать дату ее окончания
    
*   Я, как пользователь (Создатель проекта), хочу создавать задачу, чтобы устанавливать дату ее напоминания
    
*   Я, как пользователь (Создатель проекта), хочу создавать задачу, чтобы устанавливать ее приоритет
    
*   Я, как пользователь (Создатель проекта), хочу устанавливать роли (Редактор или Просмотр) для участников, чтобы разделить зоны ответственности.
    
*   Я, как пользователь (Создатель проекта), хочу удалять участников из проекта, чтобы управлять составом команды.
    
*   Я, как пользователь (Создатель проекта, Редактор), хочу просматривать карточку задачи, чтобы менять ее описание
    
*   Я, как пользователь (Создатель проекта, Редактор), хочу просматривать карточку задачи, чтобы менять ее статус
    
*   Я, как пользователь (Создатель проекта, Редактор), хочу просматривать карточку задачи, чтобы добавлять в нее комментарий
    
*   Я, как пользователь (Создатель проекта, Редактор), хочу просматривать карточку задачи, чтобы менять ее приоритет
    
*   Я, как пользователь (Создатель проекта, Редактор, Просмотр), хочу фильтровать задачи по приоритету, чтобы сосредоточиться на более важных задачах.
    
*   Я, как пользователь (Создатель проекта, Редактор, Просмотр), хочу просматривать карточку задачи, чтобы просматривать ее описание
    
*   Я, как пользователь (Создатель проекта, Редактор, Просмотр), хочу просматривать карточку задачи, чтобы просматривать статус задачи
    
*   Я, как пользователь (Создатель проекта, Редактор, Просмотр), хочу просматривать карточку задачи, чтобы просматривать комментарии к задаче
    
*   Я, как пользователь (Создатель проекта, Редактор, Просмотр), хочу просматривать список задач, чтобы видеть даты окончания задач
    
*   Я, как пользователь (Создатель проекта, Редактор, Просмотр), хочу просматривать список задач, чтобы видеть даты окончания задач
    

USE CASE
========

![plant-2](https://github.com/user-attachments/assets/dce7d7f6-a191-4deb-98eb-9dd5f10c4b61)

![plant](https://github.com/user-attachments/assets/7421c148-e3ea-49b4-b324-baa3bca810dc)

![plant-1](https://github.com/user-attachments/assets/c1c0033f-6896-4c3b-9e96-1f500aaaf29d)


Код на Plant UML

```java
@startuml
' Диаграмма 1: Базовые функции пользователя
actor "Пользователь" as User

package "Базовые функции пользователя" {
    usecase "Авторизация" as Auth
    usecase "Просмотр списка задач на сегодня" as DailyTasks
    usecase "Получение уведомлений\nпо напоминаниям" as Notifications
    usecase "Настройка профиля" as Profile
    usecase "Просмотр достижений" as Achievements
    usecase "Просмотр расписания ВУЗа" as Schedule
    usecase "Изменение темы интерфейса\n(светлая/темная)" as Theme
    usecase "Просмотр диаграммы прогресса\nвыполнения задач" as ProgressDiagram
    usecase "Включение/отключение уведомлений\nдля задач и комментариев" as ToggleNotifications
}

User --> Auth
User --> DailyTasks
User --> Notifications
User --> Profile
User --> Achievements
User --> Schedule
User --> Theme
User --> ProgressDiagram
User --> ToggleNotifications
@enduml

@startuml
' Диаграмма 2: Функциональность Создателя проекта
actor "Создатель проекта" as Creator

package "Функциональность Создателя проекта" {
    usecase "Создание проекта" as CreateProject
    usecase "Добавление пользователей в проект" as AddUsers
    usecase "Создание задачи" as CreateTask
    usecase "Установка даты окончания задачи" as SetTaskDeadline
    usecase "Установка напоминания для задачи" as SetTaskReminder
    usecase "Установка приоритета задачи" as SetTaskPriority
    usecase "Установка ролей для участников" as SetRoles
    usecase "Удаление участников из проекта" as RemoveUsers
}

Creator --> CreateProject
Creator --> AddUsers
Creator --> CreateTask
CreateTask --> SetTaskDeadline
CreateTask --> SetTaskReminder
CreateTask --> SetTaskPriority
Creator --> SetRoles
Creator --> RemoveUsers
@enduml

@startuml
' Диаграмма 3: Функциональность работы с задачами
actor "Редактор" as Editor
actor "Просмотр" as Viewer
actor "Создатель проекта" as Creator

package "Работа с задачами" {
    usecase "Просмотр карточки задачи" as ViewTask
    usecase "Изменение описания задачи" as EditTaskDescription
    usecase "Изменение статуса задачи" as EditTaskStatus
    usecase "Добавление комментариев в задачу" as AddComments
    usecase "Изменение приоритета задачи" as EditTaskPriority
    usecase "Фильтрация задач по приоритету" as FilterTasks
    usecase "Просмотр списка задач с датами\nокончания" as ViewTaskList
    usecase "Просмотр описания задачи" as ViewDescription
    usecase "Просмотр статуса задачи" as ViewStatus
    usecase "Просмотр комментариев к задаче" as ViewComments
}

Creator --> ViewTask
Creator --> EditTaskDescription
Creator --> EditTaskStatus
Creator --> AddComments
Creator --> EditTaskPriority
Creator --> FilterTasks
Creator --> ViewTaskList

Editor --> ViewTask
Editor --> EditTaskDescription
Editor --> EditTaskStatus
Editor --> AddComments
Editor --> EditTaskPriority
Editor --> FilterTasks
Editor --> ViewTaskList

Viewer --> ViewTask
Viewer --> FilterTasks
Viewer --> ViewTaskList

ViewTask --> ViewDescription
ViewTask --> ViewStatus
ViewTask --> ViewComments
@enduml
```

План реализации
===============

Изменение темы
--------------

У пользователя есть возможность менять тему на Светлую, Темную или Системную

![image-20241123-153831.png](attachments/98328/590023.png?width=155)

**Авторизация**
---------------

### Макет:

![Авторизация](https://github.com/user-attachments/assets/e65d5725-c6a3-4717-ae84-c49127daf042)


### Описание элементов:

<table data-table-width="1011" data-layout="default" data-local-id="3740f470-4bfd-4e8c-a683-329504cc6a1d" class="confluenceTable"><colgroup><col style="width: 67.0px;"><col style="width: 196.0px;"><col style="width: 186.0px;"><col style="width: 562.0px;"></colgroup><tbody><tr><td data-highlight-colour="#ffffff" class="confluenceTd"><p><strong>№</strong></p></td><td data-highlight-colour="#ffffff" class="confluenceTd"><p><strong>Название элемента</strong></p></td><td data-highlight-colour="#ffffff" class="confluenceTd"><p><strong>Тип поля</strong></p></td><td data-highlight-colour="#ffffff" class="confluenceTd"><p><strong>Описание элемента</strong></p></td></tr><tr><td class="confluenceTd"><p>1</p></td><td class="confluenceTd"><p></p></td><td class="confluenceTd"><p>Иконка</p></td><td class="confluenceTd"><p>При нажатии на иконку форма закрывается</p></td></tr><tr><td class="confluenceTd"><p>2</p></td><td class="confluenceTd"><p>Авторизация</p></td><td class="confluenceTd"><p>RadioButton</p></td><td class="confluenceTd"><p>При нажатии на RadioButton открывается вкладка авторизации, где пользователь может ввести email и пароль для входа в аккаунт</p></td></tr><tr><td class="confluenceTd"><p>3</p></td><td class="confluenceTd"><p>Регистрация</p></td><td class="confluenceTd"><p>RadioButton</p></td><td class="confluenceTd"><p>При нажатии на RadioButton открывается вкладка регистрации, где пользователь может зарегистрировать свой аккаунт</p></td></tr><tr><td class="confluenceTd"><p>4</p></td><td class="confluenceTd"><p>Email</p></td><td class="confluenceTd"><p>Текст<br>Поле ввода<br>Обязательное</p></td><td class="confluenceTd"><p>Поле для ввода email</p></td></tr><tr><td class="confluenceTd"><p>5</p></td><td class="confluenceTd"><p>Пароль</p></td><td class="confluenceTd"><p>Текст<br>Поле ввода<br>Обязательное</p></td><td class="confluenceTd"><p>Поле для ввода пароля. При вводе пароля скрываем символы, которые вводит пользователь</p></td></tr><tr><td class="confluenceTd"><p>6</p></td><td class="confluenceTd"><p>Войти</p></td><td class="confluenceTd"><p>Кнопка</p></td><td class="confluenceTd"><p>При нажатии кнопки проверяется правильность введенных Email и Пароль. Если пользователь зарегестрирован и данные верны, то при нажатии на кнопку он войдет в свой профиль.<br>Если введены неправильные данные, то ему выводится ошибка.</p><p>Пример ошибок:</p><span class="confluence-embedded-file-wrapper image-left-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-left" alt="image-20241123-120721.png" width="300" loading="lazy" src="attachments/98328/589931.png?width=300" data-image-src="attachments/98328/589931.png" data-height="410" data-width="559" data-unresolved-comment-count="0" data-linked-resource-id="589931" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image-20241123-120721.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="8eb9f3f2-c5d0-4cc1-bed6-27db5cb35c6d" data-media-type="file"></span><span class="confluence-embedded-file-wrapper image-left-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-left" alt="image-20241123-120631.png" width="300" loading="lazy" src="attachments/98328/557143.png?width=300" data-image-src="attachments/98328/557143.png" data-height="432" data-width="556" data-unresolved-comment-count="0" data-linked-resource-id="557143" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image-20241123-120631.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="16618ef1-fd2a-4e63-9454-c0bfa9887b79" data-media-type="file"></span><p></p></td></tr></tbody></table>

**Регистрация**
---------------

### Макет:

![Регистрация](https://github.com/user-attachments/assets/fc612f37-2b6b-4969-9560-a952a058ee64)

### Описание элементов:

<table data-table-width="1011" data-layout="default" data-local-id="2f3953b6-828c-439a-8b3b-c7750b861522" class="confluenceTable"><colgroup><col style="width: 67.0px;"><col style="width: 196.0px;"><col style="width: 186.0px;"><col style="width: 562.0px;"></colgroup><tbody><tr><td class="confluenceTd"><p><strong>№</strong></p></td><td class="confluenceTd"><p><strong>Название элемента</strong></p></td><td class="confluenceTd"><p><strong>Тип поля</strong></p></td><td class="confluenceTd"><p><strong>Описание элемента</strong></p></td></tr><tr><td class="confluenceTd"><p>1</p></td><td class="confluenceTd"><p></p></td><td class="confluenceTd"><p>Иконка</p></td><td class="confluenceTd"><p>При нажатии на иконку форма закрывается</p></td></tr><tr><td class="confluenceTd"><p>2</p></td><td class="confluenceTd"><p>Авторизация</p></td><td class="confluenceTd"><p>RadioButton</p></td><td class="confluenceTd"><p>При нажатии на RadioButton открывается вкладка авторизации, где пользователь может ввести email и пароль для входа в аккаунт</p></td></tr><tr><td class="confluenceTd"><p>3</p></td><td class="confluenceTd"><p>Регистрация</p></td><td class="confluenceTd"><p>RadioButton</p></td><td class="confluenceTd"><p>При нажатии на RadioButton открывается вкладка регистрации, где пользователь может зарегистрировать свой аккаунт.</p></td></tr><tr><td class="confluenceTd"><p>4</p></td><td class="confluenceTd"><p>Email</p></td><td class="confluenceTd"><p>Текст<br>Поле ввода<br>Обязательное</p></td><td class="confluenceTd"><p>Поле для ввода Email. При вводе некорректного email выводится подсказка</p><span class="confluence-embedded-file-wrapper image-left-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-left" alt="image-20241123-122352.png" width="300" loading="lazy" src="attachments/98328/589948.png?width=300" data-image-src="attachments/98328/589948.png" data-height="131" data-width="537" data-unresolved-comment-count="0" data-linked-resource-id="589948" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image-20241123-122352.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="a2a6afe2-216e-448a-8ba1-5c7d164678d1" data-media-type="file"></span></td></tr><tr><td class="confluenceTd"><p>5</p></td><td class="confluenceTd"><p>Имя пользователя</p></td><td class="confluenceTd"><p>Текст<br>Поле ввода<br>Обязательное</p></td><td class="confluenceTd"><p>Поле для ввода Имени пользователя. При вводе имени пользователя менее 3 символов выводится подсказка</p><span class="confluence-embedded-file-wrapper image-left-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-left" alt="image-20241123-122456.png" width="300" loading="lazy" src="attachments/98328/589955.png?width=300" data-image-src="attachments/98328/589955.png" data-height="132" data-width="526" data-unresolved-comment-count="0" data-linked-resource-id="589955" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image-20241123-122456.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="931d7d22-5cd3-4921-9217-430c5c7d01e6" data-media-type="file"></span></td></tr><tr><td class="confluenceTd"><p>6</p></td><td class="confluenceTd"><p>Пароль</p></td><td class="confluenceTd"><p>Текст<br>Поле ввода<br>Обязательное</p></td><td class="confluenceTd"><p>Поле для ввода пароля. При вводе пароля менее 8 символов выводится подсказка</p><span class="confluence-embedded-file-wrapper image-left-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-left" alt="image-20241123-122610.png" width="300" loading="lazy" src="attachments/98328/589962.png?width=300" data-image-src="attachments/98328/589962.png" data-height="121" data-width="526" data-unresolved-comment-count="0" data-linked-resource-id="589962" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image-20241123-122610.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="cc21ea9c-db0f-4e6d-b58b-7ec0e43be93b" data-media-type="file"></span></td></tr><tr><td class="confluenceTd"><p>7</p></td><td class="confluenceTd"><p>Подтвердите пароль</p></td><td class="confluenceTd"><p>Текст<br>Поле ввода<br>Обязательное</p></td><td class="confluenceTd"><p>Поле для ввода пароля, чтобы подтвердить ранее введенный пароль</p></td></tr><tr><td class="confluenceTd"><p>8</p></td><td class="confluenceTd"><p>Зарегистрироваться</p></td><td class="confluenceTd"><p>Кнопка</p></td><td class="confluenceTd"><p>При нажатии на кнопку пользователь регистрируется в системе. После нажатии кнопки форма закрывается.</p></td></tr></tbody></table>

Бокова панель
-------------

### Макет:

![Боковая панель](https://github.com/user-attachments/assets/b17debb2-9c14-436a-bb7d-0fffb11ee072)

### Описание элементов:

Боковая панель может скрываться / раскрываться при нажатии на иконку ![image-20241123-142755.png](attachments/98328/557177.png)

<table data-table-width="1011" data-layout="default" data-local-id="c778fd91-0a92-43a6-b0ad-1c617df70b2a" class="confluenceTable"><colgroup><col style="width: 67.0px;"><col style="width: 196.0px;"><col style="width: 186.0px;"><col style="width: 562.0px;"></colgroup><tbody><tr><td class="confluenceTd"><p><strong>№</strong></p></td><td class="confluenceTd"><p><strong>Название элемента</strong></p></td><td class="confluenceTd"><p><strong>Тип поля</strong></p></td><td class="confluenceTd"><p><strong>Описание элемента</strong></p></td></tr><tr><td class="confluenceTd"><p>1</p></td><td class="confluenceTd"><p></p></td><td class="confluenceTd"><p>Рисунок</p></td><td class="confluenceTd"><p>Хэдер боковой панели, в котором выводим Команду и Иконку “Центр-Инвеста“</p></td></tr><tr><td class="confluenceTd"><p>2</p></td><td class="confluenceTd"><p>Профиль</p></td><td class="confluenceTd"><p>Иконка<br>Текст<br>Выпадающий список</p></td><td class="confluenceTd"><p>Выводим иконку (аватарку) и Имя пользователя.<br>При нажатии на элемент появляется выпадающий список состоящий из:</p><ol start="1"><li><p>Выполненные задачи - при нажатии на данный элемент открывается список задач в статусе “Готово“ из всех проектов</p></li><li><p>Статистика - при нажатии на данный элемент открываются настройки пользователя</p></li><li><p>Настройки</p></li><li><p>Выйти</p><span class="confluence-embedded-file-wrapper image-center-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-center" alt="image-20241123-143500.png" width="197" loading="lazy" src="attachments/98328/524413.png?width=197" data-image-src="attachments/98328/524413.png" data-height="204" data-width="197" data-unresolved-comment-count="0" data-linked-resource-id="524413" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image-20241123-143500.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="7de7dcfc-e0cb-4cb7-99c0-f1d54b2b0211" data-media-type="file"></span></li></ol></td></tr><tr><td class="confluenceTd"><p>3</p></td><td class="confluenceTd"><p></p></td><td class="confluenceTd"><p>Иконка</p></td><td class="confluenceTd"><p>Иконка уведомления рядом с профилем<br>В данный колокольчик приходит уведомления по созданным заданиям и напоминаниям<br>При приходе уведомления появляется цифра на иконке</p><span class="confluence-embedded-file-wrapper image-left-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-left" alt="image-20241123-153714.png" width="300" loading="lazy" src="attachments/98328/524468.png?width=300" data-image-src="attachments/98328/524468.png" data-height="204" data-width="387" data-unresolved-comment-count="0" data-linked-resource-id="524468" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image-20241123-153714.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="d1d1f1a9-b49a-4add-9d65-a39de34b3757" data-media-type="file"></span></td></tr><tr><td class="confluenceTd"><p>4</p></td><td class="confluenceTd"><p>Добавить задачу</p></td><td class="confluenceTd"><p>Кнопка</p></td><td class="confluenceTd"><p>При нажатии на кнопку открывается Поп-ап с созданием задачи - <a data-card-appearance="inline" href="https://antonbaturin2003.atlassian.net/wiki/spaces/~6364bc70548f1fe6f0c869eb/pages/98328/CyberGarden+18+2024#%D0%94%D0%BE%D0%B1%D0%B0%D0%B2%D0%B8%D1%82%D1%8C-%D0%B7%D0%B0%D0%B4%D0%B0%D1%87%D1%83" rel="nofollow">https://antonbaturin2003.atlassian.net/wiki/spaces/~6364bc70548f1fe6f0c869eb/pages/98328/CyberGarden+18+2024#%D0%94%D0%BE%D0%B1%D0%B0%D0%B2%D0%B8%D1%82%D1%8C-%D0%B7%D0%B0%D0%B4%D0%B0%D1%87%D1%83</a></p><p>Данный элемент должен быть зеленого цвета и быть больше других элементов</p></td></tr><tr><td class="confluenceTd"><p>5</p></td><td class="confluenceTd"><p>Сегодня</p></td><td class="confluenceTd"><p>Кнопка</p></td><td class="confluenceTd"><p>Выводим все задачи созданные на сегодня. Данная страница открывается пользователю первой.</p></td></tr><tr><td class="confluenceTd"><p>6</p></td><td class="confluenceTd"><p>Расписание вуза</p></td><td class="confluenceTd"><p>Кнопка</p></td><td class="confluenceTd"><p>Выводим расписание ВУЗа ИКТИБ ЮФУ. API - <a class="external-link" href="https://ictis.ru/about" rel="nofollow">О сайте - ictis alex b</a>.</p></td></tr><tr><td class="confluenceTd"><p>7</p></td><td class="confluenceTd"><p>Достижения</p></td><td class="confluenceTd"><p>Кнопка</p></td><td class="confluenceTd"><p>Выводим список достижений. Сначала в списке выводим полученные достижения. Потом достижения, которые ближе к выполнению.</p></td></tr><tr><td class="confluenceTd"><p>8</p></td><td class="confluenceTd"><p>Проекты</p></td><td class="confluenceTd"><p>Тест</p></td><td class="confluenceTd"><p>Данная надпись является заголовком. Рядом с надписью есть знак +, который используется для создания нового проекта. Так же можно сворачивать разворачивать данный блок, при нажатии на &gt;.</p></td></tr><tr><td class="confluenceTd"><p><span class="confluence-anchor-link" id="CyberGarden182024-0a0d0f21-a8f5-40d5-a925-b11792572586"><span class="confluence-anchor-link" id="0a0d0f21-a8f5-40d5-a925-b11792572586"></span></span>9</p></td><td class="confluenceTd"><p></p></td><td class="confluenceTd"><p>Иконка</p></td><td class="confluenceTd"><p>При нажатии на иконку открывается Поп-ап создания проекта.</p></td></tr><tr><td class="confluenceTd"><p>10</p></td><td class="confluenceTd"><p>Название проекта</p></td><td class="confluenceTd"><p>Кнопка</p></td><td class="confluenceTd"><p>При нажатии на элемент выводится список задач, созданных в рамках данного проекта.</p><p>Рядом с названием проекта есть иконка … При нажатии на иконку выводим кнопки:</p><ol start="1"><li><p>Редактировать - открывается заполненная форма создания задачи, которую можно изменить и сохранить</p></li><li><p>Выполненные задачи - при нажатии на данный элемент открывается список задач в статусе “Готово“ в данном проекте</p></li><li><p>Удалить - удалить проект</p></li></ol></td></tr></tbody></table>

Добавить задачу
---------------

### Макет:

![Добавление задачи](https://github.com/user-attachments/assets/0c01a0a5-3853-4afb-a8ab-a8cad38358bc)


### Описание элементов:

При нажатии на кнопку создать задачу открывается Поп-ап в котором можно создать задачу.

<table data-table-width="1011" data-layout="default" data-local-id="9c25fe31-65ef-4c42-a665-f9df6bfc0111" class="confluenceTable"><colgroup><col style="width: 67.0px;"><col style="width: 196.0px;"><col style="width: 186.0px;"><col style="width: 562.0px;"></colgroup><tbody><tr><td class="confluenceTd"><p><strong>№</strong></p></td><td class="confluenceTd"><p><strong>Название элемента</strong></p></td><td class="confluenceTd"><p><strong>Тип поля</strong></p></td><td class="confluenceTd"><p><strong>Описание элемента</strong></p></td></tr><tr><td class="confluenceTd"><p>1</p></td><td class="confluenceTd"><p></p></td><td class="confluenceTd"><p>Иконка</p></td><td class="confluenceTd"><p>При нажатии на иконку форма закрывается</p></td></tr><tr><td class="confluenceTd"><p>2</p></td><td class="confluenceTd"><p>Название задачи</p></td><td class="confluenceTd"><p>Поле ввода<br>Обязательное</p></td><td class="confluenceTd"><p>В данном поле пользователь вводит название задачи.<br>Текст в данном поле должен быть больше, чем в поле “Описание задачи“</p></td></tr><tr><td class="confluenceTd"><p>3</p></td><td class="confluenceTd"><p>Описание задачи</p></td><td class="confluenceTd"><p>Поле ввода<br>Необязательное</p></td><td class="confluenceTd"><p>В данном поле пользователь вводит описание задачи. Поле должно шириной в 3 строчки. Если пользователь вводит более 3 строк, то поле расширяется.</p></td></tr><tr><td class="confluenceTd"><p>4</p></td><td class="confluenceTd"><p>Выберите дату выполнения задачи</p></td><td class="confluenceTd"><p>Календарь<br>Обязательное</p></td><td class="confluenceTd"><p>Пользователь выбирает дату, до которой исполнитель должен выполнить задачу. Задача в списке будет находится в дате, которая выбрана в данном поле.</p><span class="confluence-embedded-file-wrapper image-left-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-left" alt="image-20241123-145332.png" width="100" loading="lazy" src="attachments/98328/622742.png?width=100" data-image-src="attachments/98328/622742.png" data-height="333" data-width="291" data-unresolved-comment-count="0" data-linked-resource-id="622742" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image-20241123-145332.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="a4d1c688-128c-4f32-8245-5511b19676d1" data-media-type="file"></span></td></tr><tr><td class="confluenceTd"><p>5</p></td><td class="confluenceTd"><p>Приоритет</p></td><td class="confluenceTd"><p>Выпадающий список с моновыбором<br>Необязательное</p></td><td class="confluenceTd"><p>Изначально задаем приоритет 1. Для выбора есть приоритеты 1-4. Чем выше приоритет, тем выше задача в списке на данный день.</p><span class="confluence-embedded-file-wrapper image-left-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-left" alt="image-20241123-145510.png" width="125" loading="lazy" src="attachments/98328/589994.png?width=125" data-image-src="attachments/98328/589994.png" data-height="178" data-width="125" data-unresolved-comment-count="0" data-linked-resource-id="589994" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image-20241123-145510.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="26d0759b-a151-4839-a673-198e5f4675d6" data-media-type="file"></span></td></tr><tr><td class="confluenceTd"><p>6</p></td><td class="confluenceTd"><p>Выберите дату напоминания</p></td><td class="confluenceTd"><p>Календарь<br>Необязательное</p></td><td class="confluenceTd"><p>Пользователь выбирает дату, когда придет уведомление, напоминающее, что нужно сделать задачу</p><span class="confluence-embedded-file-wrapper image-left-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-left" alt="image-20241123-145810.png" width="100" loading="lazy" src="attachments/98328/622749.png?width=100" data-image-src="attachments/98328/622749.png" data-height="338" data-width="256" data-unresolved-comment-count="0" data-linked-resource-id="622749" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image-20241123-145810.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="5b85791c-bedd-419c-9bbe-de27dfbf05f7" data-media-type="file"></span></td></tr><tr><td class="confluenceTd"><p>7</p></td><td class="confluenceTd"><p>Проект</p></td><td class="confluenceTd"><p>Выпадающий список с моновыбором и возможностью поиска<br>Обязательное</p></td><td class="confluenceTd"><p>Пользователь выбирает в каком проекте (из тех, в которых он состоит) создать задачу</p><span class="confluence-embedded-file-wrapper image-left-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-left" alt="image-20241123-150712.png" width="150" loading="lazy" src="attachments/98328/524442.png?width=150" data-image-src="attachments/98328/524442.png" data-height="209" data-width="255" data-unresolved-comment-count="0" data-linked-resource-id="524442" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image-20241123-150712.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="468de51b-91f5-4cc0-8c1f-90a6ec7d8ba5" data-media-type="file"></span></td></tr><tr><td class="confluenceTd"><p>8</p></td><td class="confluenceTd"><p>Исполнитель</p></td><td class="confluenceTd"><p>Выпадающий список с моновыбором и возможностью поиска<br>Обязательное</p></td><td class="confluenceTd"><p>Создатель задачи должен выбрать исполнителя, среди пользователей, которые есть в проекте</p><span class="confluence-embedded-file-wrapper image-left-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-left" alt="image-20241123-150744.png" width="150" loading="lazy" src="attachments/98328/524449.png?width=150" data-image-src="attachments/98328/524449.png" data-height="266" data-width="255" data-unresolved-comment-count="0" data-linked-resource-id="524449" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image-20241123-150744.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="c0a3077e-df85-44cc-a6a8-c4e027001caf" data-media-type="file"></span></td></tr><tr><td class="confluenceTd"><p>9</p></td><td class="confluenceTd"><p>Отмена</p></td><td class="confluenceTd"><p>Кнопка</p></td><td class="confluenceTd"><p>При нажатии на кнопку происходит отмена создания события</p></td></tr><tr><td class="confluenceTd"><p>10</p></td><td class="confluenceTd"><p>Добавить задачу</p></td><td class="confluenceTd"><p>Кнопка</p></td><td class="confluenceTd"><p>При нажатии на кнопку создается задача. После создания задача должна появится в списке задач</p></td></tr></tbody></table>

**Создание проекта**
--------------------

### Макет:

![Добавление проекта](https://github.com/user-attachments/assets/c58de75f-3fac-4c08-ac24-a08bbb7c5372)


### Описание элементов:

При нажатии на + рядом с Проект ([https://antonbaturin2003.atlassian.net/wiki/spaces/~6364bc70548f1fe6f0c869eb/pages/98328#0a0d0f21-a8f5-40d5-a925-b11792572586](https://antonbaturin2003.atlassian.net/wiki/spaces/~6364bc70548f1fe6f0c869eb/pages/98328#0a0d0f21-a8f5-40d5-a925-b11792572586) ) открывается Поп-ап с созданием проекта.

<table data-table-width="1011" data-layout="default" data-local-id="9d1f9c30-7076-4227-9674-6af130a088a9" class="confluenceTable"><colgroup><col style="width: 67.0px;"><col style="width: 196.0px;"><col style="width: 186.0px;"><col style="width: 562.0px;"></colgroup><tbody><tr><td class="confluenceTd"><p><strong>№</strong></p></td><td class="confluenceTd"><p><strong>Название элемента</strong></p></td><td class="confluenceTd"><p><strong>Тип поля</strong></p></td><td class="confluenceTd"><p><strong>Описание элемента</strong></p></td></tr><tr><td class="confluenceTd"><p>1</p></td><td class="confluenceTd"><p></p></td><td class="confluenceTd"><p>Иконка</p></td><td class="confluenceTd"><p>При нажатии на иконку форма закрывается</p></td></tr><tr><td class="confluenceTd"><p>2</p></td><td class="confluenceTd"><p>Добавить проект</p></td><td class="confluenceTd"><p>Текст</p></td><td class="confluenceTd"><p>Данная надпись является заголовком</p></td></tr><tr><td class="confluenceTd"><p>3</p></td><td class="confluenceTd"><p>Имя проекта</p></td><td class="confluenceTd"><p>Текст<br>Поле ввода<br>Обязательное</p></td><td class="confluenceTd"><p>В данном поле пользователь вводит название (имя) проекта</p></td></tr><tr><td class="confluenceTd"><p>4</p></td><td class="confluenceTd"><p>Пользователь</p></td><td class="confluenceTd"><p>Выпадающий список с мультивыбором и возможностью поиска<br>Необязательное</p></td><td class="confluenceTd"><p>Создатель проекта может сразу добавлять пользователей по их имени или email.</p><p>При выборе пользователя, он выводится ниже данного элемента, рядом с ним появляется иконка крестика, которая дает возможность удалить пользователя.</p><span class="confluence-embedded-file-wrapper image-left-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image image-left" alt="image 10.png" width="200" loading="lazy" src="attachments/98328/557241.png?width=200" data-image-src="attachments/98328/557241.png" data-height="656" data-width="425" data-unresolved-comment-count="0" data-linked-resource-id="557241" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image 10.png" data-base-url="https://antonbaturin2003.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="98328" data-linked-resource-container-version="30" data-media-id="f6c1768d-e5f8-4388-b187-2aebe48e0d76" data-media-type="file"></span></td></tr><tr><td class="confluenceTd"><p>5</p></td><td class="confluenceTd"><p>Отмена</p></td><td class="confluenceTd"><p>Кнопка</p></td><td class="confluenceTd"><p>При нажатии на кнопку происходит отмена создания проекта</p></td></tr><tr><td class="confluenceTd"><p>6</p></td><td class="confluenceTd"><p>Добавить</p></td><td class="confluenceTd"><p>Кнопка</p></td><td class="confluenceTd"><p>При нажатии на кнопку создается задача. После создания задача должна появится в списке проектов</p></td></tr></tbody></table>

4.  **Список задач | Проект**
    

Заголовок - Название проекта

Ниже выводим количество задач, которое есть в списке

Выводим список задач по датам. С возможностью создать задачу в данную дату

**При нажатии на чекбокс (можно выбирать несколько чекбоксов разом) появляется кнопка “Закрыть задачи“ рядом с Заголовком (Название проекта). При нажатии на кнопку открывается поп-ап. Заголовок - Закрыть задачу. Две кнопки - Да / Нет.**

Пример:

![image-20241122-225446.png](attachments/98328/557062.png?width=760)

Задачи в списке выводятся согласно их приоритетам. Задачи с высшим приоритетом выводятся выше. Если у задач одинаковый приоритет, то выводим согласно алфавиту от А-Я.

В списке задач, на каждой строчке задачи выводится исполнитель.

Рядом с название задачи выводим Выпадающий список с моновыбором статусов задачи. Возможность изменять статус есть у Создателя проекта и Редактора.

5.  **Список задач | Сегодня**
    

Заголовок - Сегодня

Ниже выводим количество задач, которое есть в списке

Выводим список задач по датам.

**При нажатии на чекбокс (можно выбирать несколько чекбоксов разом) появляется кнопка “Закрыть задачи“ рядом с Заголовком (Название проекта). При нажатии на кнопку открывается поп-ап. Заголовок - Закрыть задачу. Две кнопки - Да / Нет.**

![image-20241123-002845.png](attachments/98328/589860.png?width=760)

Задачи в списке выводятся согласно их приоритетам. Задачи с высшим приоритетом выводятся выше. Если у задач одинаковый приоритет, то выводим согласно алфавиту от А-Я.

В списке задач, на каждой строчке задачи выводится исполнитель.

Рядом с название задачи выводим Выпадающий список с моновыбором статусов задачи. Возможность изменять статус есть у Создателя проекта и Редактора.

**В самом верху выводим просроченные задачи (нынешняя дата > дата окончания задачи)**

Заголовок - Просроченные задачи. Под названием задачи пишется насколько просрачена задача

Пример:

![image-20241123-002807.png](attachments/98328/622633.png?width=222)

6.  **Карточка задачи**  
    При нажатии на название задачи открывается карточка задачи. Данная карточка состоит из 2 блоков - Блок с Названием/Статусом/Описанием/Возможность добавлять подзадачи/Комментарием и Блок с Проектом/Исполнителем/
