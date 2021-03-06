Changelog
=========

3.07.02 (Пре-релиз)
^^^^^^^^^^^^^^^^^^^^^^^

* Админка - Исправлена иногда возникающая ошибка Undefined variable: _COOKIE
* Админка::Тип устройств пользователей - добавлена проверка на использование перед удалением.
* Админка::IP Pool - Добавлено массовое добавление IP Pool на тарифы.


3.07.01 bugfix (19.02.2021)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Админка::Онлайн - исправлено отображение онлайна
* Админка::Поиск - исправлен поиск по адресу
* Админка::Быстрый поиск - исправлено отображение кол-ва найдених записей
* Админка::Выкидывание - исправлена ошибка когда абонент оставался висеть "онлайн" после выкидывания.
* Админка::Платежные системы - исправлена ошибка проверки подписи в ЦКасса.


3.06.05 (18.02.2021)
^^^^^^^^^^^^^^^^^^^^^^^

* Админка::Консольные команды - добавлена команда iptv_user_sync для синхронизации подписок указанного абонента
* Админка::Консольные команды - добавлена команда iptv_sub_sync для синхронизации абонентов с указанной подпиской
* Админка::Карта абонента - исправлено отображение карты при проблеме с устройством абонента.
* Админка::Онлайн - оптимизация получения данных и кол-во отправляемой информации.
* Админка::IP Pools - добавлены поля для ввода DNS1 и DNS2.
* Админка::Тарифы - Переименована вкладка в свойствах тарифа с IP Pools в Dynamic Pools
* Админка::Тарифы - В свойства тарифа добавлена вкладка Real IP Pools
* Админка::Карта абонента - Выдача реального IP абонента из Real IP Pools тарифа (если добавлены).
* Админка::Снятия АП - исправлена ошибка приводившая к игнорированию пополнения, если оно было совершено в момент снятия АП.
* Админка::Абоненты - подготовка к переходу на использование одной таблицы users.
* Админка::Поиск - оптимизация запроса поиска.
* Личный кабинет - Исправлена кодировка в примечании к платежу за реальный IP.
* Личный кабинет - Исправлено отображение комиссии в плат.системе Тиньков
* Личный кабинет - Исправлена ошибка кодировки при смене пароля на кириллицу.
* Личный кабинет - Добавлен вызов mb_event_ticket_open.sh при создании тикета.
* Личный кабинет - Добавлен вызов mb_event_ticket_message.sh при добавлении сообщения в тикет.
* Личный кабинет - Исправлена локализация в шаблонах.
* Личный кабинет - Выдача реального IP абоненту из Real IP Pools тарифа (если добавлены)
* Ядро - оптимизация работы с accounting.
* Ядро - Fix работы Mikrotik RADIUS DHCP на v6.46 и выше.
* Ядро - добавлен тайминг обработки запросов.
* Ядро::Accel V2 - добавлена выдача шлюза, маски, dns из Real IP Pool.
* Ядро::Nokia 7750SR - добавлена выдача шлюза, маски, dns из Real IP Pool.
* Ядро::Cisco ASR - добавлена выдача шлюза, маски, dns из Real IP Pool.
* Wiki: Real IP: выдача из IP Pool


3.06.04 (26.01.2021)
^^^^^^^^^^^^^^^^^^^^^^^^

* Админка::Отчеты - исправлена ошибка в отчете "максимум трафика".
* Админка::Тикеты - добавлен перевод переменных в логах тикетов.
* Админка::Платежи - исправлена кодировка в платеже "за подключение".
* Админка::MAC на портах - исправлена ошибка при обработке абонентов.
* Админка::Поиск - исправлена ошибка при поиске абонентов по IP
* Админка::Сегменты - исправлена ошибка при указании range в сегменте.
* Админка::Выкидывание - добавлено экранирование параметров передаваемых на radclient
* Админка::Скрипты - добавлено экранирование параметров передаваемых на запускаемые скрипты
* Личный кабинет - добавлено уведомление с информацией "о переходе" на тариф с нового месяца.
* Личный кабинет - исправлена ошибка отображения страниц при активации/деактивации услуги "Реальный IP".
* Ядро - добавлено экранирование параметров передаваемых на radclient
* Ядро - добавлено экранирование параметров передаваемых на запускаемые скрипты
