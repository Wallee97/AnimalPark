# Specifikation

## Inledning
Jag t�nker skriva ett program som h�ller reda p� djur i en djurpark. Djuren ska tilldelas namn, �lder, art och k�n med vilka de senare ska kunna sorteras och s�kas efter.
Programmet ska �ven kunna ge rekommendationer p� vilka djur som ska k�pas/ s�ljas baserat p� befintliga djur i djurparken.
Utmaningen med programmet �r att f� det l�tt�versk�dligt. 

## Anv�ndarscenarier

### Inventering av djur
Peter �ger en djurpark med 173 st djur av olika art och alla med unika namn. En dag skaffar han en koala. F�r att h�lla koll p� alla djuren har han matat in alla djurens information i programmet. Peter startar han upp programmet och g�r in p� "L�gg till djur".
D�refter matar han in koalans k�n, �lder, namn och art. Informationen sparas och han hittar sedan informationen i undermenyn "befintliga djur".

### Rekommendationer vid f�rs�ljning
Peter best�mmer sig f�r att minska p� antalet djur i parken. 
Genom att g� in i programmet och klicka p� alternativet "rekommendationer" och sedan "ta bort djur" f�r han en lista d�r han ser att det finns 7 kvinnliga bj�rnar och endast 2 manliga. 
F�r att j�mna ut f�rh�llandet v�ljer han att s�lja h�lften av de kvinnliga bj�rnarna.

# Kodskelett

```
class animal(object):
	"""Skapar ett objekt per djur och tilldelar parametrarna �lder, k�n, namn, art"""
	possibleAnimals="arter som �r m�jliga att l�gga till, l�ses in fr�n extern fil (arter.txt)"
	
	listAnimals="lista med alla djuren i form av objekt"
	
def mainMenu(lsSpecies, lsAnimals):
		"""Huvudmenyn, ska inneh�lla alternativen l�gg till djur, ta bort djur, visa �versikt, rekommendationer"""

def overview(lsAnimals):
	"""returnerar alla djuren med dess information""""


def recommendationMenu(lsAnimals):
		"""2 alternativ, som rekommenderar vilka/vilket djur som ska tas bort/ l�ggas till."""
	
def sortAnimals(type):
		"""4 alternativ: art, namn, k�n och �lder. Sorterar djuren beroende vad (type) �r, t.ex. art. Returnerar en sorterad version av listan"""
		
def addAnimal(lsAnimals, lsSpecies):
		"""l�gger till ett djur i listan, kan endast v�lja arter som finns i listan lsSpecies. �lder, k�n och namn tilldelas med hj�lp av inmatning fr�n anv�ndaren.
		Namnet j�mf�rs med �vriga namn f�r att avg�ra om det �r unikt. Ska �ven finnas ett maxtak ff�r antalet djur"""
		
def removeAnimal(lsAnimals):
	"""Tar bort ett valt djur fr�n lsAnimals. Anv�ndaren blir presenterad samma lista som i �versikt"""
	
def search(lsAnimals, userInput):
		"""returnerar objekt fr�n lsAnimals som inneh�ller userInput"""
		
	
```

# Programfl�de
N�r programmet startas, l�ses information om vilka djur som finns och vilka arter som �r till�tna som inmatning fr�n tv� separata filer. 
Anv�ndaren kan d�refter v�lja mellan flera olika alternativ som tar anv�ndaren till olika undermenyer. Alternativen �r: ta bort/ l�gga till djur, �versikt, rekommendationer, och avsluta. 
N�r anv�ndaren v�ljer att l�gga till/ ta bort djur kommer metoden addAnimal alternativt removeAnimal utf�ras p� det objekt som specificeras av anv�ndaren. 
Alternativet sort animals utf�r metoden sortAnimals p� listan listAnimals beroende p� v�rdet p� type. 

