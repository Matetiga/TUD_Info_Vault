---
type:
  - words
aliases:
  - japanese
---
(word:: kore)
translation:: this


[word:: oishii]
translation:: delicious

keeki
cake

```dataview
TABLE word AS Japanaese, translation
WHERE file.name = "Hiragana"
```



```dataview
TABLE word, translation
FROM "Japanese"
```


```dataview
TABLE translation
WHERE contains(word, "kaake")
```



| word  | translation |
| ----- | ----------- |
| keeki | cake        |
| kore  | this        |
| sore  | that        |
|       |             |
