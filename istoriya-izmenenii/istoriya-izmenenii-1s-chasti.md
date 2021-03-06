# История изменений 1С-части

## Версия 2.4.7.1 от 29.05.2018

**Минимальная версия для обновления: 2.4.4.42**

**ВНИМАНИЕ! Обмен версии 1 удален. Перед обновлением необходимо перейти на обмен версии 2 \(см. инструкцию по обновлению к версии 2.4.4.40\)**

**Главное**

* Изменена структура главного меню.

### Добавлено:

* Изменена структура главного меню:
  * Уменьшено количество уровней вложенности.
  * Увеличено количество разделов первого уровня. 
* Автоматическое снятие флагов для объектов обмена, относящихся в подсистеме "Виртуальный склад вер. 1", если эта подсистема не установлена.
* Принудительная очистка каталога с временными файлам обмена перед каждым обменом.
* Пересчет цены в ценообразовании по сегментам из валюты управленческого учета в валюту документа.

### Изменено:

* Нет

### Исправлено:

* Конвертация основного склада отгрузки при переходе со старых версий.
* При расчете цены по сегментам номенклатуры, при отсутствии правила теперь возвращается исходная цена, а не нулевая.
* Ошибка, связанная с расчетом цены по сегменту при выборе номенклатуры в заказе поставщику.
* Ошибки в форме установки правил ценообразования по сегментам.

### Удалено:

* Нет.

## Версия 2.4.7.0 от 24.04.2018

**Минимальная версия для обновления: 2.4.4.42**

**ВНИМАНИЕ! Обмен версии 1 удален. Перед обновлением необходимо перейти на обмен версии 2 \(см. инструкцию по обновлению к версии 2.4.4.40\)**

**Главное**

* Добавлена возможность указать скидки \(наценки\) для покупателей на произвольные сегменты номенклатуры.

### Добавлено:

* Возможность указать скидки \(наценки\) для покупателей на произвольные сегменты номенклатуры \(ЗетаСофт - Zeta Web - Каталог и продажи - Ценообразование - Ценообразование по сегментам номенклатуры покупателей\). Принцип работы ценообразования по сегментам следующий:
  * Номенклатура делится на произвольное количество сегментов \(состав сегмента может быть заполнен по схеме СКД, состав сегментов может обновляться регламентным заданием\)
  * Для для номенклатуры, входящей в сегменты могут быть настроены скидки \(наценки\) как для всех покупателей и договоров покупателей в целом, так и для каждого покупателя и договора покупателя в отдельности.
  * Скидка применяется к цене по договору покупателя в том случае, если на нее не были применены другие скидки.

### Изменено:

* В регистре сведений "Связь номенклатуры и узлов" измерения "Узел" и "Номенклатура" стали обязательными. 

### Исправлено:

* Ошибка при создании заказов поставщиков, при импорте заказов покупателей с размещением на виртуальном складе.
* Ошибка получения складов поставщиков виртуального склада.
* Наименование поля "Выпускает грузовые автомобили" в справочнике "Внешний каталог \(Производители\)".

### Удалено:

* Нет.

## Версия 2.4.6.0 от 13.04.2018

**Минимальная версия для обновления: 2.4.4.42**

**ВНИМАНИЕ! Обмен версии 1 удален. Перед обновлением необходимо перейти на обмен версии 2 \(см. инструкцию по обновлению к версии 2.4.4.40\)**

**Главное**

* Добавлена возможность работы с метатегами страниц и основных объектов \(каталога, номенклатуры и т.п\).

### Добавлено:

* Возможность работы с метатегами страниц, каталога сайта, номенклатуры, информационных блоков, марок, моделей, модификаций и узлов \(ЗетаСофт - Zeta Web - Наполнение сайтов - SEO - Управление метатегами\).
  * Поддерживаются два режима заполнения, простой и расширенный. В простом режиме можно указать метатеги для страниц, используя небольшое количество предопределенных переменных. В расширенном режиме можно заполнить метатеги для страниц, используя любые данные, которые можно получить запросом из базы данных.
