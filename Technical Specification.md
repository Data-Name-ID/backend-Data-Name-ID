# Backend: Travel agent 3.0

## PROD: индивидуальный этап

С условием задания вы можете ознакомиться в [Notion](https://centraluniversity.notion.site/PROD-a404fd65bd6044da83fdf60859ff7733).

Вы можете самостоятельно выбирать стек и фреймворки, которые вы хотите использовать. Единственное ограничение &mdash; воздержитесь от изменения директории `.github` в корне репозитория.

Вы должны самостоятельно подготовить файл [`docker-compose.yml`](https://docs.docker.com/compose/). Убедитесь, что ваше приложение запускается с помощью `docker compose up -d`.

## Описание

Представьте, что вы хотите поехать в путешествие со своими друзьями, но для этого нужно сделать массу вещей: купить билеты, забронировать отель, спланировать маршрут, делить расходы, выбирать развлечения и еще при этом понимать, какая погода будет на протяжении маршрута. Вам необходимо реализовать Telegram бота, который поможет людям планировать совместные путешествия без головной боли!

В данном задании мы будем оценивать полноценное приложение, созданное с вами “с нуля”. Мы не сможем предоставить четкие критерии к приложению, так как на этот раз вы полностью отвечаете за идеи, креатив и реализацию.

## Общие требования к проекту

- Разработка приложения происходит с помощью технологии git. **Оценивается версия приложения, загруженная в приватный репозиторий организации до дедлайна**.
- Для разработки приложения доступны следующие языки: Python, Go, Java, Kotlin, Scala, C#, NodeJS, Rust, C++, PHP, YAML.
- Разработчик проекта самостоятельно выбирает стек и технологии для разработки.
- В репозитории проекта должен находиться файл docker-compose.yml, с помощью которого происходит сборка (Dockerfile) и запуск приложения и его зависимостей.
- Данные пользователей должны сохраняться в СУБД.
- Разработчик самостоятельно выбирает набор нужных зависимостей (PostgreSQL, sqlite, MySQL, redis, cassandra, S3, rabbitmq и другие). Главное, чтобы этот выбор был оправдан, а зависимости корректно запускались с помощью docker compose.
- Для поиска маршрутов должно использоваться API OpenStreetMap (разрешается использовать фреймворки и библиотеки для работы с ним).
- Приложение должно подключаться к Telegram Bot API, используя токен бота, полученный участником у [@BotFather](https://t.me/BotFather). Если сторонние интеграции требуют аутентификации, участник должен самостоятельно указать токены доступа.
- В README проекта находится документация: инструкция по сборке, сценарии использования, описание логики работы и описание интеграции со сторонними решениями.

### Отправка задания

Исходный код решения необходимо загрузить в форк-репозиторий в нашей приватной организации.

После 20 марта в github репозиториях будет доступен Github CI для тестирования запуска docker compose вашего решения. До этого момента вы можете разрабатывать приложение в репозитории без CI. **До этого времени не редактируйте директорию `.github` в корне репозитория.**

Так как в репозиториях нет доступа к Github Secrets, токены для общения с Telegram / сторонними API придется хранить в открытом виде (например, в docker-compose.yml). Можете считать, что на данном этапе мы разрабатываем приложение в staging окружении, а после окончания соревнования вы сможете перенести его в свои репозитории и подкладывать настоящие секреты, используя безопасный механизм Github Secrets.

### 💯 Оценивание

Вы самостоятельно выбираете набор возможностей, которое будет предоставлять ваше приложение.

**Обратите внимание: в некоторых направлениях сумма баллов за поднаправление превышает максимально возможный балл за направление.** В первую очередь важно не количество поддерживаемых механик, а их проработанность.

Например, реализовав все опциональные возможности на максимальный балл, в теории можно получить 26 баллов, однако существует ограничение сверху: не более 18 баллов за опциональные функциональные возможности.

Перед оцениванием мы будем запускать docker compose с вашим решением, после чего будет проводиться ручная проверка бота в Telegram. Убедитесь, что ваше приложение запускается с помощью команды `docker compose up -d` в репозитории и не требует зависимостей, которые не определены в репозитории. Перед финальной отправкой не забудьте “выключить” бота на своем локальном компьютере, чтобы он не конкурировал с версией, которую запустим мы.

| Направление | Группа | Максимальный балл |
| --- | --- | --- |
| Обязательные функциональные возможности |  | 17 |
|  | Добавление данных пользователя | 2 |
|  | Управлением путешествием | 5 |
|  | Заметки к путешествию | 3 |
|  | Путешествия с друзьями | 2 |
|  | Прокладывание маршрута путешествия | 5 |
| Опциональные функциональные возможности |  | 18 |
|  | Прогноз погоды в промежуточных точках | 3 |
|  | Подбор билетов | 3 |
|  | Подбор отелей | 3 |
|  | Рекомендация местных достопримечательностей | 3 |
|  | Выбор кафе и ресторанов | 3 |
|  | Поиск пользователей для совместного путешествия | 3 |
|  | Общие траты в путешествии | 3 |
|  | Ваши собственные идеи | 5 |
| Общая оценка бота |  | 3 |
| Документация проекта |  | 5 |
|  | Инструкция по запуску приложения | 1 |
|  | Демонстрация работы приложения | 2 |
|  | Описание внешних интеграций | 2 |
|  | Схема данных СУБД | 1 |
| Наличие юнит тестов |  | 3 |
| Обоснованность выбора технологий |  | 3 |
| Чистота кода |  | 3 |

Баллы могут быть снижены за:

- Некорректная работа с git — до 2 баллов (баллы будут снижаться за откровенное отклонение от всех разумных шаблонов использования git: например, за безрассудные commit message и т. д.)
- Бот не запускается при помощи docker compose — до 5 баллов

### Функциональные требования

Прежде всего это креативная работа, разработчику необходимо самостоятельно проработать логику работу приложения, выбрать его функциональные возможности и придумать дизайн.

В таблице разбалловки вы можете увидеть два направления: обязательные и необязательные функциональные возможности.

Обязательные функциональные возможности — минимальные базовые возможности, которые мы будем ожидать от ваших ботов. Этот блок нужен для выравнивания работ участников, чтобы мы все были на одной волне и делали приложение, которое решает одну проблему.

Необязательные функциональные возможности — дополнительные идеи, с помощью которых мы можете улучшить своих ботов. Некие killer-feature! Мы даем пример того, что можно реализовать, однако мы готовы выдавать баллы за ваши уникальные идеи.

**При оценивании функциональных возможностей мы оцениванием их как пользователи: насколько механика соответствует ожиданиям, насколько это удобно и “гладко”. UX тоже важен.**

Для получения информации о маршрутах, билетах, ресторанах и так далее мы рекомендуем использовать публичные API. Особых ограничений на данный момент нет.

#### Добавление пользователей

У пользователя есть возможность добавить информацию о себе: возраст, город и страна проживания, краткое bio (как в Telegram).

Этот механизм используйте при первом взаимодействии пользователя с ботом, после чего у пользователя появляется возможность редактировать данную информацию.

Планирование путешествие осуществляется исходя из того, что пользователь находится городе, который он указал в регистрационной информации. Можете поддержать функцию “поделиться локацией” :)

#### Управление путешествием

Бот позволяет управлять путешествием. Путешествие - это сущность, которая включает в себя название (должно быть уникальным), краткое описание, локации в порядке, которые необходимо посетить, с датами начала и конца посещения.

Бот должен уметь выполнять следующие операции с путешествием

1. Просмотр. При просмотре должен отображаться список путешествий, в котором должно быть id, имя, описание, список локаций с датами начала и конца посещения.
2. Создание. При создании пользователь указывает минимальную необходимую информацию, у путешествия создается уникальный ID.
3. Редактирование. Тут все понятно, путешествие можно отредактировать :) Например, добавить еще один город для посещения.
4. Удаление. Если поездка отменилась, мы захотим удалить информацию о ней!

#### Путешествие с друзьями

Путешествовать с друзьями намного веселее, поэтому бот должен уметь добавлять в путешествие других людей. После добавления других участников, добавленные участники должны также иметь доступ к путешествию и видеть всю информацию, связанную с ним.

При добавлении нового пользователя в путешествие, все добавленные пользователи получают об этом уведомление. Вы сами выбираете, как именно приглашать пользователей в путешествие.

#### Заметки к путешествию

В процессе путешествия вы делаете много фотографий, а также бронируете отели, покупаете билеты и экскурсии, все это хочется хранить. Бот должен уметь сохранять файлы и различные картинки для путешествия, а также иметь команду для просмотра списка всех заметок по конкретному путешествию. Также к заметкам хочется добавить возможность приватности, чтобы либо только владелец заметки мог ее видеть, либо она была общедоступной для всех участников путешествия. При выполнении операции бот должен писать в ответ “Заметка <имя файла> успешно добавлена в <название путешествия>”

#### Прокладывание маршрута путешествия

У бота должна быть возможность строить маршрут по всем локациям, которые были указаны в путешествии от стартовой до конечной локации по порядку и присылать изображение пути.

Также для всех участников путешествия бот должен уметь прокладывать маршрут от места, где они находятся, до стартовой точки путешествия. Для прокладывания маршрутов мы рекомендуем использовать OpenStreetMap.

**Ограничьтесь от использования популярных проприетарных API  (yandex maps, 2gis, google maps). Попробуйте именно OpenStreetMap.**

#### Прогноз погоды в промежуточных точках

Когда вы едете в новые города и страны, то вы хотите знать какую одежду стоит брать с собой, а для этого будет круто, если бот сможет показывать прогноз погоды для каждой локации на даты пребывания в ней.

#### Подбор билетов

Бот должен уметь предлагать возможные билеты (авиа и железнодорожные) на даты посещения локаций и отображать время поездки и стоимость билета, а также ссылку на покупку.

#### Подбор отелей

Бот должен уметь предлагать возможные отели на даты посещения локаций и отображать название, количество звезд, местоположение и стоимость разных номеров.

#### Рекомендация достопримечательностей

Бот должен уметь показывать список достопримечательностей, которые круто было бы посетить в локациях маршрута путешествия. Должен отображаться список мест с названием, городом и адресом.

Например, если мы едем в Рим, то неплохо бы предложить посетить Колизей. Ну, вы поняли… :)

