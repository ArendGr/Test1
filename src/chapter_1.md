# Chapter 1

```plantuml
@startuml

# Verkeerslicht Diagram
stateDiagram-v2
    [*] --> RoodR
    RoodR --> GroenR : AutoR aankomt
    GroenR --> GeelR : Timer eindigt
    GeelR --> RoodR : Timer eindigt

    [*] --> RoodL
    RoodL --> GroenL : AutoL aankomt
    GroenL --> GeelL : Timer eindigt
    GeelL --> RoodL : Timer eindigt

    # Stoplichtsysteem

Dit is de visualisatie van het stoplichtsysteem.

## Werking

Het stoplichtsysteem bestaat uit twee richtingen, Rechts (R) en Links (L). Elke richting heeft een stoplicht met de kleuren: Rood, Geel, Groen. 
De status van het stoplicht verandert afhankelijk van de aanwezigheid van een auto, en de tijd die het licht op elke status aanblijft.

- **Rood**: Stoplicht is rood
- **Groen**: Stoplicht is groen
- **Geel**: Stoplicht is geel
Redelijk vanzelfsprekend

Elke status heeft zijn eigen tijdsinstellingen:
- **Rood**: 5 seconden
- **Geel**: 2 seconden
- **Groen**: 5 seconden

### Voorbeeld van het Stoplichtsysteem

Als er een auto aankomt, Dan kan het stoplicht op groen gaan springen. Nu doet het stoplicht mee aan de cyclus.

1. **Auto van Rechts**:
   - Rood → Groen → Geel → Rood
2. **Auto van Links**:
   - Rood → Groen → Geel → Rood

@enduml
```