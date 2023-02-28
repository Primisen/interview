## Java 8

## Java 11

## Java 13

## Java 17
**Что нового**  
Встретила мнение, что многие добавленные фичи упрощают реализацию machine learning программ на Java     
      
_Sealed Classes and Interfaces_ 
Эта функция предназначена для включения более тонкого контроля наследования в Java. Запечатывание позволяет классам и интерфейсам определять свои разрешенные подтипы.        
Другими словами, класс или интерфейс теперь могут определять, какие классы могут его реализовывать или расширять. Это полезная функция для моделирования предметной области и повышения безопасности библиотек.       
Ясность кода, непозволение злоупотреблять переиспользованием кода. (?)    
        
_Switch-выражения_
Было:           
`           
static String formatter(Object o) {                       
    String formatted = "unknown";                 
    if (o instanceof Integer i) {                       
        formatted = String.format("int %d", i);                        
    } else if (o instanceof Long l) {                      
        formatted = String.format("long %d", l);            
    } else if (o instanceof Double d) {         
        formatted = String.format("double %f", d);          
    } else if (o instanceof String s) {         
        formatted = String.format("String %s", s);          
    }             
    return formatted;         
`          
Стало:            
`           
static String formatterPatternSwitch(Object o) {            
    return switch (o) {       
        case Integer i -> String.format("int %d", i);       
        case Long l    -> String.format("long %d", l);            
        case Double d  -> String.format("double %f", d);                
        case String s  -> String.format("String %s", s);                
        default        -> o.toString();               
    };                  
}
`      
                        
_Records_                 
Объявление легковесного класса без тонны стандартного кода:             
`record Person(int id, String name){}`          

        
**Преимущества**      
Существенно перебран GC. Java 17 где-то в среднем на 7% эффективнее для сборщиков мусора      
          
**Недостатки**    
Во-первых, в ней **отсутствуют 100% обратной совместимости**. Мы привыкли, что обратная совместимость — это главная концепция, вокруг которой выстраиваются новые версии Java. Но в 17 было удалено довольно большое количество методов, которые до этого обозначались как deprecated. Также многие внутренние модули изменили видимость и стали приватными. Поэтому теперь у вас нет к ним доступа.
