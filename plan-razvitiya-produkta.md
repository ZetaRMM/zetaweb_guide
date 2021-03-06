# План развития продукта



## **План развития продукта Zeta Web**

Наш продукт постоянно развивается, получает новые функции и улучшения \([история версий](istoriya-izmenenii/)\).  

Естественно, работа над оптимизацией, исправлением ошибок и улучшением производительности тоже идёт непрерывно.

### Описание формата версий или “что важно понимать”:

**n.v.x.y** - общий формат номера релиза продукта, где:

**n** - глобальная ветка развития. Основа продукта.

**v** - номер мажорного \(старшего\) релиза, версия определяющая функционал на уровне подсистем и важных изменений.

**x** - номер минорного \(младшего\) релиза. Как правило, включает функционал на уровне контролов и частей контролов.

**y** - номер сборки, их может быть неограниченное количество, при этом номера веб-части и 1С-части могут иметь разницу. Как правило, сюда попадают задачи, которые не влияют на функциональность продукта, и включают в себя оптимизации, исправление ошибок и т.п.

Продукт включает в себя как 1С-часть, так и веб \(состоящую из файлов сайта и базы данных сайта\).

Для корректной работы продукта очень важно иметь совместимые части \(чтобы 1С-часть и веб-часть имели одинаковые версии в рамках n.v.x и представляли собой одно целое\).

### Совместимость частей:

**n** - несовместимы

**v** - вероятно, несовместимы

**x** - совместимы, с определенной потерей функционала. Например, разработаны новые контролы или части шаблонов контролов, но при этом “старая” 1С еще не содержит новых контролов и частей шаблонов, и нет возможности их использовать.

**y** - не влияет на совместимость.

#### Чем отличаются редакция 1 от редакции 2?

* в редакции 1.х продукт был полностью объединен с одной из типовых конфигураций 1С \(Управление торговлей, Альфа-авто и т.п.\)
* в редакции 2.х продукт представляет собой отдельную конфигурацию на поддержке.

#### На что это повлияло?

* скорость разработки и внесения изменений увеличилась на порядок
* трудоемкость и сложность обновления снизилась на порядок
* редакция 1.х более не поддерживается

### Кратко о предыдущих релизах:

* редакция 2.0 - переход на новую редакцию продукта
* редакция 2.1 - подсистема “Возвраты товаров”
* редакция 2.2 - большой объем рефакторинга и доработок, в том числе внешнего каталога Laximo, подсистемы обмена сообщениями и т.д.
* редакция 2.3 - новая подсистема “Система управления подчиненными пользователями”, новая структура настройки стоимости доставки товаров, поддержка ФЗ-54

### Текущая версия:

* редакция 2.4 - новый поиск по артикулам товаров, с возможностью использования веб-сервисов поставщиков
  * редакция 2.4.1 - группы сопутствующих товаров, поддержка розничного ценообразования для товаров с розничных складов
  * редакция 2.4.2 - вывод списка кросс-кодов товара в результатах поиска,  Возможность "быстрой" регистрации \(по номеру телефона / адресу электронной почты\), возможность автоматической регистрации при оформлении заказа анонимным клиентом.
  * редакция 2.4.3 - новая подсистема обмена с сайтом со стороны 1С-части
    * увеличение скорости и надежности обмена
    * новая система логирования
    * улучшенный интерфейс управления
    * регистрация изменений в индивидуальных узлах планов обмена для каждого объекта обмена \(чтобы ошибка обмена для одного объекта обмена не влияла на обмен другими объектами\)
    * проверочный инструмент для сравнения остатков товаров в 1С с расчетной формулой остатков на сайте.
  * редакция 2.4.4 - новая подсистема доставки, включающая в себя внутреннюю логистику и полное прохождение срока доставки товаров от закупки до продажи
    * ряд оптимизаций и исправлений
  * редакция 2.4.5 - удаление старой подсистемы обмена с сайтом
    * возможность размещения текста перед закрывающим тегом body
  * редакция 2.4.6 - новая подсистема работы с мета-тегами
    * общий механизм работы с мета-тегами, в т.ч. title, keywords, description
    * поддержка мета-тегов Open Graf
    * поддержка атрибута canonical для детальной карточки товара
  * редакция 2.4.7 - новый механизм возможностей ценообразования. Возможность указать скидки/наценки на произвольные сегменты номенклатуры
    * изменение структуры главного меню
    * оптимизация рендеринга страниц сайта
    * оптимизации и исправления

В этом плане отмечены важные функции и нововведения, которые ожидают продукт в будущем \(многие, но, конечно, далеко не все\):

### Ожидается в минорных релизах \(ориентировочный срок - 2-й квартал 2018 г. - начало 3-го квартала 2018 г.\):

* редакция 2.4.8.х - отправка почты по произвольным шаблонам. Плановая оптимизация и рефакторинг, небольшие доработки и UX-оптимизация подсистемы доставки
* редакция 2.4.9.х - изменение логики работы с корзиной, возможность смены договора в корзине

### Ожидается в мажорных релизах \(ориентировочный срок - 3-4 квартал 2018 г.\):

* редакция 2.5 - переработки подсистемы хранения сайтов и их объектов \(более четкое разделение сущностей, формирование иерархической структуры объектов, принадлежащих сайту
  * возможность “выгружать и загружать” из системы и обратно весь сайт целиком “одной кнопкой”
  * поддержка “множества сайтов” и “множества дизайнов”
* редакция 2.6 - полностью переработанная система статусов \(включает в себя новый механизм управления строками и статусами строк заказов, а также систему статусов на уровне заказа.
* редакции 2.7 - новые пользовательские интерфейсы по управлению функционалом Зета Веб. Переход на управляемые формы.

### Далее:

* редакция 2.8 - расширение поддерживаемых конфигураций 1С.
* и многое другое

