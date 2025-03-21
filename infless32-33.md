# par 32
1. Почему пользователей не устраивает «чистый» HTML?
«Чистый» HTML (HyperText Markup Language) — это статический язык разметки, который используется для описания структуры веб-страниц. Проблема заключается в том, что он ограничен в возможностях интерактивности: страницы, созданные исключительно на HTML, выглядят плоскими и неподвижными. Пользователи ожидают более насыщенного взаимодействия с контентом, анимации, возможности изменять элементы страницы в режиме реального времени. Для решения этой проблемы применяются дополнительные технологии, такие как CSS и JavaScript.
2. Что такое динамический HTML? Какие технологии он использует?
Динамический HTML (DHTML) — это комбинация HTML, CSS и JavaScript, позволяющая создавать интерактивные и динамичные веб-страницы. Основные технологии включают:
HTML — определяет структуру документа.
CSS — управляет внешним видом элементов страницы (цвета, шрифты, позиционирование).
JavaScript — добавляет интерактивность, позволяя манипулировать элементами страницы в реальном времени.
В отличие от простого HTML, DHTML позволяет изменять содержимое и стиль страницы после её загрузки браузером, обеспечивая гибкость и возможность реагировать на действия пользователя.

3. Чем отличается DHTML от HTML?
Основное различие между DHTML и HTML заключается в добавлении интерактивности. 
HTML является статическим языком разметки, тогда как DHTML включает динамические изменения содержимого и стиля страницы благодаря использованию JavaScript и CSS. 
Это делает DHTML более мощным инструментом для создания интерактивных веб-приложений.
4. Что представляет собой JavaScript-код? 
JavaScript — это скриптовый язык программирования, который выполняется непосредственно в браузере пользователя. 
Код JavaScript добавляется в HTML-документ и используется для управления поведением веб-страницы.
С помощью JavaScript можно изменять содержание страницы, обрабатывать события (например, нажатия кнопок), взаимодействовать с сервером через AJAX-запросы и многое другое.
5. Что такое DOM?
6. Зачем нужна такая структура? 
DOM (Document Object Model) — это объектная модель документа, представляющая веб-страницу в виде дерева объектов. 
Каждый элемент HTML-документа (заголовки, параграфы, изображения и т.д.) представлен в DOM как узел. Эта структура позволяет программам (в основном JavaScript) манипулировать содержимым веб-страницы, добавлять, удалять или изменять элементы, а также реагировать на события, происходящие на странице. DOM обеспечивает доступ ко всем частям страницы и делает возможным создание динамических изменений.
Как можно найти нужный элемент на веб-странице из JavaScript-кода? В JavaScript существует несколько методов для поиска нужных элементов на веб-странице:
document.getElementById('id') — находит элемент по уникальному идентификатору (id).
document.querySelector('.className') — выбирает первый элемент, соответствующий указанному селектору CSS (класс, ID, тег и т.д.).
document.querySelectorAll('.className') — возвращает список всех элементов, соответствующих селектору.
document.getElementsByTagName('tagName') — находит все элементы с заданным именем тега.
document.getElementsByClassName('className') — находит все элементы с указанным классом.
7. Что такое «ролл-овер»?
Приведите примеры, когда этот эффект действительно полезен. Ролл-овер (или hover-эффект) — это изменение внешнего вида элемента веб-страницы при наведении указателя мыши.
Например, кнопка может менять цвет или размер, изображение может становиться ярче, или появляется всплывающее окно с дополнительной информацией. Этот эффект полезен в следующих случаях:
Улучшение навигации: Изменение цвета или формы кнопки помогает пользователям лучше ориентироваться на сайте.
Информирование: Появление подсказок или дополнительной информации при наведении на элемент улучшает восприятие контента.
Привлечение внимания: Эффект ролл-овера привлекает внимание к важным элементам интерфейса.
Анимационные эффекты: Использование ролл-овера для создания анимаций делает интерфейс более привлекательным и современным.
1. Как вы понимаете слово «событие»? С какими событиями мы работали в приведённых примерах?
Слово «событие» в контексте веб-разработки относится к действиям, выполняемым пользователем или системой, которые могут вызывать реакцию на веб-странице. Примеры событий включают клики мышью, перемещение курсора, ввод текста, загрузка страницы и другие взаимодействия. В ваших примерах, вероятно, использовались события вроде click, mouseover, load.

