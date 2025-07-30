## [[Annotations]]
[[Exceptions]]

#### In JUnit 4 it is not necessary to have a TestSuite


```Java
import static org.junit.Assert.*;
import org.junit.Before;
import org.junit.Test;

// the class does not have to be an extension of TestClass
public class AdelTest {
	private Adel adel;

	@Before
	public void setUp() {
		adel = new Adel();
	} 
	
	@Test
	public void testSteuerA1() {
		try {
			adel.setEinkommen(-1);
			fail("Keine Exception aufgetreten");
		} catch (IllegalArgumentException e) {
			assertEquals("Einkommen darf nicht negativ sein", e.getMessage());
		}
	}
	// this i also a valid syntax when a test expects an exception 
	@Test (expected = IllegalArgumentException.class)
		public void testSteuerE5(){
		einwohner.setEinkommen(-12);
	}

	@Test
	public void testSteuerE2() {
		einwohner.setEinkommen(0);
		assertEquals(1, einwohner.steuer());
	}
}
```


###### To run this tests VsCode has a extension (**Testing**)  located in the left side

### @Test
tests that <span style="color:#ffff00">expect an exception</span> can have this syntax:
- <span style="color:#1fffc7">@Test (expected = Exception.class)</span>

Otherwise a <span style="color:#ffff00">try-catch block </span>can be used:
```Java
	@Test
	public void testSteuerA1() {
		try {
			adel.setEinkommen(-1);
			fail("Keine Exception aufgetreten");
		} catch (IllegalArgumentException e) {
			assertEquals("Einkommen darf nicht negativ sein", e.getMessage());
		}
	}
```