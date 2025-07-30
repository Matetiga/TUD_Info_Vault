Test suites are used to group similar tests, that should be ran one after the other

```Java
import junit.framework.*;
import junit.swingui.TestRunner;

public class AlleTestsKoenigreich {
	public static Test suite() {
		// this line creates a new instance of TestSuite
		// suite object is created
		TestSuite suite = new TestSuite("una vaina loca");

		// adding tests classes to the suite
		suite.addTestSuite(EinwohnerTest.class);
		suite.addTestSuite(KoenigTest.class);
		suite.addTestSuite(AdelTest.class);
		suite.addTestSuite(BauerTest.class);
		suite.addTestSuite(LeibeigenerTest.class);
		return suite;
	
	}
	// Calling main provokes AlleTestsKoenigreich to be called
	//  that means "main" is mandatory to run all test suites
	public static void main(String[] args) {	
	TestRunner.run(AlleTestsKoenigreich.class);
	
	}

}
```

##### new TestSuite(*String name*)
##### .addTestSuite(*Class testClass*)