2. Что такое обработчик события?
Обработчик события — это функция или код, который выполняется в ответ на возникновение определенного события. Например, если событие — это клик мыши, то обработчик может быть функцией, меняющей цвет фона или открывающей новое окно.

3. Что означает запись this.src?
Запись this.src в JavaScript обычно применяется внутри обработчика события и обозначает источник текущего объекта. Например, если объект — это изображение, то src будет указывать путь к изображению. Таким образом, запись this.src = 'new_image.jpg' заменит текущее изображение новым.

4. Расскажите о правилах использования кавычек в JavaScript-коде.
В JavaScript можно использовать одинарные ('') и двойные ("") кавычки взаимозаменяемо. Главное правило — соблюдать согласованность: если строковая константа начинается с одного типа кавычек, она должна заканчиваться таким же типом. К примеру:


let str1 = "Hello";
let str2 = 'World';
Однако есть небольшие нюансы:

Если внутри строки уже используются одни кавычки, лучше использовать другой тип снаружи, чтобы избежать экранирования:

let message = "He's a good guy"; // Двойные кавычки
let anotherMessage = 'She said, "Hello!"'; // Одинарные кавычки
5. Подумайте, зачем могут понадобиться скрытые блоки на веб-странице.
Скрытые блоки часто используются для реализации различных эффектов, таких как всплывающие окна, аккордеоны, меню, а также для постепенной подгрузки контента по мере прокрутки страницы. Они позволяют экономить пространство на экране и показывать контент только тогда, когда это необходимо.

6. Объясните, зачем скрытому блоку в рассмотренном примере присвоен и класс, и идентификатор.
Идентификаторы (id) обеспечивают уникальную идентификацию конкретного элемента на странице, что полезно для прямого обращения к нему через JavaScript. Классы (class), напротив, могут применяться сразу к нескольким элементам, объединяя их по стилю или поведению. Присвоение обоих атрибутов позволяет сочетать уникальные манипуляции с элементом через его id и стилизацию через общий class.

7. Какое свойство блока нужно изменить, чтобы скрыть или показать его?
Для скрытия или отображения блока можно изменить свойство display. Чтобы скрыть элемент, присваиваем значение none:


elem.style.display = "none";
Чтобы снова показать элемент, используем значения block, inline-block или другое подходящее в зависимости от контекста:


elem.style.display = "block";
8. Как вы думаете, зачем JavaScript-код выносят в отдельные файлы?
Вынесение JavaScript-кода в отдельные файлы способствует лучшей организации проекта, облегчает чтение и поддержку кода, а также позволяет повторно использовать скрипты на разных страницах сайта. Это также улучшает производительность, так как браузер кэширует внешние скрипты, ускоряя загрузку страниц.

9. Как подключаются к веб-странице файлы, содержащие JavaScript-код?
Файлы с JavaScript подключаются с помощью тега <script>, расположенного либо в разделе <head> или перед закрывающим тегом </body>. Пример подключения:


<script src="path/to/your/script.js"></script>
10. Как получить ссылку на элемент, идентификатор которого мы знаем?
Чтобы получить ссылку на элемент по его идентификатору, можно использовать метод getElementById():


let element = document.getElementById("elementId");
11. Зачем в функцию show из рассмотренного примера добавлен условный оператор?
Условный оператор в функции show используется для проверки состояния элемента перед выполнением действий. Например, если элемент уже виден, то функция может не скрывать его снова или наоборот. Условие помогает избежать ненужных манипуляций и поддерживает корректное поведение интерфейса.

