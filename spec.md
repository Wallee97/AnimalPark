# Specifikation

## Inledning
Jag tänker skriva ett program som håller reda på djur i en djurpark. Djuren ska tilldelas namn, ålder, art och kön med vilka de senare ska kunna sorteras och sökas efter.
Programmet ska även kunna ge rekommendationer på vilka djur som ska köpas/ säljas baserat på befintliga djur i djurparken.
Utmaningen med programmet är att få det lättöverskådligt. 

## Användarscenarier

### Inventering av djur
Peter äger en djurpark med 173 st djur av olika art och alla med unika namn. En dag skaffar han en koala. För att hålla koll på alla djuren har han matat in alla djurens information i programmet. Peter startar han upp programmet och går in på "Lägg till djur".
Därefter matar han in koalans kön, ålder, namn och art. Informationen sparas och han hittar sedan informationen i undermenyn "befintliga djur".

### Rekommendationer vid försäljning
Peter bestämmer sig för att minska på antalet djur i parken. 
Genom att gå in i programmet och klicka på alternativet "rekommendationer" och sedan "ta bort djur" får han en lista där han ser att det finns 7 kvinnliga björnar och endast 2 manliga. 
För att jämna ut förhållandet väljer han att sälja hälften av de kvinnliga björnarna.

# Kodskelett

```
class animal(object):
	"""Skapar ett objekt per djur och tilldelar parametrarna ålder, kön, namn, art"""
	possibleAnimals="arter som är möjliga att lägga till, läses in från extern fil (arter.txt)"
	
	listAnimals="lista med alla djuren i form av objekt"
	
def mainMenu(lsSpecies, lsAnimals):
		"""Huvudmenyn, ska innehålla alternativen lägg till djur, ta bort djur, visa översikt, rekommendationer"""

def overview(lsAnimals):
	"""returnerar alla djuren med dess information""""


def recommendationMenu(lsAnimals):
		"""2 alternativ, som rekommenderar vilka/vilket djur som ska tas bort/ läggas till."""
	
def sortAnimals(type):
		"""4 alternativ: art, namn, kön och ålder. Sorterar djuren beroende vad (type) är, t.ex. art. Returnerar en sorterad version av listan"""
		
def addAnimal(lsAnimals, lsSpecies):
		"""lägger till ett djur i listan, kan endast välja arter som finns i listan lsSpecies. Ålder, kön och namn tilldelas med hjälp av inmatning från användaren.
		Namnet jämförs med övriga namn för att avgöra om det är unikt. Ska även finnas ett maxtak fför antalet djur"""
		
def removeAnimal(lsAnimals):
	"""Tar bort ett valt djur från lsAnimals. Användaren blir presenterad samma lista som i översikt"""
	
def search(lsAnimals, userInput):
		"""returnerar objekt från lsAnimals som innehåller userInput"""
		
	
```

# Programflöde
När programmet startas, läses information om vilka djur som finns och vilka arter som är tillåtna som inmatning från två separata filer. 
Användaren kan därefter välja mellan flera olika alternativ som tar användaren till olika undermenyer. Alternativen är: ta bort/ lägga till djur, översikt, rekommendationer, och avsluta. 
När användaren väljer att lägga till/ ta bort djur kommer metoden addAnimal alternativt removeAnimal utföras på det objekt som specificeras av användaren. 
Alternativet sort animals utför metoden sortAnimals på listan listAnimals beroende på värdet på type. 

