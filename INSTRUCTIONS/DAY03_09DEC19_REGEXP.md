# LEEBAO-BIOINFORMATICS

Хакатон по биоинформатике Лаборатории экологии и эволюционной биологии водных организмов ДВФУ

## ДЕНЬ 03. РЕГУЛЯРНЫЕ ВЫРАЖЕНИЯ

## СОДЕРЖАНИЕ

1. [ОСНОВЫЕ КОМАНДЫ РЕГУЛЯРНЫХ ВЫРАЖЕНИЙ](https://github.com/vinni-bio/LEEBAO-BIOINFORMATICS/blob/master/INSTRUCTIONS/DAY03_09DEC19_REGEXP.md#1-%D0%BE%D1%81%D0%BD%D0%BE%D0%B2%D1%8B%D0%B5-%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D1%8B-%D1%80%D0%B5%D0%B3%D1%83%D0%BB%D1%8F%D1%80%D0%BD%D1%8B%D1%85-%D0%B2%D1%8B%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D0%B9)
2. [ДАННЫЕ ДЛЯ ТРЕНИРОВКИ](https://github.com/vinni-bio/LEEBAO-BIOINFORMATICS/blob/master/INSTRUCTIONS/DAY03_09DEC19_REGEXP.md#2-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%B5-%D0%B4%D0%BB%D1%8F-%D1%82%D1%80%D0%B5%D0%BD%D0%B8%D1%80%D0%BE%D0%B2%D0%BA%D0%B8)
     
### 1. ОСНОВЫЕ КОМАНДЫ РЕГУЛЯРНЫХ ВЫРАЖЕНИЙ
|ЯКОРЯ | СИМВОЛЫ | КВАНТОРЫ |
| --------- | --------- | --------- |
|`^` – начало строки | `\c` – управляющий символ | `*` – 0 или больше|
|`\A` – начало текста | `\s` – пробел | `*?` – 0 или больше, нежадный |
|`$` – конец строки | `\S` – не пробел | `+` – 1 или больше |
|`\Z` – конец текста | `\d` – цифра | `+?` – 1 или больше, нежадный |
|`\b` – граница слова | `\D` – не цифра | `?` – 0 или 1 |
|`\B` – не граница слова | `\w` – слово | `??` – 0 или 1, нежадный |
|`\<` – начало слова | `\W` – не слово| `{3}` – ровно 3 |
|`\>` – конец слова | | `{3,}` – 3 и больше |
| | | `{3,5}` – 3,4 или 5 |
| | | `{3,5}?` – 3,4 или 5, нежадный |

|СПЕЦ СИМВОЛЫ | ДИАПАЗОНЫ | 
| --------- | --------- |
|`\` – отмена (экран) | `.` – любой символ |
|`\n` – новая строка | `(a\|b)` – a или b |
|`\r` – возврат каретки | `(...)` – группа |
|`\t` – табуляция | `(?:...)` – нежадная группа |
|`\v` – вертикальная табуляция | `[abc]` – a или b или с |
|`\f` – новая страница | `[^abc]` – не a, не b и не с|
|`\e` – escape символ | `[a-q]` – между a и q|
| | `[1-7]` – между 1 и 7|

##### МЕТАСИМВОЛЫ, которые должны экранироваться
```
^ $ ( ) < > { } [ ] \ | . * + ?
```

## 2. Данные для тренировки

##### Для упражнений вам потребуется блокнот Brackets. Инструкции по его установке находятся [здесь](https://github.com/vinni-bio/LEEBAO-BIOINFORMATICS/blob/master/INSTRUCTIONS/DAY01_25NOV19_LINUX.md#i-%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%BE%D0%B2%D0%BE%D0%B3%D0%BE-%D1%80%D0%B5%D0%B4%D0%B0%D0%BA%D1%82%D0%BE%D1%80%D0%B0-brackets)

* [Названия видов](https://raw.githubusercontent.com/vinni-bio/LEEBAO-BIOINFORMATICS/master/FILES/species.txt)
* [Аминокислотные последовательности](https://raw.githubusercontent.com/vinni-bio/LEEBAO-BIOINFORMATICS/master/FILES/proteins.fas)
* [Географические координаты](https://raw.githubusercontent.com/vinni-bio/LEEBAO-BIOINFORMATICS/master/FILES/coordniates.txt)
* [Журнал наблюдений](https://raw.githubusercontent.com/vinni-bio/LEEBAO-BIOINFORMATICS/master/FILES/observations.txt)


