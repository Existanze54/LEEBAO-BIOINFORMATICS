# LEEBAO-BIOINFORMATICS

Хакатон по биоинформатике Лаборатории экологии и эволюционной биологии водных организмов ДВФУ

## ДЕНЬ 08. БАЗЫ ДАННЫХ

### БАЗЫ ГЕНОМНЫХ ДАННЫХ:
* [INSDC: International Nucleotide Sequence Database Collaboration](http://www.insdc.org/)
* [NCBI: National Center for Biotechnology Information](http://www.ncbi.nlm.nih.gov/)
* [EMBL: European Molecular Biology Laboratory](http://www.embl.org/)
* [DDBJ: DNA Data Bank of Japan](http://www.ddbj.nig.ac.jp/)
* [ENSEMBL](https://www.ensembl.org/index.html)
* [UCSC Genome Browser](http://hgdownload.soe.ucsc.edu/downloads.html)
* [FlyBase](http://flybase.org/)
* [WormBase](https://www.wormbase.org/)
* [SGD: Saccharomyces Genome Database](http://www.yeastgenome.org/)
* [RNA-Central](http://rnacentral.org/)
* [TAIR](https://www.arabidopsis.org/)
* [EcoCyc](http://ecocyc.org/)
* [HUMAN1000](https://www.internationalgenome.org/)
* [ENCODE](https://www.encodeproject.org/)
* [UniProt: Swiss-Prot & TrEMBL](https://www.uniprot.org/)
* [Virus Pathogen Resource](https://www.viprbrc.org/)


### БАЗЫ ДАННЫХ NCBI

| Имя базы NCBI | Описание |
| --------- | --------- |
| [`assembly`](https://www.ncbi.nlm.nih.gov/assembly) | Сборки | 
| [`biocollections`](https://www.ncbi.nlm.nih.gov/biocollections) | Музейные коллекции | 
| [`bioproject`](https://www.ncbi.nlm.nih.gov/bioproject) | Проекты | 
| [`biosample`](https://www.ncbi.nlm.nih.gov/biosample) | Биологические материалы | 
| [`biosystems`](https://www.ncbi.nlm.nih.gov/biosystems) | Биологические системы | 
| [`books`](https://www.ncbi.nlm.nih.gov/books) | Книги | 
| [`clinvar`](https://www.ncbi.nlm.nih.gov/clinvar) | Изменчивость генома человека | 
| [`gap`](https://www.ncbi.nlm.nih.gov/gap) | Генотип и фенотип | 
| [`dbvar`](https://www.ncbi.nlm.nih.gov/dbvar) | Структурная вариация | 
| [`gene`](https://www.ncbi.nlm.nih.gov/gene) | Гены | 
| [`genome`](https://www.ncbi.nlm.nih.gov/genome) | Геномы | 
| [`gds`](https://www.ncbi.nlm.nih.gov/gds) | Экспрессия генов | 
| [`geoprofiles`](https://www.ncbi.nlm.nih.gov/geoprofiles) | Индивидуальная экспрессия генов | 
| [`gtr`](https://www.ncbi.nlm.nih.gov/gtr) | Генетические тесты | 
| [`homologene`](https://www.ncbi.nlm.nih.gov/homologene) | Генные гомологи | 
| [`ipg`](https://www.ncbi.nlm.nih.gov/geoprofiles) | Идентичные белки | 
| [`medgen`](https://www.ncbi.nlm.nih.gov/medgen) | Медицинские данные |
| [`mesh`](https://www.ncbi.nlm.nih.gov/mesh) | Медицинские термины |
| [`ncbisearch`](https://www.ncbi.nlm.nih.gov/ncbisearch) | Сайт NCBI |
| [`nlmcatalog`](https://www.ncbi.nlm.nih.gov/nlmcatalog) | National Library of Medicine |
| [`nuccore`](https://www.ncbi.nlm.nih.gov/nuccore) | ГенБанк |
| [`omim`](https://www.ncbi.nlm.nih.gov/omim) | Банк генетических заболеваний |
| [`pmc`](https://www.ncbi.nlm.nih.gov/pmc) | Журналы PMC |
| [`popset`](https://www.ncbi.nlm.nih.gov/popset) | Популяционные данные |
| [`protein`](https://www.ncbi.nlm.nih.gov/protein) | Белки |
| [`proteinclusters`](https://www.ncbi.nlm.nih.gov/proteinclusters) | Белковые кластеры |
| [`pcassay`](https://www.ncbi.nlm.nih.gov/pcassay) | Активность веществ |
| [`pccompound`](https://www.ncbi.nlm.nih.gov/pccompound) | Химические соединения |
| [`pcsubstance`](https://www.ncbi.nlm.nih.gov/pcsubstance) | Химические вещества |
| [`pubmed`](https://www.ncbi.nlm.nih.gov/pubmed) | Онлайн библиотека |
| [`snp`](https://www.ncbi.nlm.nih.gov/snp) | Нуклеотидные полиморфизмы |
| [`sparcle`](https://www.ncbi.nlm.nih.gov/sparcle) | Функциональная структура белков |
| [`sra`](https://www.ncbi.nlm.nih.gov/sra) | Короткие последовательности |
| [`structure`](https://www.ncbi.nlm.nih.gov/structure) | Структура макромолекул |
| [`taxonomy`](https://www.ncbi.nlm.nih.gov/taxonomy) | Таксономия |
| [`toolkit`](https://www.ncbi.nlm.nih.gov/toolkit) | Программы |


### ПОЛЯ ЗАПРОСОВ NCBI

| Имя Поля  | Аббревиатура | Функция | Базы NCBI |
| --------- | --------- | --------- | --------- | 
| `[Accession]` | `[ACCN]` | Идентификатор NCBI | Все |
| `[All Fields]` | `[ALL]` | Все поля | Все |
| `[Author]` | `[AU]` / `[AUTH]` | Автор | Все |
| `[Feature Key]` | `[FKEY]` | Характеристики | Nucleotide, Protein, GSS |
| `[Filter]`| `[FILT]` / `[SB]` | Фильтрация / Исключение | Все |
| `[Genome Project]`|  | Числовой идентификатор геномного проекта | Все |
| `[Issue]` | `[ISS]` | Номер журнала | Все |
| `[Journal]` | `[JOUR]` | Журнал | Все |
| `[Keyword]` | `[KYWD]` | Ключевое слово | Все |
| `[Modification Date]` | `[MDAT]` | Дата последнего изменения | Все |
| `[Molecular Weight]` | `[MOLWT]` | Молекулярный вес | Protein |
| `[Organism]` | `[ORGN]` | Латинское или народное название организма | Все |
| `[Page Number]` | `[PAGE]` | Страница | Все |
| `[Primary Accession]` | `[PACC]` | Основной идентификатор | Все |
| `[Primary Organism]` | `[PORGN]` | Основной организм | Все |
| `[Properties]` | `[PROP]` | Свойства | Все |
| `[Protein Name]` | `[PROT]` | Название белка | Все |
| `[Publication Date]` | `[PDAT]` | Дата публикации | Все |
| `[SeqID String]` | `[SQID]` | Идентификатор последовательности | Все |
| `[Sequence Length]` | `[SLEN]` | Длина последовательности | Все |
| `[Substance Name]` | `[SUBS]` | Название вещества | Все |
| `[Text Word]` | `[WORD]` | Описание | Все |
| `[Title]` | `[TI]` / `[TITL]` | Заголовок | Все |
| `[TITL]` | `[VOL]` | Том | Все |


### УПРАЖНЕНИЯ

1. ENTREZ API

2. Установка ENTREZ:

* Для установки программ создайте директорию `PROGRAMS` в вашей домашней директории
* Скачайте [Entrez](ftp://ftp.ncbi.nlm.nih.gov/entrez/entrezdirect/edirect.tar.gz) в директорию `PROGRAMS`
* Распакуйте архив
* Удалите архив
* Переименуйте директорию `edirect` в `EntrezDirect`
* Добавьте путь к директории в ваш BASH профайл для запуска программ Entrez по умолчанию 
```
echo "export PATH=${PATH}:$HOME/PROGRAMS/EntrezDirect" >> $HOME/.profile
```
* Запустите внутренний скрипт-установщик ENTREZ
```
cd EntrezDirect
./setup.sh
```
* Перезапустите терминал
* Проверьте установку, запустив несколько пробных команд
```
esearch -version
xtract -version
esearch -db pubmed -query "Babalobi OO[au] AND 2008[pdat]" | 
```

