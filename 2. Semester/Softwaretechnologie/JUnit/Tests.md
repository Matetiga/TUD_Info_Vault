## [[Exceptions]]
are not errors perse 


## Methoden
- setUp()
- tearDown()
- Pro Testfall ein Testmethode schreiben


**Rregressiontests**: Test should be ran each time the code is compiled

### Testen sollten in einer Testtabelle dargestellt werden
(*this test is made for the 02_Ubung*)


```Java
public class Inhabitant{
	protected int income;
	public int taxableIncome(){
	return income;
	}  
	public int tax(){
		// (int) ensures the operation returns an interger (removing any float number)
		int taxes = (int) (taxableIncome() * 0.1);
		if (taxes < 1){
			return 1;
		} 
		return taxes;
	} 
	public void setIncome(int income){
		
		this.income = income;
		
		}
	}
```

| ID  | Status    | klasse     | Parameter: int income | Outcome                                             |
| --- | --------- | ---------- | --------------------- | --------------------------------------------------- |
| T1  | OK        | Inhabitant | 42                    | 4                                                   |
| T2  | OK        | Inhabitant | 0                     | 1                                                   |
| T3  | OK        | Inhabitant | $2^{30}$              | $0.1*2^{30}$                                        |
| T4  | Exception | Inhabitant | -1                    | Income can not be negative    ->IllegalArgException |
| T5  | OK        | Inhabitant | 16                    | 1                                                   |
| T6  | OK        | Inhabitant | 9                     | 1                                                   |


| ID  | Status    | klasse | Parameter: int income | Outcome                    |
| --- | --------- | ------ | --------------------- | -------------------------- |
| T1  | OK        | Adel   | 30                    | 20                         |
| T2  | OK        | Adel   | 0                     | 20                         |
| T3  | Exception | Adel   | -1                    | Income can not be negative |
| T4  | OK        | Adel   | 400                   | 40                         |
|     |           |        |                       |                            |

| ID  | Status    | klasse | Parameter: int income | Outcome |
| --- | --------- | ------ | --------------------- | ------- |
| T1  | OK        | King   | 394868                | 0       |
| T2  | Exception | King   | -1                    | 0       |
| T3  | OK`       | King   | 0                     | 0       |

| ID  | Status | klasse | Parameter: int income | Outcome |
| --- | ------ | ------ | --------------------- | ------- |
| T1  | OK     | Serf   | 1                     | 1       |
| T2  | OK     | Serf   | 0                     | 1       |
| T3  | OK     | Serf   | -1                    | 1       |
| T4  | OK     | Serf   | 40                    | 2       |