12. Как понимать запись elem.style.display?
Запись elem.style.display в JavaScript обращается к свойству display элемента elem. Оно контролирует способ отображения элемента на странице. Значения могут включать block, inline, none и другие, определяющие, как именно элемент будет рендериться в документе.

13. Зачем в обработчик гиперссылки в рассмотренном примере добавлена команда return false?
Команда return false в обработчике события предотвращает стандартное действие браузера по умолчанию, связанное с событием. В случае гиперссылки это отменяет переход по ссылке, позволяя вместо этого выполнить определенный сценарий JavaScript.

14. Что такое форма? Для чего она предназначена?
Форма — это структурированный набор полей ввода на веб-странице, предназначенный для сбора данных от пользователя. Формы позволяют отправлять введенные данные на сервер для обработки. Примеры использования форм включают регистрацию, вход в систему, отправку сообщений и т.п.

15. Как можно использовать формы без «принимающей» серверной программы?
Формы можно использовать локально на клиентской стороне, например, для выполнения простых вычислений или валидации данных без отправки на сервер. Это особенно полезно для предоставления мгновенных результатов или проверки правильности заполнения полей до передачи данных.

16. Зачем нужен атрибут name для формы и её элементов?
Атрибут name необходим для идентификации формы и её элементов при передаче данных на сервер. Серверная программа получает данные в формате пар ключ-значение, где ключи — это имена полей формы. Без атрибута name данные не будут правильно переданы.

17. Как браузер отличает кнопку от поля ввода (оба элемента задаются тэгом <input>)?
Браузер отличает кнопку от поля ввода по значению атрибута type. Например:


<input type="text"> <!-- Поле ввода -->
<input type="button"> <!-- Кнопка -->
Различные значения type определяют, каким образом элемент будет отображаться и функционировать.

18. Как задать текст на кнопке?
Текст на кнопке задаётся с помощью атрибута value:


<input type="button" value="Нажми меня">
19. Какая функция используется для вывода сообщения пользователю в отдельном окне?
Функция alert(message) выводит сообщение в диалоговом окне. Она останавливает выполнение сценария до тех пор, пока пользователь не закроет окно.
20. Зачем в обработчик гиперссылки в рассмотренном примере добавлена команда return false?
Команда return false в обработчике события гиперссылки предотвращает стандартное поведение браузера — переход по ссылке. Вместо этого выполнение передается написанному вами сценарию JavaScript. Это полезно, когда ссылка служит триггером для какого-то действия на странице, а не для перехода на новый адрес.

21. Что такое форма? Для чего она предназначена?
Форма — это структурированный набор полей ввода на веб-странице, предназначенный для сбора данных от пользователя. Эти данные затем отправляются на сервер для дальнейшей обработки. Примеры использования форм включают регистрацию, авторизацию, отправку контактных данных и т.д.

22. Как можно использовать формы без «принимающей» серверной программы?
Формы можно использовать локально на клиентской стороне для выполнения таких задач, как проверка валидности данных (например, проверка формата электронной почты или номера телефона) или даже проведение простых расчетов без отправки данных на сервер. Локальная обработка данных полезна для немедленного отклика без задержки на пересылку запросов.

23. Зачем нужен атрибут name для формы и её элементов?
Атрибут name необходим для идентификации каждого элемента формы при передаче данных на сервер. Когда форма отправляется, браузер собирает пары «ключ-значение», где ключом выступает имя элемента, указанное в атрибуте name. Серверная программа получает эти данные именно по этому имени, и без него невозможно корректно обработать отправленные сведения.

24. Как браузер отличает кнопку от поля ввода (оба элемента задаются тэгом <input>)?
Браузер различает типы элементов формы, задаваемых тегом <input>, по значению атрибута type. Например:

<input type="text"> — поле для ввода текста.
<input type="password"> — поле для ввода пароля.
<input type="submit"> — кнопка для отправки формы. Таким образом, разные значения атрибута type указывают браузеру, какой тип элемента нужно создать.
25. Как задать текст на кнопке?
Текст на кнопке задается с помощью атрибута value:


