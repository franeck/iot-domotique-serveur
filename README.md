# Projet IOT Alarme - Serveur

## Spécifications de l'api :
> Pour communiquer avec la base

POST /alarm

```text
  Token : token
```
  
```json
  { 
    "state": Boolean,
    "reason": String
  }
```

## Déscription 

Le serveur reçoit la commande d'armer l'alarme. Si dans les 15 secondes qui suivent il ne reçoit pas de commande de désarmement il actve l'alarme. Sinon il le désactive. En plus il dispose d'un motif à afficher à l'utilisateur ( intrusion, capteur offline )

Le serveur expose un endpoint pour connaître l'état de l'alarme ( off, armed, on ) - afin d'afficher dans l'applie / sur le site.

Le serveur peut envoyer des notifications push vers des appareils souscrits pour les notifications d'alarme

Le serveur expose une api permettant de connaître l'état des capreurs. Pour le déterminer il fait des appels à la station base.