#### Выбор кафе и ресторанов

Бот должен уметь отображать список кафе и ресторанов для каждой локации маршрута путешествия. В списке должно отображаться название, город, адрес, рейтинг и средний чек.

#### Поиск пользователей для совместного путешествия

Иногда бывает, что у друзей постоянно много работы или учебы, а вы хотите отправиться в путешествие не один. Для этого здорово было бы реализовать возможность подбора людей для путешествия по интересами. Бот должен отображать список людей, которые подходят по интересам и имеют разницу в возрасте не более 5 лет. В списке должны быть логин, возраст, пол, страна, город и интересы.

#### Общие траты в путешествии

Вот вы поехали с друзьями и кто-то не ест мясо, кто-то не пьет газировку, а кто-то не ест сладкое. И каждый из друзей оплачивает что-то на всех и хочет не хранить чеки, а просто делить сумму покупок на тех, кто вместе что-то ел или пил. Бот должен уметь сохранять покупки и делить их между участниками. Для этого он должен уметь сохранять пользователя, сумму транзакции, дату и участников, на которых необходимо поделить покупку, в случае если участника не существует в путешествии, то операция считается не валидной и бот должен предупредить об этом пользователя. В случае успешной операции бот должен уведомить всех участников покупки.

Бот также должен уметь отображать для каждого участника список его долгов и долгов перед ним. В списке должен быть пользователь и сумма, которую участник должен пользователю, либо пользователь участнику. Есть возможность отметить трату как зачтенную (когда друг вернет долг).

