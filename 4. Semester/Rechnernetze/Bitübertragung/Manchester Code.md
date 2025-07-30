## Eigenschaften
- Each Bit period is divided into two halves 
- A transition *occurs at the midpoint* of each bit period, with the direction of the **transition indicating the bit value** 
- Transitions at the *start of a bit period* (if any) **ensure the signal is in the correct state** for the mid-bit transition but carry no data
- This makes the signal **self-clocking** 

### Transition Indicating Bit Value
- **1** : for transition from *high-to-low*
- **0** : for transition from *low-to-high*


### Bespiel 
- Das Data *1010* wird wie gefolgt encodiert
- `10 01 10 01`
	- für jede **1** im Data : *10* 
	- für jede **0** im Data : *01* 