* В начальные данные включены основные метатеги \(в том числе, метатеги Open Graph\) \(см. ЗетаСофт - Zeta Web - Наполнение сайтов - SEO - Управление метатегами - Метатеги\) и переменные, которые можно использовать для метатегов в заголовках страниц \(см. ЗетаСофт - Zeta Web - Наполнение сайтов - SEO - Управление метатегами - Переменные в заголовках страниц\). 
* Возможность проверки подключения при настройке подключения к виртуальному складу версии 3.

### Изменено:

* Для единицы измерения с кодом 796 \(штука\) в классификаторе единиц измерения принудительно устанавливается международный код "PCE" для того, чтобы при создании новой номенклатуры на стороне сайта не дублировались единицы измерения.
* При запуске контролируется наличие узла плана обмена "Статусы строк заказов".
* Переработаны формы элементов и списков справочников "Внешний каталог \(производители\)", "Внешний каталог \(модели\)", "Внешний каталог \(типы\)", "Внешний каталог \(дерево узлов\)".
* Справочник "Каталог сайта" отображается по умолчанию в свернутом виде. 

### Исправлено:

* Логирование ошибок при загрузке заказа покупателя.
* Ошибка формирования документа "Возврат товаров от покупателя" при заполнении на основании заявки на возврат, оформленной на сайте.
* Ошибка загрузки табличных частей документов при импорте с сайта \(в некоторых случаях табличные части не загружались\).
* При создании нового регламентного задания обмена с сайтом задание создается с пользователем "Сайт".

### Удалено:

* Метатеги, которые заполнялись как реквизиты объектов больше не используются \(справочники "Страницы", "Номенклатура", "Каталог сайта", документ "Информационный блок"\). Данные из этих полей перенесены в регистр "Значения метатегов объектов".
* Удалены реквизиты справочника "Пользователи сайта":
  * Высылать счет по электронной почте, после подтверждения корзины
  * Отображать счет на сайте, после подтверждения корзины.
* Удалено большое количество предопределенных элементов в справочнике "Метатеги".

## Версия 2.4.5.0 от 16.03.2018

**Минимальная версия для обновления: 2.4.4.42**

**ВНИМАНИЕ! Обмен версии 1 удален. Перед обновлением необходимо перейти на обмен версии 2 \(см. инструкцию по обновлению к версии 2.4.4.40\)**

**ВНИМАНИЕ! В следующем релизе в справочнике "Номенклатура" будет удалено поле "Дополнительная информация"**

**Главное**

* Удален обмен версии 1.
* Удалены неиспользуемые объекты.

### Добавлено:

* В панели управления сайтом на закладке "События-Новые заказы" добавлена кнопка снятия фильтра по периоду "За все время". 
* В панели управления сайтом на закладке "События-Новые заказы" фильтр по периодам по кнопкам "За день", "За неделю", "За месяц", "За все время" теперь запоминается и восстанавливается при следующем открытии панели управления сайтом.
* Для настройках домена появилась возможность указать произвольный текст не только после открывающего тэга body, но и перед закрывающим тэгом body. 

### Изменено:

* Поведение флагов "Скрыть заказы созданные в 1С" и "Скрыть корзины пользователей" теперь работает следующим образом: заказами, созданными в 1С считаются все заказы, у которых не заполнен реквизит "Статус \(статус заказа на сайте"\).
* Улучшена диагностика правильности запросов обмена с сайтом.
* При записи номенклатуры без режима ОбменДанными.Загрузка = Истина сразу формируется наименование в URL.

### Исправлено:

* Слишком длинное имя файла обмена для объектов с большим количеством подчиненных объектов.
* Возможность добавления собственного параметра в управляемой форме справочника "Контролы".
* Очистка реквизита "Наименование в URL" при копировании номенклатуры.

### Удалено:

