
<span style="color:#1fffc7">fail()</span> => if this is reached, means no exceptions have been found


## Timeout
if a test passes a time limit
```Java
public class EuroTest(){

	@Test (timeout = 100)
	public void performTest(){
		...
		}
}
```