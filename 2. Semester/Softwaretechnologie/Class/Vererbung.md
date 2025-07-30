### Nicht mehrfach vererben!
#### [[Biologisches Programmieren]]

| Person   | Professor    | Stundent         |
| -------- | ------------ | ---------------- |
| wakeUp() | wakeUp()     | wakeUp()         |
| work()   | work()       | work()           |
| sleep()  | sleep()      | sleep()          |
|          | giveLecure() | recieveLecture() |

#### the professor and student class have similarities to Person

## Refactoring (Vererbungsrelations werden refaktorisiert)

```Java
Professor extends Person {};
Student extends Person {};
```

![[Vererbungrelationen.canvas]]
```Java
drinksBeer extends Person {};
Professor extends drinkBeer {};
Stundent extends drinkBeer {};
```
