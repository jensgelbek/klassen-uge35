# Uge35: Linux
### tirsdag d 25/8 

[Link til CPR-video II](https://youtu.be/R_b9QT7v-3o)

[Link til CPR-video III](https://youtu.be/N1fQIGzKWIA)

### onsdag d 25/8 


### Første øvelse
Nedenfor er der en liste over kommandoer. Og her en [video](https://youtu.be/wW8azHjdmwc) 
Opgaven består i at spotte de vi aktioner der forekommer

Editor - vi

1) micro cheat-sheet  
#### kommandoer  
  u : undo  
  n : redo last command  

#### navigation 

  vha hjkl tasterne  
  vha w tasten (ét ord ad gangen)  
  vha e + shift g  
  vha linjenummer + shift g  
  vha 0 : flyt hen til starten af linjen  
  vha $ : flyt hen til slutningen af linjen  


#### redigere
 
  x : sletter én karakter  
  dw : sletter et ord ad gangen  
  dd : sletter en linje ad gangen   
  4d : sletter 4 linjer (som er i clipboarden)  
  d + shift g : sletter fra cursoren og alle linjer neden under  
  shift d : sletter fra cursoren og resten af linjen  
  yy : kopierer en linje  
  yw : kopierer   
  yw : sletter og er klar til at erstatte med nyt   
  p : paster hvad der er gemt i clipboard   
  r : replace character  



### Anden øvelse

Hent de to settings-filer fra dagens repo
Diff de to filer
Tilføj vha cat forskellen til bunden af settings.xml
Åben settings.xml med vi og tilføj Id,username og password fra den anden fil

### Tredje øvelse - forberedelse
a) find doubletter  
kig på loc-prepare-1.txt og find ud af hvilken linje forekommer 2 gange  
kør nu flg kommando: cat loc-prepare-1.txt | sort | uniq -c  
åben filen og slet dubletten  
b) find ved hjælp af samme teknik - kombineret med cut - ud af hvor mange der kommer fra Køge  
c) kig på loc-prepare-2.txt og lav en liste over ip-adressernes hyppighed - samme teknik som ovenfor  


### Tredje øvelse
(der følger intro idag til kommandoerne nedenfor)

Hent loc.tar.bz2 fra dagens repo
Lav en folder hvor du kan pakke filen ud
Pak filerne ud i denne folder (tar og bzip2)
Find de unikke ip-adresser (grep, sort, uniq samt "pipe")  
Find ud hvor mange gang de optræder (uniq)

### Fjerde øvelse - jeopardy
Hent master_season1-35clean.tsv.gz
Lav en folder hvor du kan arbejde med filen 
hvor mange linjer? (enten vi eller cat | wc)
Lav en lille testfil med 10 linjer
(brug f.eks head og ">" til at lægge x antal linjer ind i en ny fil)

### Femte øvelse - jeopardy
brug cut til at hente det første felt ud og find hyppigheden (sort og uniq)
brug cut til at hente kategori-feltet ud og find hyppigheden

### sjette øvelse
(tricky og driller tit (mig :-))
Lav et lille java-projekt i intellij
Få Intellij til at lave en jar-fil (google!)
Flyt jar-filen til din droplet (sftp)

### extra øvelse
Kig på filen Jack-Challenge.csv som kommer fra excel, gem-som CSV UTF-8
Problemet er at der er multiline indhold i en af kolonnerne. 
"Heldigvis" er det "rigtige" linjeskift anderledes end linjeskiftet i cellen.
Opgaven går så ud på at få fjernet alle almindelige linjeskift så der kun er carriage return tilbage (0d).
De oversættes så til almindelige linjeskift (line feed, 0a)
værktøjer: asciitabel, tr og f.eks xxd til hexdump

### extra øvelse
Kig på file cars.csv
Hvor mange forskellige typer er der?
antag at du har en database med en tabel til biler. Den skal nu fyldes op med bilerne fra filen.
Overvej hvordan du kan bruge følgende:
cat  cars.csv |  while read x; do echo "insert into cars (..) values();";done