<input type="button" value="Отправить">
Здесь текст «Отправить» будет отображён на кнопке.

26. Какая функция используется для вывода сообщения пользователю в отдельном окне?
Для вывода сообщения пользователю в новом окне используется функция alert(). Она открывает диалоговое окно с сообщением и ожидает реакции пользователя (обычно нажатия кнопки OK):


alert("Ваше сообщение здесь!");

# par 33
1. Что такое хостинг?
Хостинг — это услуга, предоставляемая специализированными компаниями (хостерами), которая заключается в размещении файлов вашего сайта на сервере, постоянно подключенном к Интернету. Это позволяет другим пользователям получать доступ к вашему сайту круглосуточно.

2. Почему не имеет смысла размещать сайт на своём домашнем компьютере?
Размещение сайта на домашнем компьютере связано с рядом проблем:

Непостоянство соединения. Домашний компьютер может отключаться, а значит, ваш сайт будет недоступен.
Ограниченная пропускная способность. Домашние интернет-соединения имеют ограниченную скорость и пропускную способность, что затрудняет стабильную работу сайта.
Безопасность. Ваш домашний компьютер менее защищен от атак, чем профессиональные серверы, которые используют мощные системы безопасности.
Технические сложности. Поддержание работы сервера требует знаний и постоянного мониторинга, что сложно реализовать дома.
3. За счёт чего зарабатывают бесплатные хостинги?
Бесплатные хостинги зарабатывают различными способами:

Реклама. Часто на сайтах, размещенных на бесплатных хостингах, показывается реклама, прибыль от которой идет провайдеру услуг.
Продажа платных услуг. Бесплатные пользователи могут впоследствии перейти на платные тарифы с дополнительными функциями.
Партнерские программы. Хостер может зарабатывать комиссионные за привлечение клиентов к другим сервисам.
4. Что такое тарифный план?
Тарифный план — это пакет услуг, предлагаемых хостингом, который включает различные параметры: объем дискового пространства, лимит трафика, количество баз данных, почтовых ящиков и другие ресурсы. Тарифы различаются по стоимости и функционалу, что позволяет выбрать оптимальный вариант в зависимости от потребностей.

5. Почему вводится ограничение на трафик сайтов?
Ограничение на трафик (объем передаваемой информации) вводится для контроля нагрузки на серверы и сети. Если бы каждый сайт мог потреблять неограниченный трафик, это могло бы привести к перегрузкам и снижению производительности для всех пользователей. Ограничения помогают сбалансировать нагрузку и поддерживать стабильность работы.

6. Как зарегистрировать доменное имя второго уровня?
Доменное имя второго уровня регистрируется через аккредитованных регистраторов доменов. Процесс регистрации включает следующие шаги:

Проверка доступности желаемого домена.
Выбор регистратора.
Заполнение анкеты с персональными данными.
Оплата услуги регистрации. После успешного завершения процесса доменное имя закрепляется за вами на определённый срок (обычно 1–2 года).
7. Как связать доменное имя с сервером, на котором хранятся файлы?
Для связи доменного имени с сервером необходимо настроить DNS-записи. Обычно это делается через панель управления доменом у регистратора. Вам потребуется указать IP-адрес или NS-серверы вашего хостинга, чтобы запросы к вашему домену перенаправлялись на соответствующие серверы.

8. Какими способами можно загружать файлы на сервер?
Существует несколько способов загрузки файлов на сервер:

FTP/SFTP. Протоколы File Transfer Protocol (FTP) и Secure FTP (SFTP) позволяют передавать файлы между вашим компьютером и сервером.
Панель управления хостингом. Многие хостинги предоставляют собственные панели управления, через которые можно загружать файлы прямо в браузере.
SSH. Используя SSH (Secure Shell), можно загружать файлы через командную строку.
Git. Некоторые хостинги поддерживают интеграцию с системами контроля версий, такими как Git, что позволяет легко обновлять файлы на сервере.
