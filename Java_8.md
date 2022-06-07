### Stream
#### 1. How to calculate sum value of fields of every collection element?
 int sum = widgets.stream()    
                      .mapToInt(w -> w.getWeight())     
                      .sum();     
