# module19_homework

Этот проект представляет собой учебную практику по AJAX.
## Технологии
- [JS](https://www.javascript.com/)
## Цели
* Задание 1. 
    * Написать код, который будет преобразовывать XML в JS-объект и выводить его в консоль.
* Задание 2. 
    * Дан образец JSON-строки:
        ```
        {"name":"Anton","age":36,"skills":["Javascript","HTML","CSS"],"salary":80000}
        ```
        Задача — создать JS-объект, который при преобразовании в JSON будет возвращать в качестве результата такую же JSON-строку, как в образце. Получившуюся строку вывести в консоль.

* Задание 3. 
    * Написать скрипт, который при открытии страницы будет делать следующее:
        Если пользователь зашел в первый раз, вывести окно prompt с сообщением: «Добро пожаловать! Назовите, пожалуйста, ваше имя».

        После того, как пользователь введет имя, записать имя, дату и время визита в localStorage.

        Если пользователь открывает страницу не впервые, вывести в alert сообщение вида: «Добрый день, *имя пользователя*! Давно не виделись. В последний раз вы были у нас *дата последнего посещения*» и перезаписать дату последнего посещения.
* Задание 4.
    * Создать Promise, в котором c задержкой в три секунды сгенерировать случайное целое число от 1 до 100. Если сгенерированное число четное — Promise выполнится успешно, если нечетное — выполнится с ошибкой. После разрешения Promise обработать результат его выполнения и вывести сообщение в консоль:
        * «Завершено успешно. Сгенерированное число — number», если Promise завершился успешно. Вместо number подставить сгенерированное число
        * «Завершено с ошибкой. Сгенерированное число — number», если Promise завершился с ошибкой. Вместо number подставить сгенерированное число
* Задание 5. 
    * Написать код приложения, интерфейс которого состоит из поля ввода и кнопки «Получить список   задач». При нажатии на кнопку нужно отправить запрос с помощью fetch на URL https://jsonplaceholder.typicode.com/users/3/todos. Число 3 представляет собой id пользователя, вместо него нужно подставить число, введенное в поле. Если пользователь с таким id существует, вернется список задач для этого пользователя, каждая задача представлена объектом вида:
        ```
        {
            "userId": 3,
            "id": 43,
            "title": "tempore ut sint quis recusandae",
            "completed": true
        }
        ```
        Где title — описание задачи, а completed — флаг, отображающий, выполнена задача или нет. Вывести данный список на страницу, оформив соответствующим образом: в виде списка (ul или ol), выполненные задачи должны быть написаны зачеркнутым текстом. Если пользователь с введенным id не существует, вывести сообщение: «Пользователь с указанным id не найден».
* Задание 6. 
    * Написать код приложения, интерфейс которого состоит из двух input и кнопки. В input можно ввести любое число.

        При клике на кнопку происходит следующее:
        * Если число в первом input не попадает в диапазон от 1 до 10 или не является числом — выводится ниже текст «Номер страницы вне диапазона от 1 до 10».
        * Если число во втором input не попадает в диапазон от 1 до 10 или не является числом — выводится ниже текст «Лимит вне диапазона от 1 до 10».
        * Если и первый, и второй input не в диапазонах или не являются числами — выводится ниже текст «Номер страницы и лимит вне диапазона от 1 до 10».
        * Если числа попадают в диапазон от 1 до 10 — сделать запрос по URL https://picsum.photos/v2/list?page=1&limit=10, где GET-параметр page — это число из первого input, а GET-параметр limit — это введённое число второго input. 

        Пример: если пользователь ввёл 5 и 7, то запрос будет вида https://picsum.photos/v2/list?page=5&limit=7.
        После получения данных вывести список картинок на экран.

        Если пользователь перезагрузил страницу, то ему должны показываться картинки из последнего успешно выполненного запроса (использовать localStorage).