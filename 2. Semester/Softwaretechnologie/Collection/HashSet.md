Schneller als [[Mengensortierung - TreeSet]]

```Java
class Warengruppe {
	private String name;
	private String lagerplatz;
	private Set<Artikel> inhalt;
	public Warengruppe
	(String name, String lagerplatz) {
		this.name = name;
		this.lagerplatz = lagerplatz;
		this.inhalt = new HashSet<Artikel>();
	}
	public void add (Artikel a) { inhalt.add(a); }
	public int anzahl() { return inhalt.size(); }
	public String toString() {
		String s = "Warengruppe "+name+"\n";
		Iterator it = inhalt.iterator();
		while (it.hasNext()) {
			s += " "+(Artikel)it.next();
		};
	}
}
```