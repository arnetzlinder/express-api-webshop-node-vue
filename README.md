# Nedan följer instruktionerna för uppgiften som vi fick i skolan. 

------------------------------------------------------------------------------------------------------------------------------
Målet var att skapa en webbshop med backend och frontend för betyget VG. Jag skapade en webbshop som säljer färdigsydda kläder. Fronten är byggt i VUE.

Du har fått i uppdrag att utveckla API’et till en webbshop.

En lösningsarkitekt har redan dokumenterat vilka endpoints som skall finnas för API’et samt skrivit ett test flöde med REST-Client som ni kan börja utveckal med. Dvs vilka endpoints och vad de skall heta samt vad de förväntas returnera är redan förutbestämt. 

För att testerna skall fungera behöver ni Rest-Client (extension) installerat till vsc.

För G krav så räcker det att de endpoints markerade med G fungerar. 

För VG behöver även de endpoints markerade med VG fungera. För VG så skall även en frontend klient för projektet skapas där minst endpointsen för G kraven används (se nedan för en lista av vilka krav som specifieras för klienten). 
Dvs, för betyget G behöver ingen frontend skapas.

Projektet ni klonar har förutom test-rest filerna förberett även en mapp för backend, där ni kan installera express på valfritt sätt. Samt en mapp för frontend där ni kan skapa er frontend klient på valfritt sätt. 

All data skall sparas i en lokal MongoDB databas. Döp databasen enligt “fornamn-efternamn”.

Det är helt ok att skapa alla produkter med “mock” data, samt att för designens skull använda en “placeholder”-bild för produkterna, dvs att alla produkter har samma bild.


### Skillnader mellan G och VG krav:

För kravet G så behöver inte anänvdarens lösenord krypteras. 

För VG så behöver användarens lösenord i endpointen krypteras innan det sparas i databasen. Samt så skall alla administratörs endpoints skyddas med en API nyckel, dvs om inte rätt nyckel skickas med i POST body, eller som param i GET, så skall inte anropet hanteras av servern utan istället svara med en statuskod 401 (unauthorized) och lämna ett passande medelande ({“message”: “Not Authorized”). 


