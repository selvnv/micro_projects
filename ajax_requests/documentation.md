## AJAX запросы при помощи jQuery

| Метод | Настройки | Тип, значение по умолчанию | Описание |
| ---- | ---- | ---- | ---- |
| `$.ajax(settings)` | _url_ | string, адрес текущей страницы | Определяет адрес, на который будет отправлен запрос |
|  | _type_ | string, GET | Определяет тип выполняемого запроса (GET или POST). Можно использовать также типы PUT и DELETE, но нужно помнить, что их поддерживают не все браузеры. |
|  | _success(data, textStatus, jqXHR)_ | function array | Функция, которая будет вызвана в случае удачного завершения запроса к серверу. Ей будут переданы три параметра: данные, присланные сервером и уже прошедшие предварительную обработку (которая отлична для разных dataType). Второй параметр — строка со статусом выполнения. Третий параметр содержит объект jqXHR (в более ранних версиях библиотеки (до 1.5), вместо jqXHR используется XMLHttpRequest). Начиная с jQuery-1.5, вместо одной функции, этот параметр может принимать массив функций. |
|  | _data_ | object / string | Данные, которые будут отправлены на сервер. Если они заданы не строчным значением, то будут предварительно преобразован в строку. Избежать этого преобразования можно изменив параметр processData (его описание можно найти ниже). В случае запроса методом GET, строка с данными добавляется в конец url. Если данные задаются с помощью объекта, то он должен соответствовать формату: {fName1:value1, fName2:value2, ...}. |
| | _async_ | boolean, true | По умолчанию, все запросы без перезагрузки страницы происходят асинхронно (то есть после отправки запроса на сервер, страница не останавливает свою работу в ожидании ответа). Если вам понадобиться синхронное выполнение запроса, то установите параметр в false. Кроссдоменные запросы и запросы типа "jsonp" не могут выполняться в синхронном режиме. Имейте ввиду, что выполнение запросов в синхронном режиме может привести к блокировке страницы, пока запрос не будет полностью выполнен. |
|  | _dataType_ | string, определяется автоматически | Тип данных, в котором ожидается получить ответ от сервера. Если он не задан, jQuery попытается определить его автоматически с помощью полученного от сервера MIME. |
|  | _username_ | string | Имя пользователя для аутентификации на сервере, если это требуется. |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |