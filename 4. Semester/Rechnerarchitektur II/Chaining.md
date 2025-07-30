## Ohne Chaning
- $k_{mul}-1+n+k_{add}-1+n + n_{io}$
- mit $n_{io}$ die extra Takte für Instruction Fetch, Instruction Decode und Writeback
	- $n_{io}=4$ da die Addition erst **nach dem WB von der Multiplikation** durchgeführt werden kann 



	## Mit Chaining
Addition fängt es an, wenn das **erste Element der Multiplikation fertig ist** 