* Удален обмен версии 1.
* Удалено большое количество устаревших объектов метаданных.

## Версия 2.4.4.42 от 19.02.2018

**Минимальная версия для обновления: 2.3.1.0**

**ВНИМАНИЕ! В одной из ближайших версий ZetaWeb планируется удаление обмена версии 1. Рекомендуем вам запланировать переход на обмен версии 2 в ближайшее время \(см. инструкцию по обновлению к версии 2.4.4.40\)**

**Главное**

* Исправлены выявленные ошибки.

### Добавлено:

* Возможность включения и выключения отложенной транслитерации номенклатуры \(ZetaWeb-Настройки и администрирование-Настройки ZetaWeb-Наименования транслитом\). 

### Изменено:

* Изменен принцип поиска номенклатуры, заказанной на внешних складах \(через веб-сервисы WSG или через Виртуальный склад вер. 3\).

### Исправлено:

* Импорт заказов с сайта.
* Отмена регистрации изменений при длительных обменах.
* Отложенная транслитерация номенклатуры.
* Расширение поисковой строки при использовании обмена вер. 2.

### Удалено:

* Нет.

## Версия 2.4.4.41 от 06.02.2018

**Минимальная версия для обновления: 2.3.1.0**

**ВНИМАНИЕ! В одной из ближайших версий ZetaWeb планируется удаление обмена версии 1. Рекомендуем вам запланировать переход на обмен версии 2 в ближайшее время \(см. инструкцию по обновлению к версии 2.4.4.40\)**

**Главное**

* Добавлена возможность импортировать склады из Виртуального склада \(редакции 3.0\), для управления подсветкой и доступностью.

### Добавлено:

* Импорт складов поставщиков из Виртуального склада вер.3 \(версия Виртуального склада не ниже 3.0.0.5, версия подсистемы "Веб-сервисы РММ" не ниже 1.2.2.х\), см. меню "ЗетаСофт-ZetaWeb-Настройки и администрирование-Настройки интеграции с внешними системами-Параметры подключения к виртуальному складу\).
* Автоматическое создание необходимого узла обмена для подсистемы статусов строк заказов.
* В настройки рассылки прайсов пользователей сайта появилась возможность включать архивацию файлов. 

### Изменено:

* Обновлена библиотека работы с веб-сервисами WSG.
* Формы списков и выбора справочников внешних каталогов заменены на управляемые.

### Исправлено:

* Хранение истории транслитерации объектов.

### Удалено:

* Нет.

## Версия 2.4.4.40 от 25.01.2018

**Минимальная версия для обновления: 2.3.1.0**

**ВНИМАНИЕ! В одной из ближайших версий ZetaWeb планируется удаление обмена версии 1. Рекомендуем вам запланировать переход на обмен версии 2 в ближайшее время \(см. инструкцию по обновлению\)**

**Главное**

* Появилась возможность обмениваться таблицами любых размеров в полном обмене и в обмене изменениями.

### Добавлено:

* В обмене версии 2 добавлена возможность устанавливать разделители обмена для полного обмена и обмена изменениями для того, чтобы можно было обмениваться с сайтом таблицами любого размера.
* В обмене версии 2 появилась возможность выполнить обмен с дополнительным экранированием служебных символов XML. Настройка доступна в справочнике "Настройки обмена" - "Служебные параметры" - "Удалять некорректные символы". Эту настройку нужно включить, если при обмене не удается прочитать файл обмена и выключить после того, как обмен пройдет без ошибок \(включенная настройка замедляет чтение файлов обмена\). 
* Настройки обмена с сайтом вынесены в отдельную форму \(доступны из вкладки "Обмен с сайтом" панели управления и из формы настроек ZetaWeb\)
* Расширены проверки корректности настроек обмена версии 2.
* Добавлена возможность отслеживания количества новых сообщений или ответов, непрочитанных пользователем.
* Добавлена возможность установить использование протокола https в панели управления сайтом.

### Изменено:

* Цвет поля "Статуса заказа покупателя на сайте" изменен со светло-золотистого на золотистый.
* Изменена форма лога обмена с сайтом.
* Возможность использования имени домена без префикса "www" в качестве основного доменного имени.

### Исправлено:

* Ошибки регистрации изменений для независимых регистров сведений в обмене версии 2.
* Ошибка записи CSS класса.
* Ошибка, возникающая при обмене с другими конфигурациями \(например, Бухгалтерия предприятия\) через внешнее соединение.
* Ошибка округления нулевой цены \(при округлении в большую сторону нулевая цена округлялась до порядка округления\)

### Удалено:

* Нет.

## Версия 2.4.4.1 от 18.12.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* Добавлена возможность загрузки начальных данных при режиме совместимости конфигурации начиная с 8.3.3.
* В обработке "Настройка логистики" появилась возможность добавить всех поставщиков в форму настройки и скрыть поставщиков, которые уже настроены \(см. закладку "Возможность доставки от поставщиков", кнопки "Заполнить всеми поставщиками", "Скрыть заполненных поставщиков"\). 

### Изменено:

* Форма справочника "Контролы".

### Исправлено:

* Ошибка записи группы справочника контрагенты.
* Формирование статусов строк заказов, если коэффициент для товара в табличной части "Товары" в документе "Заказ покупателя" или "Реализация товаров и услуг" по каким-то причинам ошибочно равен нулю.
* Удаление лога обмена с сайтом при сжатии и удалении периодических данных.
* Ссылочные объекты не регистрировались для обмена с сайтом в обмене вер. 2 при непосредственном удалении.
* Ошибка при создании раздела каталога сайта, привязанного к категории.
* Поле "Исходный артикул" в справочнике кроссов теперь всегда заполняется.
* При настройке оплаты и доставки больше нет возможности не указать поставщика услуги доставки.

### Удалено:

* Нет.

## Версия 2.4.4.0 от 29.11.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* Автоматическое заполнение основного склада отгрузки контрагента для заказов с сайта складом по умолчанию \(в панели управления на закладке "Склады" есть возможность установить или изменить этот склад\).
* В подсистеме "Расчет сроков доставки" появилась возможность указать основной склад отгрузки для региона \(используется на сайте для расчета срока доставки до региона контрагента\). Поле "Склад" для региона в форме "Настройки логистики" на закладке "Возможность доставки в регионы", гиперссылка "Открыть настройки региона"
* В подсистеме "Расчет сроков доставки" появилась возможность указать, что внешний поставщик передает срок доставки до склада компании, а не до своего склада \(например, поставщик, подключенный через веб-сервис, указывает срок доставки для нашего склада\). Флажок "Возвращает срок доставки до нашего склада" в форме "Настройки логистики" на закладке "Графики доставки от поставщика", гиперссылка "Открыть настройки поставщика"  

### Изменено:

* Настройка срока доставки между своими складами в  подсистеме "Расчет сроков доставки" перенесена с закладки "Возможность доставки со склада на склад" на закладку "Графики доставки со склада на склад".
* Изменен порядок определения склада отгрузки \(реквизит "Склад/группа"\) в заказе покупателя, который импортируется с сайта. Склад отгрузки заполняется первым существующим значением в следующем порядке:
  * Склад отгрузки в заказе, созданном на сайте.
  * Основной склад отгрузки заказов с сайта, указанный в карточке контрагента.
  * Основной склад, указанный в настройках пользователя.
* Склад отгрузки, который указывался в справочнике "Пользователи сайта" больше не используется
* Форма элемента справочника "Контролы" переведена в упраляемый режим.
* Изменены некоторые синонимы объектов подсистемы "Zeta Web" \(добавлен суффикс "\(Zeta Web\)"\).

### Исправлено:

