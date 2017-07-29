# HashMap Class
*create and add objects in HashMap*
```java
HashMap<Integer, Integer> map = new HashMap<Integer, Integer>(); // Create objects
map.put(21,73); // add objects, 21 is the key, 73 is the value.
```

*retrieving value from HashMap*
```java
// using get method.
int key = 21;
int value = map.get(key);
```
>output
>73

*iterating over HashMap* 
the [set interface](http://www.codejava.net/java-core/collections/java-set-collection-tutorial-and-examples) and [iterator interface](https://www.tutorialspoint.com/java/java_using_iterator.htm) are two concepts to understand.

*size and clear in HashMap* 
the [synchronization](http://javarevisited.blogspot.sg/2011/04/synchronization-in-java-synchronized.html) is to understhand.

*contains keys and contains value*
```java
HashMap<Integer,String> map = new HashMap<Integer, String>();
map.put(21,"Jason");
map.put(22,"Zeyu");
System.out.println(map.containsKey(21));
System.out.println(map.containsValue(22));
System.out.println(map.containsValue("Zeyu"));
```
>output:
true
false
true

*check map size, clean map and check if map is empty*
```java
        HashMap<Integer,String> map = new HashMap<Integer, String>();
        map.put(21,"Jason");
        map.put(22,"Zeyu");
        System.out.println(map.size());
        System.out.println(map.isEmpty());
        map.clear();
        System.out.println(map.size());
        System.out.println(map.isEmpty());
```
>output
2
false
0
true

*remove ovject from map*
```java
        HashMap<Integer,String> map = new HashMap<Integer, String>();
        map.put(21,"Jason");
        map.put(22,"Zeyu");
        System.out.println(map.size());
        
        int key = 21;
        map.remove(21);
        System.out.println(map.size());
```
>output
2
1

*sort HashMap* 
[TreeMap](http://javarevisited.blogspot.com/2011/12/treemap-java-tutorial-example-program.html) is to understand.

[source](http://www.java67.com/2013/02/10-examples-of-hashmap-in-java-programming-tutorial.html)