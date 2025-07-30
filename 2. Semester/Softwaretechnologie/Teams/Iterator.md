- Folge von Objekten 

### Java Klasse
```Java
java.io.InputStream
```

#### Implementierungmuster Iterator
```Text
T thing;
List<T> list;
..
Iterator<T> i = list.iterator();
while (i.hasNext()) {
	doSomeThing(i.next());
}
```
