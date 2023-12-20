![image](https://github.com/dimilka/Analisist_lab_2/assets/46933758/fa2cc77d-1259-418b-8035-9b6bf05f0011)

# Цель работы:
Знакомство с облачными сервисами. Понимание уровней абстракции над инфраструктурой в облаке. Формирование понимания типов потребления сервисов в сервисной-модели. Сопоставление сервисов между разными провайдерами. Оценка возможностей миграции на отечественные сервисы.

# Дано:
1. Слепок данных биллинга от провайдера после небольшой обработки в виде SQL-параметров. Символ % в начале/конце означает, что перед/после него может стоять любой набор символов.
2. Google с документациями провайдера.

# Ход работы
1. Импорт .csv файла в Excel.
2. Поиск и анализ информации о сервисах Azure.
3. Формирование таблицы "Описание сервисов Azure".
4. Поиск отечественных аналогов и инофрмации о них. Параллельное заполнение таблиц "Описание отечественных сервисов" и сопоставления.
5. Анализ ситуации на облачном рынке и формирования суждения о возможности миграции с зарубжных сервисов на российские.

# Описание сервисов Azure

В таблице представлено описание рассмотренных сервисов Microsoft Azure.

| Сервис | Описание|
|----------|----------|
| Data Lake Store    | Хранилище данных, предназначенное для накопления больших объемов структурированных, полуструктурированных и неструктурированных данных. Это репозиторий для хранения всех видов данных в их первоначальном формате без жестких ограничений по размеру учетной записи или файла. Data Lake сохраняет большие объемы данных с целью повышения интеграции данных и производительности аналитических процессов.  |
| Data Management (предположительно речь идёт о Data Manager) | Azure Data Manager является мощной облачной службой, специально разработанной для организации и управления процессами интеграции и трансформации данных. Платформа предоставляет комплексные инструменты и услуги, которые позволяют эффективно управлять потоком данных между различными источниками.|
| Data Services   | Комплекс облачных сервисов и инструментов, предоставляемых Microsoft Azure, для работы с данными и анализа информации. Эти службы обеспечивают возможности сбора, хранения, обработки, анализа и визуализации данных в облачной среде.   |
|SQL Data Warehouse|Облачня система управления базами данных, предназначенная для обработки больших объемов данных из различных источников. Сервис обеспечивает колоночное хранение данных и горизонтальное масштабирование ресурсов. Оптимизирован для запросов и анализа данных с помощью SQL.|
|Functions|Облачный сервис, который позволяет разработчикам создавать и развертывать микросервисы и функции, работающие в реакции на события и триггеры без необходимости управления инфраструктурой|
|Traffic Manager|Балансировщик нагрузки на основе DNS, который управляет распределением пользовательского трафика к конечным точкам обслуживания в различных центрах обработки данных. Использует метод маршрутизации трафика, а также проверяет состояние конечных точек.|
|Azure Firewall|Управляемая облачная служба сетевой безопасности, которая обеспечивает защиту ресурсов виртуальных сетей Azure. Это высокоэффективный брандмауэр, который предоставляет функции межсетевого экранирования, инспекции пакетов и фильтрации трафика, а также интегрируется с другими службами Azure для обеспечения комплексной защиты сети и приложений.|
|Notification Hubs|Высокомасштабируемый движок отправки мобильных уведомлений, предназначенный для быстрой отправки миллионов уведомлений на устройства iOS, Android, Windows или Kindle. Он сотрудничает с APNs, GCM, WNS и другими сервисами.|
|Power BI|Мощная платформа для бизнес-аналитики и визуализации данных, предоставляемая Microsoft. Она позволяет организациям собирать, анализировать и визуализировать данные из различных источников, чтобы принимать более обоснованные бизнес-решения.|
|Power BI Embedded|Служба визуализации данных, предоставляемая Microsoft Power BI, которая позволяет встраивать интерактивные отчеты и дашборды Power BI в собственные приложения, веб-сайты или приложения для мобильных устройств.|
|Recovery Services|Cлужба, предоставляемая Microsoft Azure, которая специализируется на резервном копировании данных и восстановлении информации в случае непредвиденных сбоев или катастроф. Она предоставляет организациям средства для создания резервных копий данных и систем, а также для восстановления их работоспособности в случае потери или повреждения данных.|
|Scheduler (вышел из эксплуатации и заменен Azure Logic Apps)| Azure Logic Apps - облачная служба интеграции, которая помогает организациям автоматизировать свои бизнес-процессы. Она позволяет пользователям быстро и легко создавать автоматизированные рабочие процессы с использованием графического пользовательского интерфейса, без необходимости писать код.|
|Sentinel|Облачный сервис управления информацией о безопасности и событиях (SIEM), предоставляемый Microsoft Azure. Он разработан для помощи организациям в обнаружении, исследовании и реагировании на угрозы и инциденты в их облачных и локальных средах.|
|SQL Advanced Threat Protection|Сервис обнаруживает аномальные действия, указывающие на необычные и потенциально опасные попытки доступа к базам данных или их использования. Может выявлять потенциальные SQL-инъекции, доступ из необычного расположения или дата-центров, доступ из незнакомого или потенциально опасного приложения.|
|Advanced Data Security|Набор возможностей безопасности, предлагаемых в рамках Azure SQL Database и SQL Managed Instanc. Он включает в себя функциональность для обнаружения и защиты от угроз, таких как вредоносные или подозрительные активности, а также предоставляет инструменты для оценки уязвимостей и управления безопасностью баз данных.|
|SQL Database| Облачная служба, предназначенная для хранения и управления реляционными базами данных с использованием языка SQL. |

# Описание отечественных сервисов

В таблице представлено описание российских сервисов, являщихся аналогами сервисов Azure.

| Сервис | Описание|
|----------|----------|
|Yandex Object Storage|Универсальное масштабируемое облачное объектное хранилище. Объекты в Object Storage хранятся в нескольких географически распределённых зонах доступности. Также, объектное хранилище S3 автоматически расширяется по мере необходимости.|
|Yandex Cloud Data Transfer|Cервис, предназначенный для эффективной интеграции и передачи данных между различными источниками и назначениями в облачной среде. Облегчает процесс миграции данных в облако Yandex, поддерживает широкий спектр форматов и источников данных.|
|ClickHouse|Развёртываемая с помощью Yandex Managed Service for ClickHouse в Yandex Cloud колоночная система управления базами данных. Система масштабируема, что позволяет ей обрабатывать большие объемы данных. Заточена под анализ данных и использует собственный диалект SQL, близкий к стандартному, но содержащий различные расширения.|
|Yandex Cloud Functions|Cервис бессерверных вычислений, позволяющий пользователям выполнять код в ответ на различные события без необходимости заботиться о базовой инфраструктуре. Это означает, что разработчики могут сосредоточиться на написании кода функций, а Yandex Cloud автоматически управляет вычислительными ресурсами, необходимыми для его выполнения.|
|Yandex Cloud Load Balancer|Балансировщик сетевой нагрузки. Помогает обеспечить отказоустойчивость приложений за счет равномерного распределения нагрузки по облачным ресурсам. Сервис позволяет создавать сетевые балансировщики нагрузки и объединять облачные ресурсы в группы целей, между которыми может распределяться трафик. Для ресурсов из группы целей, подключенных к балансировщику нагрузки, регулярно осущетсвляются проверки работоспособности, что обеспечивает передачу трафика только на работающие ресурсы.|
|Yandex DataLens|Сервис аналитики и визуализации данных. Он позволяет пользователям легко анализировать данные из различных источников, создавать интерактивные отчеты и информативные панели управления. Сервис предназначен для бизнес-аналитиков, менеджеров и других пользователей, которым необходимо принимать решения на основе данных.|
|Yandex Cloud Backup|Сервис резервного копирования, позволяющий пользователям эффективно создавать, управлять и восстанавливать резервные копии своих данных и приложений, размещенных в облаке Yandex. Он обеспечивает безопасное хранение данных и их защиту от потерь или повреждений.|
|Yandex Managed Service for SQL Server|Облачный сервис от Yandex, который предоставляет полнофункциональную среду для работы с Microsoft SQL Server с мерами безопасности, включающими шифрование, управление доступом, мониторинг и защиту от вредоносного программного обеспечения.|

# Итоговая таблица сопоставления

| Meter Category                 | Meter Sub-Category   | Meter Name                    | Consumed Service              |                  | Russian equivalent                    |
|--------------------------------|----------------------|-------------------------------|-------------------------------|------------------|---------------------------------------|
| Data Lake Store                |                      | Pay-as-you-go Data at Rest    | Microsoft.DataLakeStore       |                  | Yandex Object Storage                 |
| Data Lake Store                |                      | %Transactions%                | Microsoft.DataLakeStore       |                  | Yandex Object Storage                 |
| Data Management (Data Manager) |                      | Geo-Replicated Data Transfer% |                               |                  | Yandex Cloud Data Transfer            |
| Data Management (Data Manager) | Geo Redundant        |                               |                               |                  | Yandex Cloud Data Transfer            |
| Data Management (Data Manager) |                      |                               |                               |                  | Yandex Cloud Data Transfer            |
| Data Services                  |                      |                               |                               |                  | None                                  |
| SQL Data Warehouse             | Compute Optimized%   | 100 DWUs                      | Microsoft.Sql                 |                  | ClickHouse                            |
| Functions                      |                      | %Execution%                   | Microsoft.Web                 |                  | Yandex Cloud Functions                |
| Functions                      |                      | %Duration                     | Microsoft.Web                 |                  | Yandex Cloud Functions                |
| Traffic Manager                |                      | %Azure Endpoint%              | Microsoft.Network             |                  | Yandex Cloud Load Balancer            |
| Traffic Manager                |                      | %Service Endpoint%            | Microsoft.Network             |                  | Yandex Cloud Load Balancer            |
| Traffic Manager                |                      | %DNS Queries%                 | Microsoft.Network             |                  | Yandex Cloud Load Balancer            |
| Traffic Manager                |                      | %Real User Measurements       | Microsoft.Network             |                  | Yandex Cloud Load Balancer            |
| Traffic Manager                |                      | %Traffic View%                | Microsoft.Network             |                  | Yandex Cloud Load Balancer            |
| Azure Firewall                 |                      | Deployment                    | Microsoft.Network             |                  | None                                  |
| Azure Firewall                 |                      | Data Processed                | Microsoft.Network             |                  | None                                  |
| Notification Hubs              |                      |                               | Microsoft.NotificationHubs    |                  | None                                  |
| Power BI                       | Embedded             |                               | Microsoft.PowerBI             |                  | Yandex DataLens                       |
| Power BI Embedded              | Power BI Embedded    | A1 Node                       | Microsoft.PowerBIDedicated    |                  | Yandex DataLens                       |
| Power BI Embedded              |                      | A1                            | Microsoft.PowerBIDedicated    |                  | Yandex DataLens                       |
| Recovery Services              | Backup               | Protected Instances           |                               |                  | Yandex Cloud Backup                   |
| Recovery Services              | Site Recovery        | VM replicated to Azure        | Microsoft.RecoveryServices    |                  | Yandex Cloud Backup                   |
| Scheduler                      | Scheduler            | Free Scheduler Units          |                               |                  | Yandex Cloud Functions                |
| Scheduler                      | Scheduler            | Standard Scheduler Units      |                               |                  | Yandex Cloud Functions                |
| Scheduler                      |                      | Free Unit                     | Microsoft.Scheduler           |                  | Yandex Cloud Functions                |
| Scheduler                      |                      | Standard Unit                 | Microsoft.Scheduler           |                  | Yandex Cloud Functions                |
| Sentinel                       |                      | Free Trial                    | microsoft.operationalinsights |                  | Yandex Cloud Security Command Center  |
| Sentinel                       |                      | Analysis                      | microsoft.operationalinsights |                  | Yandex Cloud Security Command Center  |
| SQL Advanced Threat Protection |                      | %Nodes                        | Microsoft.Sql                 |                  | None                                  |
| Advanced Data Security         |                      | Standard%Node                 | Microsoft.Sql                 |                  | Yandex Managed Service for SQL Server |
| SQL Database                   |                      | Database Units%               | Database                      |                  | Yandex Managed Service for SQL Server |
| SQL Database                   | LTR Backup Storage   | Data Stored                   |                               |                  | Yandex Managed Service for SQL Server |
| SQL Database                   | Managed Instance%    |                               | Microsoft.Sql                 |                  | Yandex Managed Service for SQL Server |
| SQL Database                   | Single/Elastic Pool% | vCore                         | Microsoft.Sql                 |                  | Yandex Managed Service for SQL Server |
| SQL Database                   | Elastic Pool%        | eDTUs                         | Microsoft.Sql                 |                  | Yandex Managed Service for SQL Server |
| SQL Database                   | SingleDB Hyperscale% | vCore                         | Microsoft.Sql                 |                  | Yandex Managed Service for SQL Server |
| SQL Database                   | Single%              | %DTUs                         | Microsoft.Sql                 |                  | Yandex Managed Service for SQL Server |
| SQL Database                   | Compute Reservation  | Usage                         | Microsoft.Sql                 | %SLO_: _MIBC%G5% | Yandex Managed Service for SQL Server |
| SQL Database                   | Compute Reservation  | Usage                         | Microsoft.Sql                 | %SLO_: _MIGP%G5% | Yandex Managed Service for SQL Server |
| SQL Database                   |                      |                               | Microsoft.Sql                 |                  | Yandex Managed Service for SQL Server |

# Выводы о возможностях миграции
На данный момент не каждый сервис Microsoft Azure имеет прямой аналог на отечественном технологическом рынке. Однако компания Yandex уже покрывает практически весь функционал облачных сервисов зарубежного конкурента.

Кроме того, по прогнозам Stack Group по итогам года рост российского облачного рынка составит не менее 40%, что говорит о востребованности данной отрасли и её развитии.

Также благоприятно на процесс импортозамещения сервисов Azure может повлиять официальное заявление Microsoft о прекращении работы на территории РФ, сигнализирующее о необходимости поиска своих решений и достижения технологической независимости отечественных компаний.

Совокупность данных фактов говорит о том, что миграция возможна, а российский облачный рынок практически полностью готов к ней.