* Регламентное задание транслитерации наименований номенклатуры завершалось с ошибкой, если элемент справочника был удален из базы данных.
* В форму справочника "Номенклатура" на закладку "Инфо для сайта-Прочее" выведен реквизит "Ед. кратности продаж".
* В обмене данными версии 2 исправлена ошибка обмена табличными частями.
* Исправлена ошибка отображения на сайте свойств номенклатуры с типом "Булево".
* В форме элемента справочника "Внешний каталог \(типы\)" выведен реквизит "Двигатель" \(Engine\). 

### Удалено:

* Реквизит "СкладГруппа" в справочнике "СайтПользователи".

## Версия 2.4.3.3 от 29.10.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* Добавлен отчет "Анализ остатков по номенклатуре для Управления Торговлей, ред.10.3"\(ЗетаСофт-ZetaWeb-Каталог и продажи\). Отчет предназначен для сверки остатков на сайте и в базе данных 1С.

### Изменено:

* Рекомендуется перейти на обмен данными версии 2.
  * В панели управления сайтом добавлена закладка "Обмен с сайтом"
  * Закладка "Обмен с сайтом" на закладке "Настройки" переименована в "Обмен с сайтом, вер.1"
  * Перед переходом на новую версию обмена необходимо обязательно выключить все регламентные задания, относящиеся к обмену версии 1.

### Исправлено:

* Исправлены выявленные ошибки.

### Удалено:

* Нет.

## Версия 2.4.3.2 от 24.10.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* Форма настройки ценообразования на внешние остатки в панели управления сайтом.
* Добавлена автоматическая регистрация заказов поставщиков и складов поставщиков в группах доступности складов для тех настроек, в которых не указано размещение.

### Изменено:

* Изменена закладка "Спец.цены" в панели управления сайтом. Закладка переименована в "Ценоборазование", на нее вынесены дополнительные настройки ценообразования, относящиеся к работе сайта.

### Исправлено:

* Ошибка регистрации удаления данных независимых регистров сведений в бета-версии обмена данными сайтом версии 2.
* Исправлены выявленные ошибки.

### Удалено:

* Нет.

## Версия 2.4.3.1 от 16.10.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* Нет.

### Изменено:

* Нет.

### Исправлено:

* Исправлены выявленные ошибки.

### Удалено:

* Нет.

## Версия 2.4.3.0 от 15.10.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* Подсистема "Расчет сроков доставки" предназначенная для возможности задать и рассчитать сроки доставки от поставщиков до своих складов, между своими складами, и от своих складов до регионов покупателей \(см. "ЗетаСофт - ZetaWeb - Доставка - Расчет сроков доставки"\).
* Подсчет количества объектов в обмене в бета-версии обмена данными сайтом версии 2.
* Возможность ручного обмена одним объектом обмена из настройки обмена в бета-версии обмена данными сайтом версии 2.
* Добавлена возможность для контрагента указать склад отгрузки по умолчанию для заказов, сделанных на сайте \(закладка "Прочее" в карточке контрагента\)

### Изменено:

* Изменен внешний вид меню "ZetaWeb", объекты подсистем "ZetaWeb",  сгруппированы по их функциональному назначению.

### Исправлено:

* Ошибка выбора типа группы в группе каталога сайта.
* Ошибка регистрации данных независимых регистров сведений в бета-версии обмена данными сайтом версии 2.
* Исправлены выявленные ошибки.

### Удалено:

* Нет

## Версия 2.4.2.2 от 18.09.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* В бета-версию обмена данными добавлена проверка настроек подсистемы обмена.
* В бета-версию обмена данными добавлена возможность подсчета количества объектов для обмена в настройке обмена.
* CSS классы в верстке можно указывать не только как ссылку на справочник, но и как строку.

### Изменено:

* Выполнена подготовка к удалению стархы объектов метаданных.

### Исправлено:

* Исправлены выявленные ошибки.

### Удалено:

* Нет.

## Версия 2.4.2.1 от 13.09.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* Бета-версия обмена данными сайтом версии 2.

### Изменено:

* Изменен формат вывода имени файлов \(css, js и т.п.\) с GUID на имя объекта, если оно заполнено. 

### Исправлено:

* исправлены выявленные ошибки.

### Удалено:

* Нет.

## Версия 2.4.2.0 от 07.09.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* Нет.

### Изменено:

* Нет.

### Исправлено:

* Ошибка создания кросса "сам на себя" для номенклатуры без артикулов.

### Удалено:

* Нет.

## Версия 2.4.1.2 от 03.09.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* Нет.

### Изменено:

* Внешний вид некоторых форм.

### Исправлено:

* Исправлены выявленные ошибки.

### Удалено:

* Нет.

## Версия 2.4.1.1 от 24.08.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* В справочнике "Договоры контрагентов" добавлено поле "Запретить продажу товаров в рознице на сайте по условиям договора \(не по розничнным ценам\). Для таких договоров для складов - автоматизированных торговых точек на сайте будут показываться цены автоматизированной торговой точки.
* В справочнике "Настройки обмена" добавлено поле "Таймаут", которое прерывает обмен, если при завершении экспорта таблиц на сайт по каким-то причинам не приходит ответ. По умолчанию, при смене вида обмена для полного обмена устанавливается таймаут в 3600 сек, для обмена изменениями - 900 сек.

### Изменено:

* Нет.

### Исправлено:

* Исправлены незначительные ошибки.

### Удалено:

* Нет.

## Версия 2.4.1.0 от 17.08.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* Возможность делить номенклатуру, продаваемую совместно на группы:
  * Справочник "Группы номенклатуры, продаваемой совместно" \(ЗетаСофт - Zet Web - Номенклатура, продаваемая совместно\).
    * Регистр сведений "Номенклатура, продаваемая совместно" \(ЗетаСофт - Zet Web - Номенклатура, продаваемая совместно\).
* Группы доступности складов теперь можно уточнить для контрагента, договора контрагента и пользователя сайта \(см. формы элементов соответствующих объектов\).

### Исправлено:

* Исправлены ошибки при работе клиента WSG.

## Версия 2.4.0.1 от 16.08.2017

**Минимальная версия для обновления: 2.3.1.0**

### Добавлено:

* Форма для управления веб-сервисами WSG.
* В справочнике "Точки выдачи контрагентов" добавлен реквизит "Склад отгрузки", который используется в качестве склада отгрузки при выборе точки отгрузки.
* В обработке "Настройка доставки и способов оплаты" добавлена проверка на корректность записей в регистре настройки.

### Исправлено:

* Ошибка записи при отложенной транслитерации номенклатуры.
* Ошибка конвертации групп доступности складов при переходе на версию 2.4.0.0.
* Ошибка применения ручных скидок.
* Ошибка при загрузке новых данных сайта при обновлении.

### Удалено:

* Нет.

## Версия 2.4.0.0 от 07.08.2017

### Добавлено:

* Добавлена подсистема работы с вненшними остатками \(через веб-сервисы поставщиков и через внешний виртуальный склад\), которая позволяет работать с отстатками поставщиков, не храня номенклатуру в собственной базе:
  * Форма настроек подключения к WSG \(веб-сервисы поставщиков\) и к внешним каталогам кроссов \(ЗетаСофт - Zet Web - Администрирование - Настройки WSG и внешних каталогов автозапчастей\).
  * Форма настроек подсветки и наименования складов для новых контролов поиска \(ЗетаСофт - Zet Web - Склады поставщиков и правила ценообразования - Описания складов поставщиков\).
  * Форма настроек ценообразования на остатки веб-сервисов и внешнего виртуального склада \(ЗетаСофт - Zet Web - Склады поставщиков и правила ценообразования - Правила ценообразования на внешние остатки\),
  * Форма настроек сроков групп доступности складов с учетом внешних складов \(ЗетаСофт - Zet Web - Склады поставщиков и правила ценообразования - Группы доступности складов\).
  * Форма настроек сроков доставки от поставщика на склад \(ЗетаСофт - Zet Web - Доставка - Внутренняя логистика - Настройка логистики\).
  * Форма "О программе", в которую сведена информация о версиях различных компонент программного комплекса Zeta Web.
