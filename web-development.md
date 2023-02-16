#### 1. Архитектура Client-Server.
Клиентом может выступать frontend, который формирует запрос, а сервер, backend, обрабатывает запрос: обрабатывает полученные данные, взаимодействует с базой данной или другими серверами, отдает нужные данные клиенту и т.п. 

#### 2. Что такое REST
Representational State Transfer(REST) — или архитектруный стиль, описывающий взаимодействие клиента с сервером. 

#### 3. Принципы REST
* __Client-Server__ — клиент-серверная архитектура
* __Stateless__ — не хранит состояние (информация о запросах и ответах нигде не хранится)
* __Cacheable__ — должно быть явное указание, можно ли клиенту кэшировать ответ на запрос
* __Uniform interface (единый интерфейс)__ — все данные должны запрашиваться через один URL и стандартными протоколами (например HTTP) 
* __Layred system (многоуровневая система)__ — приложение можно разделить на слои, но должно выполняться условие, что каждый слой может видеть только соседний слой
* __Code on demand (предоставление кода по запросу) [необязательное ограничение]__ — означает, что код может выполняться на стороне клиента


#### 4. Stateless
Не хранит состояние. Это значит, что запросы не зависят друг от друга.

#### 5. Stateful
Хранит состояние в сессиях (сессия позволяет сохранять информацию на время сеанса).

#### 6. Чем отличаются `POST`, `PUT`, `PATCH`?
* `POST` — добавляет новую запись
* `PUT` — обновляет уже существующую запись
* `PATCH` — для частичного изменения ресурса

#### 7. Идемпотентные и не идемпотентые http методы 
Идемпотетный метод - это тот метод, который при вызове одного и того же запроса несколько раз вернет один и тот же результат.  
`GET`, `PUT`, `DELETE` идемпотентны.
`POST`, `PATCH` - не идемпотентны.

#### 8. Http методы

#### . When validating a JWT, what are some of the claims that you must confirm? (Select all that apply.)
A. The exp (expiration) has not passed.
B. The algorithm is sufficient.
C. The signature matches the payload.
D. The token was Base64 encoded.
E. The iss (issuer) is the auth server you expect.
F. There is a refresh token.
G. The cid (client ID) is the client you expect.
H. The token was encrypted.

Answer:

#### . When you get a 429 response code, what should you do next
