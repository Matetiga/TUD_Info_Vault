## Eigenschaften
4B/5B encoding is a block coding technique designed to improve efficiency and ensure sufficient signal transitions for clock recovery
- Maps blocks of 4 Bits into predefined 5 Bit-code words


### 5-Bit code words Eigenschaften
- 16 5-Bit code words are used for Data, the rest are for control purposes
- There are at least *two 1* in the 5-Bit code word (preventing long sequences of 0, which would cause synchronization loss)
- Transmitted using NRZI (**Non Return to Zero Inverted**) 
	- 1 causes a Signal transition
	- 0 maintains current Signal level


Higher efficiency compared with [[Manchester Code]], because it only adds 25% baud Overhead 
- So 100Mbps only requires 125 MHz
- (With Manchester Code it would require 200 MHz)