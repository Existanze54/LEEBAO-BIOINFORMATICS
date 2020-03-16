# LEEBAO-BIOINFORMATICS

Хакатон по биоинформатике Лаборатории экологии и эволюционной биологии водных организмов ДВФУ

## ДЕНЬ 09. АНАЛИЗ КОРОНАВИРУСОВ

### Severe acute respiratory syndrome-related coronavirus (SARS-CoV-2)<br/>Острое респираторное инфекционное заболевание (ОРВИ)

<img src="https://www.viprbrc.org/brc/images/2019_nCoV_virion_genome.png" 
alt="SARS coronavirus" width="600" border="5" />

### ИНФОРМАЦИЯ ПО COVID-19

* [Statistics: Information is Beautiful](https://informationisbeautiful.net/visualizations/covid-19-coronavirus-infographic-datapack/)
* [NCBI: SARS-CoV-2](https://www.ncbi.nlm.nih.gov/genbank/sars-cov-2-seqs/)
* [GISAID: Global Initiative on Sharing All Influenza Data](https://www.gisaid.org/)
* [Virus Pathogen Resource: SARS-CoV-2](https://www.viprbrc.org/brc/home.spg?decorator=corona_ncov)
* [China National GeneBank: 2019-nCoV Database](https://db.cngb.org/datamart/disease/DATAdis19/)
* [UniProt: Wuhan 2019-2020 Coronavirus](http://insideuniprot.blogspot.com/2020/02/wuhan-2019-2020-coronavirus-uniprotkb.html)
* [World Health Organization (WHO): novel-coronavirus-2019](https://www.who.int/emergencies/diseases/novel-coronavirus-2019)

### АЛЬТЕРНАТИВНЫЕ НАЗВАНИЯ ВИРУСА

* SARS-CoV-2
* 2019-nCoV
* nCoV-2019
* BetaCov

### ПРОВЕРЯЕМ ПУБЛИКАЦИИ В NCBI PUBMED

##### 1. Сколько всего публикаций в 2020 году с "2019-nCoV" в заголовке статьи?
```
esearch -db pubmed -query "2019-nCoV[TITL] AND 2020[PDAT]"
```

##### 2. Скачиваем абстракты
```
esearch -db pubmed -query "2019-nCoV[TITL] AND 2020[PDAT]" | \
efetch -format abstract -mode text > abstracts2020.txt
```

##### 3. Создаем список авторов
```
esearch -db pubmed -query "2019-nCoV[TITL] AND 2020[PDAT]" | \
efetch -format xml | \
xtract -pattern PubmedArticle -block Author -sep " " -tab "\n" -element LastName,ForeName | \
sort | uniq -c | sort -nr | more
```

##### 4. Создаем список подразделений
```
esearch -db pubmed -query "2019-nCoV[TITL] AND 2020[PDAT]" | \
efetch -format xml | \
xtract -pattern PubmedArticle -block Author -sep " " -tab "\n" -element Affiliation | \
sort | uniq -c | sort -nr | more
```

### СКАЧИВАЕМ ДАННЫЕ ИЗ NCBI

##### 1. Создаем запрос для всех коронавирусов
```
esearch -db nucleotide -query "coronavirus"
```

##### 2. Создаем запрос для всех коронавирусов с фильтрацией по полноте генома и времени публикации
```
esearch -db nucleotide -query "coronavirus" | \
efilter -query "complete genome[TITL]" -days 100
```

##### 3. Скачиваем описание последовательностей в формате генного банка
```
esearch -db nucleotide -query "coronavirus" | \
efilter -query "complete genome[TITL]" -days 100 | \
esummary -format gb -mode text > coronavirus.gb
```

##### 4. Скачиваем описание последовательностей в FASTA формате
```
esearch -db nucleotide -query "coronavirus" | \
efilter -query "complete genome[TITL]" -days 100 | \
efetch -format fasta > coronavirus.fasta
```