Hospitals crud.

Информация должна отображаться в виде таблицы, со следующими полями:
* Наименование учреждения (поле full_name)
* Адрес (поле address)
* Телефон (поле phone)

Функционал: 
* При нажатии на кнопку добавления открывается модальное окно с полями ввода, кнопками "Добавить" и "Отмена"
* При заполненных полях ввода и нажатии кнопки "Добавить", добавляется элемент мед. учреждения в таблицу и происходит запись в LocalStorage
* Кнопки "Редактирование" и "Удаление" элемента таблицы появляются при наведении на него
* При нажатии на кнопку "Редактирование" открывается модальное окно, с заполненными полями ввода, кнопками "Изменить" и "Отмена"
* При нажати на кнопку "Изменить" и заполненных полях ввода выбранный элемент из таблицы и LocalStorage изменяется
* При незаполненных полях ввода в модальном окне и нажатия на кнопки "Изменить" или "Добавить", действие не происходит
* При нажатии на кнопку "Отмена", модальное окно закрывается
* При нажатии на кнопку "Удалить", элемент удаляется из таблицы и LocalStorage

Tech stack:
  - Gulp, Babel
  - Vanilla JavaScript(ES6+)
  - SASS 
  - Семантическая, валидная верстка
  - Поддержка Internet Explorer 11 и последних версий Firefox и Chrome

Install:
* git clone https://github.com/PeachTat/hospitals-crud.git
* cd ./hospitals-crud
* yarn | npm i
* yarn start | npm run start


Test case №2.
    SELECT TOP (1000) t1.[ID],t1.[FULL_NAME],t1.[SPEC],(select SUM(t2.[SUMM]) 
    FROM [BarsGroupTest].[dbo].[TRANSACTIONS] as t2 
    WHERE t2.[DOC_ID] = t1.[ID] and YEAR(t2.[DATE]) = 2019)
    FROM [BarsGroupTest].[dbo].[Doctors] as t1
    WHERE (select SUM(t2.[SUMM]) 
    FROM [BarsGroupTest].[dbo].[TRANSACTIONS] as t2 
    WHERE t2.[DOC_ID] = t1.[ID] and YEAR(t2.[DATE]) = 2019) > 2500
