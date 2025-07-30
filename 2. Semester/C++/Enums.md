```cpp
namespace my_ns {
	enum wochentag {
		montag = 0, //< expliziter Wert
		dienstag, // wert = 1
		mittwoch, // 2 ...
		donnerstag,
		freitag,
		samstag,
		sonntag = 9 // < neuer Wert
	};
}
// werte name auf gleichem level wie
// typ sichtbar
my_ns::wochentag w = my_ns::montag;
```