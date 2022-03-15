#### 1. Какие есть сборщики проектов?
Maven, Gradle, Ant

#### 2. Maven
__Фазы (phases)__   
Жизненный цикл maven состоит из фаз.  
Основные фазы:  
1. __validate__ - проверятся вся ли инормация доступна для сборки, корректен ли проект
2. __compile__ - компилируются файлы с исходным кодом
3. __test__ - запускаются тесты
4. __package__ - скомпилированные файлы помещаются в архив (jar, war и т.д.)
5. __verify__ - идут проверки для подтверждения готовности упакованного файла
6. __install__ - пакет помещается в локальный репозиторий. Теперь он может использоваться другими программами как внешняя библиотека
7. __deploy__ - собранный архив копируется в удаленный репозиторий  
Все фазы запускаются последовательно, нельзя например запустить четвертую, и пропустить 1-3 фазы.  
Также у каждой фазы есть pre- и post- фазы. Например: pre-clean, post-clean, но используются они редко.  


__Цели (goals)__  
Каждая фаза представляет из себя последовательность целей. И каждая цель отвечает за определенную задачу.  

[Источник](https://www.baeldung.com/maven-goals-phases)

#### 3. Gradle
Gradle основан на графе задач, которые могут зависеть друг от друга. Задачи выполнят какую-то работу. 

#### 4. В чем различие maven и gradle?
Одному богу известно 

#### 5. Maven, в чем отличие `dependency` от `dependency-managment`?

#### 6. `scope` в `maven`

#### 7. Как в `Maven` вынести версии зависимостей Spring в одно место? 
    
    <properties>
        <spring.version>4.2.0.RELEASE</spring.version>
        <maven-clean.version>2.6.1</maven-clean.version>
    </properties>

    <dependencies>
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-context-support</artifactId>
            <version>${spring.version}</version>
        </dependency>
    </dependencies>