Некий аналог splitwise!

#### Ваши собственные идеи

Вы можете придумать собственные идеи и реализовать их. Мы будем оценивать как пользу и ценность для пользователей, так и сложность реализации. Проявите фантазию, сделайте вашего бота уникальным.

#### Общая оценка бота

В данной категории наши проверяющие оценят бота в совокупности: насколько удобно им пользоваться, насколько он быстрый и логичный. Максимальную оценку мы ставим в том случае, если вашим ботом захочется пользоваться при каждом следующем планировании поездки.

### Нефункциональные требования

#### Документация проекта

В [README.md](README.md) (и других md-файлах) вы должны рассказать о своем проекте. Включите туда:

- **Инструкция по запуску вашего приложения**: как минимум информацию о том, как устроен ваш `docker-compose.yml`.
- **Демонстрация работы вашего приложения**: расскажите, как пользоваться вашим приложением. Покажите основные сценарии, опишите логику работы бота. Добавляйте скриншоты там, где не хватает. При этом старайтесь не писать огромные объемы текста, описание сценариев должно быть кратким. Эту информацию будут изучать проверяющие, чтобы лучше понять задумку вашего приложения.
- **Описание внешних интеграций** — опишите API и другие интеграции, которые есть у вашего решения. Расскажите, почему вы выбрали именно ту самую СУБД или тот самый сервис для рекомендации отелей? Опишите их API, которым вы пользуетесь.
- **Схема данных СУБД** — опишите модели данных в вашей СУБД и связи между ними.

#### Наличие юнит тестов

Здесь нет четких критериев по проценту покрытия кодом. Вы должны убедиться, что когда вы делаете изменения проекта, старая функциональность не ломается.

Если в проекте совсем не будет тестов, проверяющие будут грустить. Тестируйте свой код!

#### Обоснованность выбора технологий

Расскажите, почему вы выбрали именно те СУБД и внешние зависимости, которые у вас есть. Представьте, что вы защищаете техническое решение перед своей командой и рассказываете, почему именно выбранный вами стек подходит лучше всего для решения задачи.

#### Чистота кода

Да, мы любим абстрактные формулировки! Жесткого контроля здесь не будет, так как для каждого языка множество guideline для написания кода. Однако структура и качество вашего кода должны быть на хорошем уровне. Представьте, что вы пишите код, который потом будут ревьюить ваши коллеги.

Сделайте так, чтобы во время ревью было как можно меньше замечаний.