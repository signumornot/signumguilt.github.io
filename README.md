# Проекты:
+ [Форма для создания голосований на Маляре](https://github.com/signumornot/signumornot.github.io/blob/main/README.md#%D1%84%D0%BE%D1%80%D0%BC%D0%B0-%D0%B4%D0%BB%D1%8F-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D1%8F-%D0%B3%D0%BE%D0%BB%D0%BE%D1%81%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B9-%D0%BD%D0%B0-%D0%BC%D0%B0%D0%BB%D1%8F%D1%80%D0%B5)
+ [Генератор тотемов](https://github.com/signumornot/signumornot.github.io/blob/main/README.md#%D0%B3%D0%B5%D0%BD%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80-%D1%82%D0%BE%D1%82%D0%B5%D0%BC%D0%BE%D0%B2-%D1%81%D0%B5%D0%B2%D0%B5%D1%80%D0%BD%D0%BE%D0%B3%D0%BE-%D0%BA%D0%BB%D0%B0%D0%BD%D0%B0)
+ [Заготовка конструктора отчётов](https://github.com/signumornot/signumornot.github.io/blob/main/README.md#%D0%B7%D0%B0%D0%B3%D0%BE%D1%82%D0%BE%D0%B2%D0%BA%D0%B0-%D0%BA%D0%BE%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%82%D0%BE%D1%80%D0%B0-%D0%BE%D1%82%D1%87%D1%91%D1%82%D0%BE%D0%B2)
+ [JS-макросы в Google Spreadsheets](https://github.com/signumornot/signumornot.github.io/blob/main/README.md#%D0%B7%D0%B0%D0%B3%D0%BE%D1%82%D0%BE%D0%B2%D0%BA%D0%B0-%D0%BA%D0%BE%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%82%D0%BE%D1%80%D0%B0-%D0%BE%D1%82%D1%87%D1%91%D1%82%D0%BE%D0%B2)
+ [WPF-приложение](https://github.com/signumornot/signumornot.github.io/blob/main/README.md#wpf-%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5-%D1%83%D1%87%D0%B5%D0%B1%D0%BD%D0%B0%D1%8F-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0)

## Форма для создания голосований на Маляре
**UserScript для упрощения процесса создания голосований сферой Творчества**

*Ссылка на установку скрипта:* [greasyfork](https://greasyfork.org/ru/scripts/476878-%D0%BC%D0%B0%D0%BB%D1%8F%D1%80)
<br>*Путь к файлу кода в репозитории:* [signumornot.github.io/painter/painter.js](https://github.com/signumornot/signumornot.github.io/blob/main/painter/painter.js)

Установленный скрипт создаёт форму для генерации поста с голосованием на странице [catwar.su/sniff?creation](https://catwar.su/sniff?creation). После загрузки страницы под полем ввода содержимого поста появляется кнопка "Голосование". После нажатия кнопки создаётся форма для заполнения информации о голосовании. 

![](https://i.ibb.co/N131BpK/0a686b10ede9.png "Форма заполнения информации о голосовании")

### Функции скрипта:
+ **Генерация голосований**
  <br>После ввода всех необходимых данных и нажатия кнопки "Сгенерировать голосование" скрипт внесёт их в шаблоны Маляра и поместит в текстовый блок содержимого поста. Название поста также будет сгенерировано и вставлено в соответствующее поле автоматически.
+ **Генерация текста опросов голосований**
  <br>После нажатия на кнопку "Сгенерировать голосование" скрипт получит информацию о количестве добавленных новых версий, составит текст опроса голосования в соответствии с количестом версий и поместит текст опроса в буфер обмена пользователя (может некорректно работать на мобильных устройствах).
+ **Добавление новых версий**
  <br>Нажатие на кнопку "Добавить новую версию" приведёт к созданию новых полей ввода, предназначенных для размещения в них ссылок на предложенные новые версии перерисовок. В дальнейшем добавленные новые версии будут использованы в генерации голосования.
+ **Автоматический расчёт даты завершения**
  <br>Голосования Маляра длятся 7 дней с момента публикации поста. Скрипт предусматривает возможность автоматического расчёта даты завершения. Отметив чекбокс "Посчитать автоматически" рядом с выбором даты окончания, поле ручного выбора даты будет заблокировано. Вместе с генерацией голосования скрипт определит дату через неделю от сегодняшнего числа (для определения сегодняшней даты используется часовой пояс МСК) и вставит полученное в шаблон.

### Прочее:
+ Поле ввода ID автора поддерживает как ввод только цифр, так и цифр с link/cat/другими буквами. В результате скрипт выделит из введённого только цифры и поместит их в шаблон.
+ Заполнение шаблонов голосований в коде скрипта выполнено так, чтобы в случае изменений их было легко отредактировать.
+ Повторное нажатие на кнопку "Голосование" очистит форму заполнения данных о голосовании и обнулит все добавленные новые версии.
+ Если добавлена только одна новая версия, в шаблоне голосования и тексте опроса не будет указываться нумерация новых версий, поскольку это не требуется. Если новых версий будет 2 и более, шаблон и текст опроса будет содержать нумерацию новых версий.
+ Шаблон голосований за фоны структурно отличается от других типов голосований. Скрипт учитывает это и использует данные о выбранном типе объекта для заполнения нужного шаблона.

### Пример работы:
![](https://i.ibb.co/QfWTDtJ/0a686b10ede9.png "Заполненная форма данных голосования")

**Сгенерированный код голосования:**
```
[color=black]
[center][table=black]
[tr]
[td][table=#807b73]
[tr]
[td][table=0]
[tr]
[td]⠀[/td]
[td][center][b][size=14]Предмет «Карамельный череп»[/size][/b]

[table=0]
[tr]
[td][center][size=13][b]Текущая версия:[/b][/size]
[img]cw3/things/1908.png[/img][/center][/td]
[/tr]
[tr]
[td][center][size=13][b]Новая версия 1:[/b][/size]
[img]http://d.zaix.ru/BpWg.png[/img][/center][/td]
[/tr][tr]
[td][center][size=13][b]Новая версия 2:[/b][/size]
[img]http://d.zaix.ru/BpVZ.png[/img][/center][/td]
[/tr][/table][/center]
[size=13][b]Принадлежность: [/b]общедоступный[/size]
[size=9][b]Автор: [/b][i][link1457733][/i][/size]
[size=9][b]Голосование длится до: [/b]03.12.23[/size][/td]
[td]⠀[/td]
[/tr]
[/table][/td]
[/tr]
[/table][/td]
[/tr]
[/table][/center]
[/color]
```
[К содержанию](https://github.com/signumornot/signumornot.github.io/blob/main/README.md#%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D1%8B)

## Генератор тотемов Северного клана
**Страница любительского генератора тотемов Северного клана**

*Ссылка на страницу генератора:* [github.io](https://signumornot.github.io/totems/mytotem)
<br>*Путь к папке с файлами генератора в репозитории:* [signumornot.github.io/totems/](https://github.com/signumornot/signumornot.github.io/tree/main/totems)

Генерирует изображение тотема Северного клана, как в профилях игроков на сайте. Генерация включает в себя 27 существующих видов тотемов и более 50 возможных качеств, распределённых по группам по значению. Все данные, использующиеся в генерации, хранятся в json-файле. Каждому тотему присваиваются подходящие ему группы качеств.

### Как работает генератор:
+ Скрипт генерации запускается при нажатии на кнопку "Сгенерировать тотем". Вначале выбирается случайный массив данных, содержащий в себе информацию об одном из 27 тотемов: название зверя, картинку тотема, подходящие группы качеств ~~и шанс~~.
+ На странице размещён чекбокс, позволяющий выбрать параметр генерации: "умная" генерация или полностью рандомная. После генерации выбранный параметр будет указан под сгенерированным тотемом.
+ Если выбрана умная генерация, качество выбранного скриптом тотема будет сгенерировано в соответствии с присвоенными ему группами качеств: скрипт получает информацию о содержащихся в группах качествах, затем выбирает один из них.
+ Если выбрана рандомная генерация (чекбокс не отмечен), скрипт выберет случайную группу качеств, а затем одно случайное качество из выбранной группы.
+ Сгенерированные данные размещаются в соответствующих элементах на странице, формирующих картинку тотемов, как это выполнено в профилях игроков на сайте.

### Пример генерации тотема с выводом параметров в консоли для проверки
  ![](https://i.ibb.co/xLy0yQ4/0a686b10ede9.png "Пример генерации")

### Нереализованные (запланированные) функции:
+ **Использование "реальных" шансов в генерации тотема**
  <br>Соответствующий чекбокс размещён на странице генератора в заблокированном виде.
  <br>Предполагается, что при отмеченном чекбоксе в генерации будет использоваться не чистый рандом, как сейчас, а рандом с определёнными шансами, выбранными из данных статистики тотемов. При этом шанс присваивается каждому тотему в json-файле. Так, например, шанс сгенерировать тотем Лисы равняется 1,86%, а шанс сгенерировать тотем Кугуара - 6,51%. С более высокой вероятностью после генерации пользователь получит Кугуара, а не Лису.
  <br>Параметр использования реальных шансов сможет комбинироваться с умной генерацией и будет указываться в выбранных параметрах, если используется в генерации. 

[К содержанию](https://github.com/signumornot/signumornot.github.io/blob/main/README.md#%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D1%8B)

## Заготовка конструктора отчётов
**Заготовка визуальной части конструктора отчётов, задуманного как скрипт на вар**

*Ссылка на страницу конструктора:* [github.io](https://signumornot.github.io/reports/constructor)
<br>*Путь к папке с файлами конструктора в репозитории:* [signumornot.github.io/reports/](https://github.com/signumornot/signumornot.github.io/tree/main/reports)

Конструктор отчётов запланирован как мой скрипт для использования на варе, я начал заниматься им примерно 24 ноября и планирую иногда садиться за дальнейшую разработку по настроению, свободному времени и желанию.

### Что есть на странице сейчас:
+ Базовые элементы создания формы заполнения данных для отчёта.
  <br>Кнопка "Создать новый отчёт" должна будет создавать элементы для указания имени отчёта и ID блога, в котором он используется. После заполнения полей имени отчёта и ID блога и нажатия кнопки "ОК" эти элементы будут очищаться, взамен им будут создаваться те, что ниже:
  <br>Данные о разрабатываемом отчёте: имя отчёта и блог, в котором он используется.
  <br>Таблица с двумя столбцами, где первый столбец содержит предпросмотр непосредственно формы (поля ввода, кнопки и т.д.), а второй - предпросмотр BB-кода отчёта, того, что будет генерироваться после заполнения созданной формы.
  <br>Кнопка "Добавить поле", создающая элементы для выбора типа нового поля: выпадающий список и кнопку "ОК", подтверждающую создание нового поля.
  <br>Элементы выпадающего списка с выбором нового поля делятся на две группы: специализированные поля (те, что будут заготовлены заранее) и свободные поля (поля с полностью настраиваемыми пользователем параметрами).
+ Выбор какого-либо элемента выводит описание выбранного поля и элементы для его предварительной настройки.
  <br>Пример вывода описания поля работает при выборе любой опции, пример вывода элементов для предварительной настройки - при выборе опции "ID ведущего/собирающего".

![](https://i.ibb.co/qMpwFVq/0a686b10ede9.png "Заготовка конструктора отчётов")

**Текущий код конструктора - примитивная заготовка визуальной части скрипта**

### Что должен будет содержать скрипт по идее:
+ Внедрение на сайт, скорее всего, на страницу настроек. Соответственно, все элементы управления будут создаваться соответствующими JS-функциями, указанными в комментариях кода сейчас.
+ Работающий функционал создания и предпросмотра новых полей и скрипта генерации отчёта.
+ Сохранение генератора отчётов в LocalStorage, возможность удалять, импортировать и экспортировать отчёты.

[К содержанию](https://github.com/signumornot/signumornot.github.io/blob/main/README.md#%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D1%8B)

## Макросы с функциями для управления данными в гугл-таблице
**Макросы, написанные на JavaScript для упрощенного автоматизированного управления данными в статистической гугл-таблице**

**Для просмотра и тестирования макросов была создана копия гугл-таблицы с правами редактора.**
<br>*Ссылка на гугл-таблицу для просмотра и тестирования*: [docs.google.com](https://docs.google.com/spreadsheets/d/1afteArCyDboe2ANnAG6D8n4G_9btA5cyNfIPzrozfXI/edit?usp=sharing) (лист "Панель управления")
<br>*Ссылка на документацию для пользователей гугл-таблицы*: [docs.google.com](https://docs.google.com/document/d/1bkLh2x9PhKCRXo8iIhq998AT3FNW4YUmffqjdwfk5Bc/edit?usp=sharing)
<br>*Путь к файлу с кодом макросов в репозитории*: [signumornot.github.io/google spreadsheet/scripts.js](https://github.com/signumornot/signumornot.github.io/blob/main/google%20spreadsheet/scripts.js)

### Функции макросов:
+ Добавление новых данных из специально отведённых для ввода ячеек "Панели управления" в соответствующие формам листы данных "для динамики", "данные" и/или "архив". Предварительное создание на этих листах новых строк, в которые будут помещаться новые данные.
+ Поиск строки по введённым критериям (по указанному имени игрока) и удаление найденной строки в листе данных "данные". Поскольку в возможностях макросов не было найдено функции удаления строк как таковой, реализация выполнена в виде сохранения других (не подходящих под критерий) строк в переменной newData, очистке задействованного диапазона листа и последующем размещении в нём данных из переменной newData.
+ Сортировка ячеек определённого диапазона на листах "Текущая статистика" и "Общая статистика" по заранее заданным критериям. 

[К содержанию](https://github.com/signumornot/signumornot.github.io/blob/main/README.md#%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D1%8B)

## WPF-приложение (учебная работа)
**Приложение Windows Presentation Foundation, выполненное в рамках академического задания**

*Путь к папке с файлами проекта*: [signumornot.github.io/wpf/](https://github.com/signumornot/signumornot.github.io/tree/main/wpf)

Приложение, выполненное в Microsoft Visual Studio, содержащее окна Регистрации, Авторизации, Панели управления и просмотра содержимого таблицы базы данных, написанное с использованием XAML-разметки и C#. Для выполнения задания также создавалась база данных в MySQL Workbench.
### Содержимое окон: 
+ **MainWindow**
  <br>Окно регистрации. Содержит поля ввода данных для регистрации новой учётной записи. Если все поля заполнены верно, они заносятся в базу данных; иначе, если не заполнено какое-то поле или заполнено неверно, указывается ошибка в специальном поле.
+ **Login**
  <br>Окно авторизации. Содержит поля ввода данных для авторизации существующего пользователя. Если пользователь с введёнными данными существует в базе данных, осуществляется вход и перевод на окно панели управления; иначе выводится ошибка в специальном поле.
+ **Welcome**
  <br>Окно панели управления с выбором таблицы базы данных для просмотра. Код выполнен только для кнопки "Пользователи", поскольку по техническому заданию этого было достаточно.
+ **Users**
  <br>Окно просмотра содержимого соответствующей таблицы базы данных. В окне выводится таблица с данными о всех зарегистрированных учётных записях (за исключением столбца "пароль").

### Примеры работы программы:
**Окно регистрации, новая учётная запись создана**
<br>![](https://i.ibb.co/QJpL6BZ/0a686b10ede9.png "Окно регистрации")

**Окно авторизации, учётной записи с указанными данными нет в базе данных**
<br>![](https://i.ibb.co/zGVRQM9/0a686b10ede9.png "Окно авторизации")

**Окно просмотра содержимого таблицы "Пользователи"**
<br>![](https://i.ibb.co/tCdQBkB/0a686b10ede9.png "Пользователи")

[К содержанию](https://github.com/signumornot/signumornot.github.io/blob/main/README.md#%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D1%8B)
