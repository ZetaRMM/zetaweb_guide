# Контролы

**Контрол** – функциональный элемент для сайта с динамическим содержимым, решающий определенные задачи. Он может как реализовывать какие-либо действия, так и просто выводить информацию.

Перечень контролов, во многом определяющий возможности системы "Зета Веб", может видоизменяться в рамках версий продукта. Наборы контролов поставляются в рамках начальных данных, идущих с каждым релизом продукта, и загружаются в 1С с помощью обработки загрузки внутренних данных.

**Пример того, как выглядит контрол в 1С:**

![image](https://user-images.githubusercontent.com/39726989/41101453-dc3cee6e-6a6c-11e8-8ee8-4fc45f4018fb.png)

## Общая информация

Имя контрола – это то, с каким исполняемым файлом .asp связан контрол, где хранится его логика.

### Опции контрола

* Повторяющие данные – умеет ли контрол выводить список. Рисуется шапка, потом Х раз повторяющиеся данные, потом подвал.
* Многоколоночность – опция для контрола с повторяющимися данными. Если установлена опция «Многоколоночность» – то при размещении на странице он будет рисовать повторяющиеся данные в несколько колонок. Рисуется шапка, потом открывается левая колонка, потом Х раз повторяются данные по количеству колонок, потом правая колонка, потом снова левая и т.д. При неделимом нацело количестве элементов дополняет пустыми значениями.

{% hint style="info" %}
В будущем эта опция перейдет на уровень свойств шаблона, вместе с числом колонок, количеством элементов на странице и расположением данных вертикально.
{% endhint %}

### Параметры контрола

Содержат как собственные параметры контрола, задающиеся именно для него \(объединены в группу собственные\), так и те или иные типовые параметры.

### Части шаблонов контрола

Часть шаблона – это поле или элемент управления \(булево, строка, поле ввода и т.д.\). Все части шаблонов объединены в группы:

![image](https://user-images.githubusercontent.com/39726989/41103160-2111daaa-6a71-11e8-9f9d-2813ee82d9c8.png)

Группы формируются по какому-либо логическому признаку, как правило, для удобства верстки. Кроме того, к каждой группе частей шаблонов могут быть привязаны группы типовых частей шаблонов - части шаблонов, общие для нескольких контролов.

### Шаблоны контрола

Это вариант того, как отображается конкретный контрол. При выводе в контрола на страницу обязательно выбрать тот или иной шаблон его отображения. Шаблон может содержать в себе произвольное количество частей шаблона - столько, сколько нужно пользователю для решения его задач с помощью данного контрола.

В рамках типового дизайна есть набор заранее созданных шаблонов, но пользователь может добавлять собственные шаблоны на основе любого контрола самостоятельно.

### Роли

На закладке определяется, какой роли доступен тот или иной контрол.

**Резюмируя** - контрол, его опции и параметры, а также части шаблонов - это то, что создается в процессе разработки системы и формирует функционал. Данные поставляются вместе с обновлениями, стоят на поддержке и в общем случае не меняются пользователями.

При использовании контрола в рамках верстки пользователь указывает шаблон - то, как отображается конкретный контрол и какая его функциональность используется. Количество шаблонов, а также их состав \(из того, что умеет контрол\) - неограниченно, и сами шаблоны создаются пользователями.

