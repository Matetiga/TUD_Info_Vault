Used to have an own implementation on how to compare two objects

## Implementation
- Implement the method `equals()`
- Implement the method `HashCode`
	- this must be implemented *for HashSet and Hashmap* 
	- this helps the HashSet/Map to decide weather two objects are the same


### Equals()
- checks if two objects are the same
	- if it is not overridden => default implementation decides the similarity of two objects based on their spot in memory (**same memory allocation == same object**)

### HashCode
- used in Hash based collection 


---
## Example code

```Java
// without equals being overridden 
HashSet<Person> people = new HashSet<>();
people.add(p1);
people.add(p2);

System.out.println(people.size()); // This will print 2

```


```Java
// equals is not overridden

Person p1 = new Person("Alice", 30);
Person p2 = new Person("Alice", 30);

System.out.println(p1.equals(p2)); // This will print false
```

```java
public class Person implements Comparable<Person> {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Getters for name and age
    public String getName() {
        return name;
    }

    public int getAge() {
        return age;
    }

    @Override
    public int compareTo(Person other) {
        return Integer.compare(this.age, other.age);
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) {
            return true; // Check if the objects are the same instance
        }
        if (obj == null || getClass() != obj.getClass()) {
            return false; // Check if obj is null or of different class
        }
        Person person = (Person) obj;
        return age == person.age && name.equals(person.name); // Compare fields
    }

    @Override
    public int hashCode() {
        int result = name.hashCode();
        result = 31 * result + age;
        return result;
    }

```