* Добавлено большое количество служебных элементов метаданных для перехода в будущем на другую систему хранения данных о сайтах.

### Изменено:

* Поведение заявки на возврат:
  * Разрешено редактирование размещения.
  * Заполнение размещения выполняется автоматически, если это конфигурация УТ 10.3 и это операция возврата, то заполнение производится из склада продажи документа основания - заказа покупателя\).
* Планы обмена данными с сайтом разделены на план обмена данными сайта и план обмена данными конфигурации.

### Исправлено:

* В объектах конфигурации исправлена принадлежность табличной части "Товары" документа "Реализация товаров услуг".
* Исправлен обмен с сайтом по защищенному протоколу для платфоры 8.3.10.
* Исправлены некоторые запросы обмена данными.
* Исправлена ошибка с очисткой идентификатора строки заказа при копировании строки в табличной части "Товары".

### Удалено:

* Нет.

## Версия 2.3.1.0 от 09.06.2017

### Добавлено:

* В настройках добавлена обязательная проверка заполнения вариантов использования кроссов.
* Поддержка онлайн касс \(только совместно с платежной системой Яндекс.Деньги\). В справочнике "Настройки платежных систем" появились соответствующие настройки.

### Изменено:

* Нет.

### Исправлено:

* Увеличена длина идентификатора купона в документе "Заказ покупателя".
* Неверное сообщение об ошибке обмена, если обмен выполнялся без архивирования файлов.

### Удалено:

* Удален ряд неактуальных объектов.

## Версия 2.2.5.1 от 08.05.2017

### Добавлено:

* Добавлена совместимость со справочником "Типы оплат" в конфигурациях Альфа-Авто для поддержки оплат сайта.

### Изменено:

* Обмен с сайтом в части импорта объектов, изменяемых на сайте \(проведен рефакторинг\).

### Исправлено:

* При обновлении внутренних данных сайта устаревшие объекты снимаются с поддержки.
* Баннеры с неуказанным сроком действия теперь не попадают в отображение архивных баннеров.
* При копировании заказа очищается уникальный код заказа на сайте.
* Исправлены незначительные ошибки.

### Удалено:

* Нет.

## Версия 2.2.5.0 от 12.05.2017

### Добавлено:

* При настройке обмена добавлена возможность выбрать режим обмена - "Проверка полного обмена \(5000 эл. на объект\)", режим предназначен для тестирования полной выгрузки. При выборе этого режима обмена полная выгрузка будет ограничена 5000 элементов на каждый объект обмена.
* В форме списка справочника "Объекты конфигурации" добавлена возможность редактирования запросов \(повышено удобство редактирования запросов, старый механизм редактирования запросов через справочник "Виды конфигураций" пока сохранен\).
* Добавлена возможность обмена разными объектами конфигурации в одном файле обмена \(например, таблицей заказов покупателя и таблицей товаров заказов покупателя\). Для этого нужно выбрать основной объект обмена и в связанных объекта обмена в поле "Родительский объект обмена" указать основной объект обмена. По умолчанию такой обмен установлен для заказа покупателя и реализации товаров.

### Изменено:

* В карточке номенклатуры убрана видимость поля "Группа синонимов".
* Убран код для справочников, включенных в механизм версионности.

### Исправлено:

* Повышена совместимость с платформой 8.2.
* Управляемая форма элемента для справочника "Каталог" для конфигураций "Альфа-Авто".
* Стандартизировны некоторые запросы для конфигураций "Альфа-Авто".
* Исправлены выявленные ошибки.

### Удалено:

* В справочнике "Объекты конфигурации" удалены все предопределенные элементы кроме корневых. Целостность данных поддерживается на уровне механизма версионности \(см. описание релиза 2.2.0.0\) после обновления может быть снята ранее установленная пометка удаления для элементов справочника "Объекты конфигурации \(Зета Web\)".

