## Key - Value => Pairs

```Java
class Katalog {
	private String name;
	private Map<String,Artikel> inhalt; // Polymorphe Map
	public Katalog (String name) {
		this.name = name;
		this.inhalt = new HashMap<String,Artikel>();
	}
	public void put (String code, Artikel a) {
		inhalt.put(code,a);
	}
	public int anzahl() {
		return inhalt.size();
	}
	public Artikel get (String code) {
		return inhalt.get(code);
	}
	...
}
```