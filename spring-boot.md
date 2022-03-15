#### 1. Что нам дает Spring Boot?
* Встроенный сервер-приложение - контейнера сервлетов (Tomcat)
* Авто-кнфигурация
* Страртеры

#### 2. Какие аннотации включены в `@SpringBootApplication`?
* `@Configuration`
* `@EnableAutoConfiguration`
* `@ComponentScan`

#### 3. Что такое стартеры?
Эта такая зависимоть, которая содержит в себе другие зависимости. В итоге вместо того чтобы добавить несколько зависимостей, мы добавляем одну, которая содержит в себе 
список нужных нам зависимостей.
Также благодаря стартерам у нас настраивается авто-конфигурация. 

#### 4. Есть разница если мы используем starter'ы илии пропишем все зависимости вручную, кроме того что изменится количество строк?
У стартеров есть автоконфигурация. Поэтому благодаря стартерам нам не надо настраивать конфигурацию вручную.

#### 5. Базовый зависимости Spring Boot.
* spring-boot-starter-web - создание Spring Boot приложения
* spring-boot-starter-data-jpa - подключение JPA :)

#### 6. Как подключиться к БД? 
Создать файл `application.properties` путь которого `src/main/resources/application.properties` со следующим содержимым:   
`spring.jpa.hibernate.ddl-auto=update
spring.datasource.url=jdbc:mysql://${MYSQL_HOST:localhost}:3306/db_example
spring.datasource.username=springuser
spring.datasource.password=ThePassword
spring.datasource.driver-class-name =com.mysql.jdbc.Driver
#spring.jpa.show-sql: true`
