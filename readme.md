# Обучающие материалы `aom`

Ку-ку

Данный репозиторий содержит обучающие материалы по пользованию фреймворком `aom`, и описывает
популярные кейсы, лучшие практики и методологии пользования.

Репозиторий содержит примеры кода и позволяет применить на практике описанные материалы.

Базовая документация доступна по ссылке [`aom.js.org`](https://aom.js.org). Данный репозиторий рассматривает
общие и типовые случаи применения фреймворка на примере популярных бизнес-кейсов: работа со справочниками,
доступ к данным, масштабируемость, безопасность.

## Структура документации

1. Пример создания API [`api-create`](./1-api-create/readme.md)
2. Рекомендации организации файлов [`recommendations`](./2-recommendations/readme.md)
3. Общие ответы (рендеры и типовые ошибки) [`common-responses`](./3-common-responses/readme.md)
4. Роутеры из схем данных [`schemas-to-controllers`](./4-schemas-to-controllers/readme.md)
5. Комбинации маршрутов [`routes-combinations`](./5-routes-combinations/readme.md)
6. Валидация входящих данных [`body-validation`](./6-body-validation/readme.md)
7. Поиск данных [`query-search`](./7-query-search/)
8. Права доступа и ограничения вызовов [`access-control`](./8-access-control/readme.md)

## Рекомендации к прочтению

На данный момент на базе `aom` функционируют следующие проекты, написанные мною единолично:

- API методологической платформы `play.thegame.bz`: ~500 эндпоинтов в 8 сервисах
<!-- - сервис продаж мягких игрушек с онлайн-контентом `astrogotchi.com`: ~200 эндпоинтов в 6 сервисах -->
- в разработке несколько крупных проектов с совокупным количеством точек обмена данными >200 в каждом

Таким образом создается возможность делегировать удачный опыт и развивать удобный и функциональный
методологический блок, позволяющий быстро и комфортно решать большие бизнес-задачи. В планах много
наработок по расширению возможностей фреймворка, более строгой его типизации и области применения:
расширенная генерация кода, поддержка `GraphQL`, создание общих областей данных.

Документацию лучше всего читать, копируя примеры кода в собственный редактор, и экспериментально манипулируя
деталями, чтобы лучше понимать закономерности, заложенные в код. Приведенные примеры не обязательно будут
работоспособны из коробки без соблюдения общего контекста.

Также существует репозиторий [`aom-js/demo`](https://github.com/aom-js/demo), в котором собран
базовый кейс на примерах, описанных в подразделах: можно запустить и работать на живом коде.

## Об авторе и фреймворке

Меня зовут Григорий Холстинников, в разных сообществах всегда был представлен по нику `scarych`.
Я программист с давним стажем: первую программу на ZX Spectrum написал в 11 лет, с последующим погружением
в программирование на всю дальнейшую жизнь. Имею опытом разной степени погружения в `Basic`, `C++`, `Pascal`,
`Perl`, `Python`, `Scala`, `Java`, `PHP`, `JavaScript`, а также разные технологии баз данных и серверных приложений.

На протяжении последних ~20 лет решаю бизнесовые задачи в веб-разработке: создание собственных CMS, CRM,
автоматизация крупных бизнес-задач, разработка стартапов. В общем случае был занят разработкой собственного
фреймворка, на котором мне было бы удобно делать то, что я находил неудобным в популярных решениях типа `Yii`,
`Laravel`, `WordPress`, `Bitrix`, `Meteor`, `NextJS`. С 2014 года веду разработку на `NodeJS`, эволюционно
вовлекаясь в использование `express` затем `koa`, `MongoDB`, `Kafka` и других архитектурных решений.

Результатом моей работы в общих случаях было создание сложно-составных программных продуктов со
специфической функциональностью:

- cоциальная платформа [`THEGAME`](https://play.thegame.bz)
- стартап онлайн-аукционов встреч с людьми [`Meet For Charity`](https://meetforcharity.today)
- сервис автоматизации сбора данных от полевых сотрудников `UNIO`
- ряд промежуточных проектов, существоваших в разные годы, или не запущенных: онлайн-магазин одежды `CloClo`,
  коммуникативная платформа `monmio.top`, сервис сбора пользовательской обратной связи `Probleme Net`,
  экологическая платформа `Treepay`, процессинг договоров `Mindfields`, сайт клана `SteelHearts` игры
  `Бойцовский Клуб` и несколько других.

В 2021 году формализовал ряд удачных решений в мета-фреймворк на декораторах `aom`. В настоящее время
доступна стабильная `beta`-версия, которая будет предсказуемо развиваться в более сложное решение,
придерживаясь общей концепции всей методологии.

Среди критериев требований к функционалу были в том числе такие, как воспринимаемая простота кода и общее удобство
пользования. Код должен читаться естественно и давать предельно полную ожидаемую информацию о себе, и позволять
можно применять повторно типовые решения, комбинируя популярные кейсы требований к данным. Буквально обеспечивая
прослойку безопасного `API` поверх моделей данных. Отсюда и название `aom - API over models`.

С момента `beta`-релиза фреймворка на нем было запрограммировано несколько бизнес-проектов с высокой степенью
сложности предметной области: десятки справочников, высокая степень связанности данных и сложные бизнес-логики,
сотни эндпоинтов в API. Исходный код лишен многих головных болей, которые были мною были обнаружены в готовых
популярных решениях, однако может быть лишен ряда полезных вещей, которые могут с разной степенью комфорта туда
интегрированы.

Уже наработан хороший набор готовых решений, которые позволяют типичным образом решать сложные бизнес-задачи.
Код стабильно себя ведет на высоких нагрузках и больших объемах данных. Есть множество идей развития локальной
и общей функциональности, а также библиотек готовых элементов и решений.

К партнерству приглашаются заинтересованные специалисты для взаимовыгодного сотрудничества: уже существует
задокументированная практика и функционирует ряд действующих проектов, требующих развития и поддержки. И будут
появляться новые.

Заинтересован в сотрудничестве с квалифицированными программистами для совместной работы над большими проектами.

Контактные данные:

- почта [mail@scarych.ru](mailto:mail@scarych.ru)
- телеграм [@scarych](https://t.me/scarych)
