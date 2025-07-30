javac -cp *path/to/junit.jar*:. *file_name*


## Compile
### Example:
inside: /Martin/VsCode/Java/03_Final_Ubung
- javac -cp ../junit3.8.2/junit.jar:. tests/AdelTest.java

---
## Run
- java -cp ../junit3.8.2/junit.jar:. <span style="color:#ffff00">junit.textui.TestRunner </span>tests<span style="color:#00ff04">.</span>AdelT
est 

###### the point between tests.AdelTest is because Adeltest is found within tests folder

---
# Important to note:            :.
- the double dots ( : ) is to include another directory
- the dot ( . ) is to include the current directory
