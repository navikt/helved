# Satstyper

## ENG
Q: Hvis man ikke har dagsats, 
    kan vi alltid sende perioden som ENG med totalbeløpet?
```
 ╭───────────────╮  
 │ 1.feb - 4.feb │
 ╰───────────────╯  
```

## DAG7
Q: Kan vi alltid bruke dag7 og be konsumentene ekskludere helg/helligdag ved behov?
Q: Kan vi anta at en ENG-utbetaling for en periode på 1 dag, er av satstype DAG7?
```
 ╭───────╮   ╭───────╮   ╭───────╮   ╭───────╮  
 │ 1.feb │<──│ 2.feb │<──│ 3.feb │<──│ 4.feb │
 ╰───────╯   ╰───────╯   ╰───────╯   ╰───────╯  
```

## MND
Q: Kan vi alltid si at en periode på én mnd ikke kan være ENG?
```
 ╭────────────────╮  
 │ 1.feb - 28.feb │
 ╰────────────────╯  
```

# Forkorte siste periode
```
 ╭───────╮   ╭───────╮   ╭───────╮   ╭───────╮  
 │ 1.feb │<──│ 2.feb │<──│ 3.feb │<──│ 4.feb │
 ╰───────╯   ╰───────╯   ╰───────╯   ╰───────╯  
     ^  
     │ refDelytelseId
     │
 ╭───────╮   ╭───────╮   ╭───────╮  
 │ 1.feb │<──│ 2.feb │<──│ 3.feb │
 ╰───────╯   ╰───────╯   ╰───────╯  
```

# Forkorte begge ender
Q: Ved forkortelse i midten/starten, kan vi alltid referere til den første delytelsen?
    Eller må vi referere til delytelseId for 2.feb?
    Eller må vi opphøre 1.feb og referere til delytelseId for 4.feb?
    Tanken er her at vi ønsker å skrive over hele kjeden, 
    og at man i utgangspunktet har 1 kjede per behandling

## Alternativ 1 = korreksjon
```
 ╭───────╮   ╭───────╮   ╭───────╮   ╭───────╮  
 │ 1.feb │<──│ 2.feb │<──│ 3.feb │<──│ 4.feb │
 ╰───────╯   ╰───────╯   ╰───────╯   ╰───────╯  
     ^  
     │ refDelytelseId
     │
     │       ╭───────╮   ╭───────╮
     ╰───────│ 2.feb │<──│ 3.feb │
             ╰───────╯   ╰───────╯
```

## Alternativ 2 = opphør
```
 ╭───────╮   ╭───────╮   ╭───────╮   ╭───────╮  
 │ 1.feb │<──│ 2.feb │<──│ 3.feb │<──│ 4.feb │
 ╰───────╯   ╰───────╯   ╰───────╯   ╰───────╯  
                                         ^       
                          refDelytelseId │
                                         │ opphør fom 1.feb
                                     ╭───────╮   ╭───────╮   ╭───────╮
                                     │ 4.feb │<──│ 2.feb │<──│ 3.feb │
                                     ╰───────╯   ╰───────╯   ╰───────╯
```

# Funksjonell beskrivelse av type endringer
OPPRETTE    ny informasjon, historien er gyldig
KORRIGERE   endre infromasjon, historien var feil
ANNULLERE   fjerne historie, den skulle aldri vært
OPPHØRE     informasjonen er gyldig tom nå.

