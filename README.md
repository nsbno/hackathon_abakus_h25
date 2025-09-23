# Hackathon med Vy - Abakus H25

Dette repoet er ment som et skjelett dere kan bruke for å jobbe med caset dere har fått presentert i Kaggle-konkurransen. I repoet finner dere tre hovedmapper: 

## Struktur
* `/data` - I denne mappen kan dere legge datafilene som tilhører caset. 
* `/notebooks` - Denne mappen er område hvor dere kan jobbe. Her ligger det en notebook allerede med skjelett-kode som dere fritt kan bruke som utgangspunkt til å komme i gang. Denne tar utgangspunkt i at dere bruker python, og en guide for oppsettet finner dere under i denne readme-en.
* `/submissions` - Her kan dere lagre filene dere laster opp. Typisk vil dere skrive en fil fra en notebook i `/notebooks` til denne mappen med riktig format. Her kan det være lurt å tagge fil-navnene på en eller annen måte for å kunne skille mellom submissions (e.g. ved timestamp, versjonsnr, eller en kort beskrivelse av forskjell fra tidligere submissions)

## Oppsett for eksisterende skjelett-notebook
For å kjøre notebooken som ligger i `/notebooks` trenger vi tilgang til en del biblioteker som vi må installere. Disse ligger i `requirements.txt`-filen, men når vi jobber på tvers av ulike prosjekt kan ulike prosjekt bruke ulike versjoner og ulike pakker. For å skille mellom disse ulike behovene kan man benytte virtualenv-pakken i python for å sette opp et virtuelt miljø som man kan installere kun de pakkene man trenger og med riktige versjoner.

### Virtuelt miljø

For å installere selve pakken som setter opp det virtuelle miljøet kjører du
```sh
python -m pip install virtualenv
```
Når dette er gjort oppretter du det nye miljøet ved å kjøre
```sh
python -m venv env
```
> `venv` peker da til pakken som vi nettopp installerte, og `env` er navnet vi ønsker å gi mappen som skal inneholde det virtuelle miljøet - dette kan man navngi slik man ønsker, men det er vanligst å kalle det `env` eller `venv` for å vise til at det er et miljø. 

Når mappen med miljøet er opprettet, kan du aktivere miljøet ved å kjøre 
```
source env/Scripts/activate
```
> Kommando over baserer seg på git bash. For mac, kjør `env/bin/activate`. For windows,  kjør `env\Scripts\activate`.

Da kommer det gjerne en tag med miljø-navnet i terminalen som signaliserer at miljøet er aktivt
```
(env)
> ...
```
> Når du er ferdig med å jobbe i miljøet deaktiverer du det ved å kjøre kommandoen `deactivate`

### Pakker
Med miljøet aktivt installerer du pakkene som trengs ved å navigere til rooten av repoet og kjøre kommandoen 
```sh
pip install -r requirements.txt
```
Dette vil lese alle pakkene og de tilhørende versjonene fra requirements-filen. Har dere behov for andre pakker installeres de på vanlig vis ved å kjøre
```sh
pip install <pakkenavn>
```

### Data
Det siste som må på plass for å kjøre notebooken er dataen. Den finner dere på Kaggle, og kan laste ned til maskinen dere jobber på. Når det er gjort, legger dere filene i [/data](./data) for at notebooken skal finne filen.