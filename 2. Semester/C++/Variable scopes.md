```cpp
int i = 5;
{
	int i = 7; // dieses i verdeckt
	// das äußere i
	cout << "i = " << i << endl;
	// Ausgabe: i = 7
} // Ende des Blocks. Hier wird das
  // innere i zerstört

cout << "i = " << i << endl;
// Ausgabe: i = 5
```