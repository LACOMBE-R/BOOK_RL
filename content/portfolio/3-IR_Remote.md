+++
draft = false
image = "img/portfolio/IR_REMOTE/Icon.png"
date = "2016-11-05T18:25:22+05:30"
title = "Télécommande IOT"
weight = 1
+++

Faire entrer un ampli vieillissant dans le 21ème siècle en créant une télécommande infrarouge connectée.
<!--more-->

---

## Présentation

Après avoir recupéré un ampli de la marque Onkyo, j'ai eu l'idée de concevoir un dispositif permettant de le connecter avec mon **système domotique DIY** (**[Home Assistant](https://www.home-assistant.io)**).  
Dans l'idée, je souhaitais pouvoir contrôler mon ampli grâce a des **commandes vocales Google Home**, comme :

>***"Hey google, allume l'ampli"***  
>***"OK google, augmente le volume de l'ampli"***  
>***"Hey google, bascule l'entrée de l'ampli sur mon PC"***  

Pour cela, j'ai entamé une importante phase de **recherche** : La seule manière de contrôler l'ampli à distance est une **télécommande**, que je ne souhaitais pas acheter (beaucoup plus sympa de construire la mienne !). J'ai déterminé qu'il était possible de **simuler une télécommande** en utilisant une simple **LED infrarouge** connectée à un **micro-contrôleur** (ici un ESP-01).  

Il a ensuite fallu déterminer les codes à émettre pour chacune des touches dont j'avais besoin. Je m'en suis sorti grâce à la vaste librairie d'un **projet open-source** visant à recenser tout les codes infrarouges de commande en fonction des constructeurs (**[LIRC](https://www.lirc.org)**).  

La dernière pièce du puzzle est de connecter mon ESP-01 à mon centre de contrôle domotique. C'est encore une fois l'open source qui me sauve ! Le projet **[Tasmota](https://tasmota.github.io/docs/)** est un firmware modulaire et très facile d'installation conçu pour la domotique. Il possède, de plus, un module dédié au contrôle d'une **LED infrarouge**, ainsi qu'une passerelle simplifiée avec **Home Assistant**.

---

Après prototypage, j'ai souhaité aller plus loin en m'essayant au **fraisage de PCB** (circuit imprimé).
Une fois mon schéma électronique
