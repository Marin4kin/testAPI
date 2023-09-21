# API Githab Issues

<p> Коллекция Postman  (скачать и импортировать в Postman)</p> 
> <a href="https://drive.google.com/file/d/177fpF3q3_xd1H8DrxUmZIxqZlVy8Fz7d/view?usp=sharing">Ссылка на коллекцию</a>
  <br> 
<p> Для запуска этой коллекции необходимо сгенерировать на сайте githab свой Personal access tokens (classic) , скопировать и вставить токен в поле авторизации на уровне колекции, выбрав тип авторизации Bearer-Token, сохранить. </p> 
<p> Коллекция позволяет протестировать API Githab issues с методами GET, POST, PUT, PATCH, DELETE.</p> 

![image_2023-09-21_23-13-30](https://github.com/Marin4kin/testAPI/assets/132477713/ab2d44da-300c-498c-bd74-56844e60b87c)

1. Запрос на получение всех имеющихся задач (issues)<br> 
2. Запрос на получение всех задач владельца (Owner)<br> 
3. Запрос на создание Issue 1 (описание "Something went wrong", label "bug", assignee "текущий логин на GitHub")<br> 
4. Запрос на получение конкретного issue <br> 
5. Запрос на изменение названия задачи (Issue 1 на Issue 2) <br> 
6. Запрос на блокировку задачи <br> 
7. Запрос на разблокировку задачи <br> 
8. Запрос на Удаление Issue 2 - в документации https://docs.github.com/en/rest/issues/issues?apiVersion=2022-11-28#about-issues нет описания способа удаления задачи. При удалении через GUI в Chrome DevTools копируем параметры запроса, - происходит удаление с использованием метода POST, в теле прописываются параметры задачи ( verify_delete: 1, _method: delete , authenticity_token: bFzuBd4C2b_tLcuPDx3OZ_AKJ8cddU8iW0esrILzduV0VCB8m7DZ2RLWBBWdxcnq-xdvmiNB0s8rRr7aaAUlTg ) Но через Postman - нужен другой токен, тк по этому удаление уже произошло через интерфейс. Ответ приходит: 404Not Found. <br> 
9. Запрос на неверный url (соотвественно можно аналогично создать множество негативных кейсов, меняя параметры в запросах). <br> 
