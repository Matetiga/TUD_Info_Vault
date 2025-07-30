
### @Test
public void method()
- @Test identifies a method as a test method

---

### @Test(expected = Exception.class)
public void method()
- fails if the method does not throw the named exception

---

### @Before
public void method()
- this method is executed <span style="color:#ffff00">before each test</span> 
- just like setUp() in [[JUnit 3.8.2]]

---

### @After
public void method()
- this method is executed after each teste
- used as a cleanup task
- just like tearDown() in [[JUnit3.8.2]]

---

### @Ignore
public void method()
- to ignore the test method

---

### @BeforeClass
public <span style="color:#ffff00">static</span> void method()
- executed once<span style="color:#ffff00"> before all tests</span> for time intensive tasks 

---

### @AfterClasee
public <span style="color:#ffff00">static</span> void method()
- executed once<span style="color:#ffff00"> after all tests</span> for clean-up tasks

