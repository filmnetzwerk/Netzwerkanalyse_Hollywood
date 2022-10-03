# Inhalt
1.Edgeslist.csv

2.Nodelist.csv

3.Codebuch.md (Codierung der Datensätze)

# Ursprung und Datenerhebung
Wir wollen uns mit den 20 erfolgreichsten Filmen im Zeitraum von 2000 bis 2020 beschäftigen. Dabei sollen die Filme aus zwei Blickwinkel untersucht werden: Was sind die 20 Filme mit den weltweit meisten Box-Office Einnahmen in diesem Zeitraum? Was sind die 20 besten Filme aus der Sicht der Filmkritiker? Gibt es Filme, Regisseur:innen, Produzent:innen, Schauspieler:innen, Drehbuchautor:innen, Filmstudios, die in beiden Netzwerken zu finden sind? Gibt es mehrfache Nennungen innerhalb des Netzwerks? Gibt es “allround” Talente? 
Die Daten zu den Box-Office Einnahmen entnehmen wir aus der folgenden Seite: https://www.boxofficemojo.com/chart/top_lifetime_gross/?area=XWW.
Die Daten zu den von der internationalen Presse als am besten bewertete Filme entnehmen wir von der folgenden Seite: https://www.filmstarts.de/kritiken/besten/filme/pressewertung/.
Zusätzliche Informationen über beteiligte Akteure erheben bzw. prüfen wir über https://www.imdb.com/.

## 1) Edge-Attribute
id: numerische Codierung für jeden Knoten des Netzwerks 
from: initiierender Knoten, in diesem Fall: Film mit Verbindung zu allen Mitwirkenden.

to: erhaltender Knoten, in diesem Fall: mitwirkende Personen, wie beispielsweise die Schauspieler:innen, Produzent:innen etc. 

weight: Rankingplazierung aufgrund des Kritiker-Rankings bzw. der Box Office Einnahmen
20 = beste Platzierung (erste Nennung in den Rankings),
1 = schlechteste Plazierung (letzte Nennung in den Rankings)

## Node-Attribute

### id:	
Eindeutige Benennung nach Buchstabenkürzel aus Vor- und Nachname plus Kürzel nach jeweiliger Funktion, bei Filmen Kennzeichnung durch eindeutiges Schlagwort des Titels. 
### name:
Vor- und Nachname des Akteur:innen, Titel des Films, Name der Produktions- bzw. der Distributionsfirma. 
### type:	
movie
director
producer
screenplay
actor 
composer
production_company
distribution_company 
### sex:
0 = non-binary
1 = male
2 = female
3 = movie, production_company, distribution_company
### ranking_money:	
Rankingplatz nach Box-Office Einnahmen
### ranking_critics:	
Rankingplatz in den Filmkritiken
### year:	
Erscheinungsjahr Film
### director:
Regisseur:innen. Codiert nach erstem Buchstaben von Vor- und Nachname plus “d”.
### producer:	
Produzent:innen. Codiert nach erstem Buchstabe von Vor- und Nachname plus “p”.
### screenplay:	
Drehbuchautor:innen. Codiert nach erstem Buchstabe Vor- und Nachname plus “s”.
### actor1 - actor3:	
Hauptdarsteller:innen. Codiert nach erstem Buchstabe Vor- und Nachname plus “a”.
### composer:	
Komponist:innen. Codiert nach erstem Buchstabe Vor- und Nachname plus “c”.
### production_company1 - production_company4: 
Produktionsfirmen. Codiert nach Anfangsbuchstaben plus "pc".
### distribution_company:
Vertriebsgesellschaft. Codiert nach Anfangsbuchstaben plus "dc".
### box_office:	
Box-Office-Einnahmen in Milliarden US-Dollar, auf drei Dezimalstellen gerundet. 
### oscar:	
Anzahl gewonnener Oscars in Zahlen.
### golden_globe:	
Anzahl gewonnener Golden Globes in Zahlen.
### genre
Einordnung des Films in das entsprechende Genre. 
### country:
Herkunftsland der Akteur:innen oder Produktionsfirmen bzw. Vertriebsgesellschaft. Codiert nach offiziellen zweistelligen Länderkürzeln. 