## Версия 2.2.4.0 от 30.04.2017

### Добавлено:

* В механизм поддержки версионности данных сайта добавлены все данные, относящиеся к базовой функциональности \(ядру\) сайта.
* Обмен с сайтом теперь может работать по протоколу https.
* Поддержка функциональности "суперпользователь" \(см. документацию\).

### Изменено:

* Устаревшие объекты поставлены в очередь на удаление \(будут удалены в ближайших релизах\).

### Исправлено:

* Неверная регистрация регистров сведений в плане обмена "Статусы строк заказов" удалена.

### Удалено:

* Из механизма подержки версионности данных сайта исключен справочник "Шаблоны контролов".

## Версия 2.2.2.1 от 06.04.2017

### Добавлено:

* Отбор в журнале сообщений - "За сегодня", "За последнюю неделю", "За последний месяц".
* В регистры запрещенной и разрешенной номенклатуры добавлен отбор по роли, внесены измения в соответствующие запросы обмена.

### Изменено:

* Отбор в журнале пользователй "За текущую неделю" изменено на "За последнюю неделю", "За текущий месяц" изменено на "За последний месяц".

### Исправлено:

* Ошибка обмена статусов строк заказов.
* Выбор региона по умолчанию в контроле "Текущий регион пользователя".
* Небольшие изменения в отнесение объектов к подсистемам.

### Удалено:

* Нет.

## Версия 2.2.2.0

### Добавлено:

* Нет.

### Изменено:

* Внесены небольшие изменения для повышения совместимости с конфигурациями Альфа-Авто.
* Изменены некоторые синонимы реквизитов объектов.

### Исправлено:

* Исправлена ошибка редактора шаблонов контрола \(можно было произвольно менять порядок параметров группы частей шаблона\).

### Удалено:

* Нет.

## Версия 2.2.1.0 от 06.02.2017

### Добавлено:

* В менеджере справочника "Сообщения Zeta Web" добавлена функция создания сообщений для сайта.

### Изменено:

* Обновлены описания и состав типовых параметров некоторых контролов.

### Исправлено:

* Нет.

### Удалено:

* Нет.

## Версия 2.2.0.0 от 30.01.2017

### Добавлено:

* Новая подсистема обновления, хранения и редактирования внутренних данных Zeta Web.
* Внутренние данные Zeta Web хранятся в разрезе релизов. Подсистема позволяет автоматически обновлять данные на поддержке и контролировать изменения данных, которые изменены вручную.
* Добавлена обработка "Обновление внутренних данных Zeta Web" предназначеная для трехстороннего сравнения и объединения данных при обновлении сайта.
* Список поддерживаемых в этой версии объектов данных:
  * Справочники:
    * ЗетаWEBКонтролы
    * ЗетаWEBТипыПараметровКонтролов
    * ЗетаWEBТиповыеПараметрыКонтролов
    * ЗетаWEBВариантыШаблоновКонтрола
    * ЗетаWEBТиповойСоставВариантаШаблонаКонтрола
    * ЗетаWEBШаблоныКонтролов
    * ЗетаWEBОбъектыКонфигурации
  * Регистры сведений:
    * ЗетаWEBЗначенияЗапросовКОбъектамКонфигураций
    * ЗетаWEBСоответствияИменОбъектовОбмена
    * ЗетаWEBСоответствияПолейОбъектовПриЗагрузке"

### Изменено:

* Обновлены описания и состав типовых параметров большого количества контролов.

### Исправлено:

* Нет.

### Удалено:

* Нет.

## Версия 0.0.0.0 от

**Минимальная версия для обновления: 0.0.0.0**

**Главное**

* нет

### Добавлено:

* Нет.

### Изменено:

* Нет.

### Исправлено:

* Нет.

### Удалено:

* Нет.

