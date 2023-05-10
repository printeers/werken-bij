# Printeers coding challenge

Bij Printeers werken we met een microservices-gebaseerde architectuur. Omdat het neerzetten van een volledige stack nogal veel overhead geeft, voeren we met deze challenge een kleine simulatie uit. Het doel van deze challenge is om een indruk te krijgen van de skills en ook als praatstuk voor het technisch interview. Uiteraard verwachten we geen production-ready service met alle toeters en bellen. Besteed maximaal 4 uur aan deze challenge.

Wat is de opdracht?

- Een simpele `order-api` moet 'create order' requests accepteren en de orders opslaan in een postgres database.
- Een bot (`bot-client`) speelt een fictieve klant die iedere seconde één order plaatst bij de `order-api`.

Je mag zelf verzinnen welke velden je meeneemt in de order data. Het hoeft niet compleet noch realistisch te zijn, maar er moet wel minstens in zitten:

- Support voor meerdere orderregels.
- Per orderregel een afbeelding, die de fictieve klant wil laten printen op een telefooncase.
- Een unieke identifier vanuit de klant, die hooguit één keer gebruikt mag worden voor het maken van een order.
- Het adres waarnaar de order verstuurd mag worden.

De `order-api` moet teruggeven aan de client:

- Een unieke identifier voor de order.
- De verwachte tijd dat de order compleet is. Verzin zelf een fictieve tijdsduur voor het printen en verzenden van een order vanaf het moment dat de order geplaatst wordt.

Als boilerplate vind je een docker-compose setup die alle componenten draait.

Je mag zelf kiezen welke API tech je gebruikt voor de challenge, bijvoorbeeld http/json of gRPC.

Alle files in deze directory mogen aangepast.

## Boilerplate starten

Om de setup te starten, run:

```bash
docker-compose up
```

Om de database opnieuw te initialiseren, exit uit docker-compose up proces zodat de containers stoppen, en draai:

```bash
docker-compose rm
```
om de containers te deleten.

Daarna opnieuw `docker-compose up` om op te starten.


