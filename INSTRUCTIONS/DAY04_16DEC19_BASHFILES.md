# LEEBAO-BIOINFORMATICS

Хакатон по биоинформатике Лаборатории экологии и эволюционной биологии водных организмов ДВФУ

## ДЕНЬ 04. ОПЕРАЦИИ С ФАЙЛАМИ В КОНСОЛИ BASH. ПЕРВЫЙ СКРИПТ.

## СОДЕРЖАНИЕ

1. [РАЗМИНКА](https://github.com/vinni-bio/LEEBAO-BIOINFORMATICS/blob/master/INSTRUCTIONS/DAY04_16DEC19_BASHFILES.md#1-%D1%80%D0%B0%D0%B7%D0%BC%D0%B8%D0%BD%D0%BA%D0%B0)
2. [УПРАЖНЕНИЯ](https://github.com/vinni-bio/LEEBAO-BIOINFORMATICS/blob/master/INSTRUCTIONS/DAY04_16DEC19_BASHFILES.md#2-%D1%83%D0%BF%D1%80%D0%B0%D0%B6%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F)
3. [СЖАТИЕ ДАННЫХ](https://github.com/vinni-bio/LEEBAO-BIOINFORMATICS/blob/master/INSTRUCTIONS/DAY04_16DEC19_BASHFILES.md#3-%D1%81%D0%B6%D0%B0%D1%82%D0%B8%D0%B5-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85)
4. [НАШ ПЕРВЫЙ СКРИПТ](https://github.com/vinni-bio/LEEBAO-BIOINFORMATICS/blob/master/INSTRUCTIONS/DAY04_16DEC19_BASHFILES.md#4-%D0%BD%D0%B0%D1%88-%D0%BF%D0%B5%D1%80%D0%B2%D1%8B%D0%B9-%D1%81%D0%BA%D1%80%D0%B8%D0%BF%D1%82)
5. [ИЗМЕНЕНИЕ ПРАВ ПОЛЬЗОВАНИЯ ФАЙЛАМИ]()
6. [ШЕБАНГ И СТРОКА ЗАПУСКА ИНТЕРПРЕТАТОРА СКРИПТА]()

### 1. РАЗМИНКА 

```
mkdir CLASS
cd CLASS
wget https://raw.githubusercontent.com/vinni-bio/LEEBAO-BIOINFORMATICS/master/FILES/north-pacific-gyre/2012-07-03/NENE01729A.txt
ls -la
head NENE01729A.txt
tail NENE01729A.txt
less NENE01729A.txt
```

<img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" 
alt="GITHUB LOGO" width="120" border="5" />

**Скачивание всей гитхаб директории**
```
git clone https://github.com/vinni-bio/LEEBAO-BIOINFORMATICS.git
cd LEEBAO-BIOINFORMATICS/FILES
ls -al
```

**Обновление гитхаб директории**
```
git pull
```

**Поиск с помощью команды `find`**
```
find LEEBAO-BIOINFORMATICS
find LEEBAO-BIOINFORMATICS -type f
find LEEBAO-BIOINFORMATICS -type d
find LEEBAO-BIOINFORMATICS -type f -name "NENE*.txt"
find LEEBAO-BIOINFORMATICS -name "*.seq" -or -name "*.fas" -type f
find LEEBAO-BIOINFORMATICS \( -name "NENE*.txt" -type f \) -or \( -name "north*" -type d \)
find LEEBAO-BIOINFORMATICS -type f -name "NENE*.txt" -print
find LEEBAO-BIOINFORMATICS -type f -name "NENE*.txt" -exec wc -l {} \;
find LEEBAO-BIOINFORMATICS -type f -name "NENE*.txt" -delete
```

### 2. УПРАЖНЕНИЯ 

##### Начало игры
* переместитесь в директорию "2012-07-03"
* сохраните все данные в один файл
* отсортируйте значения измерений и сохраните их в новый файл

##### Конкатенация, wildcards и grep:
* переместитесь в директорию "Sequences"
* сохраните все названия файлов в отдельный файл seqnames.txt
* объедините все последовательности в один файл
* создайте отдельный файл с названиями последовательностей
* проверьте сколько раз в каждом файле был обнаружен паттерн "GAATTC"

##### Shaver et al.:
* скачайте файл с экспериментальными данными из Shaver et al., 2007
* выведите на экран заголовок таблицы
* сколько всего записей содержит таблица?
* сохраните в отдельный файл записи, касающиеся сборов в Toolik Lake (4й столбец)
* из них отдельно сохраните записи особей, собранных в августе

### 3. СЖАТИЕ ДАННЫХ

##### Создание архива (Create, a Zipped, File with Verbose)
```
tar czfv архив.tar.gz путь/к/файлу1 путь/к/файлу2
ИЛИ
gzip путь/к/файлу1 
```

##### Распаковка архива (eXtract, a Zipped, File with Verbose)
```
tar xzfv архив.tar.gz
ИЛИ
gunzip путь/к/файлу1.gz 
```

### 4. НАШ ПЕРВЫЙ СКРИПТ
```
mkdir TEST
cd TEST
touch NENE.sh
ls -al
nano NENE.sh               #### ПИШЕМ СКРИПТ
ls -al
chmod 744 NENE.sh
./NENE.sh
```

### 5. ИЗМЕНЕНИЕ ПРАВ ПОЛЬЗОВАНИЯ ФАЙЛАМИ
```
sudo chmod ugo+rwx path/to/file
sudo chmod 744 path/to/file
```
##### Пояснение каждого аргумента команды:

   `sudo` - запуск команды с правами администратора  
   `chmod` – команда, которая изменяет права доступа к файлу  
   `u` – главный пользователь  
   `g` – пользовательская группа  
   `o` – другие пользователи (гости)  
   `+` – добавление прав  
   `-` – ограничение прав  
   `r` – право на чтение файла  
   `w` - право на изменение файла  
   `x` – право на запуск файла  
   `400` – чтение главным пользователем (код)  
   `200` – изменение главным пользователем (код)  
   `100` – запуск главным пользователем (код)  
   `700` – запуск, изменение и чтение главным пользователем (код)  
   `600` – изменение и чтение главным пользователем (код)  
   `500` – запуск и чтение главным пользователем (код)  
   `744` – чтение всеми, а изменение и запуск только главным пользователем (код)  

### 6. ШЕБАНГ И СТРОКА ЗАПУСКА ИНТЕРПРЕТАТОРА СКРИПТА
```
#! /bin/bash
ИЛИ ЛУЧШЕ ВСЕГДА ИСПОЛЬЗОВАТЬ
#! /usr/bin/env bash 
```

