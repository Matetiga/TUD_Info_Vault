[[Compile and Run JUnit Tests]]
[[Suites]]
[[Exceptions]]

## setUp() - Method
#### This method is ran BEFORE each Test
- used to initialize objects
- establishing databases conennections

###### it is commonly used to create new instances of objects
```Java
import junit.framework.TestCase;

public class KoenigTest extends TestCase{
	private Koenig koenig;

	protected void setUp(){
		koenig = new Koenig();
	}
}
```


---

## tearDown() - Method
#### This method is ran AFTER each Test
- is used to <span style="color:#ffffff">perform cleanup</span> tasks 
- closing databases connections
- deleting temporary test data
- releasing file handles

