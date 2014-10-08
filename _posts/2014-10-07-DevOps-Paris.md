---
title: "[FR] Transformation d'une application"
reveal_theme: serif.css
reveal_transition: linear
---

# Exemple de transformation d'une application

---

## /me

* DevOps (venu de l'Ops)
* Consultant
* Chef/Go

---

## Contexte

--

### But

* Récupération d'évenements
  * Relais
  * Appel malade
  * ...
* Envoi d'alertes
  * SMS
  * Appel

--

IFTTT... Pour le non-communiquant.

--

### Technique

* Front
  * Django
  * Postgresql

* Back
  * Python
  * Daemon

--

### Archi

![Archi]({{ site.baseurl }}/assets/img/2.4.png)

--

### Redistribution

Vente de machines (physiques ou virtuelles)

---

## Outillage

* Git (et rien d'autre)
* Jenkins
* Chef
* Github
* Serveurs dédiés

---

## Compétences

* Ne pas avoir peur du code
* Montrer l'exemple (et connaitre l'exemple)
* Bonne culture

---

## Philosophie

Utilisation des bonnes pratiques du libre.

---

Here we go!

---

## Installation de bout en bout

[Allégorie de la grenouille](http://fr.wikipedia.org/wiki/All%C3%A9gorie_de_la_grenouille)

<p style="text-align: right">
<small>TL;DR Automatisation</small>
</p>

--

* Ecrire les scripts d'installation
* Identification fine des dépendances
* Lever les lièvres
  * Résoudre les problèmes triviaux

--

### Exemples

* Plantage quand dossier de log inaccessible
* Packaging applicatif incomplet (oubli de fichiers)
* Daemonisation barbare
* Besoin d'une entrée dns static (/etc/hosts)
* ~10 fichiers de configuration (/etc)
* Dépendance croisée !!!

--

![Recipes]({{ site.baseurl }}/assets/img/recipes.png)

--

![Cookbook graph]({{ site.baseurl }}/assets/img/graph-cookbook.png)

---

## Création d'environnements de developpement

<p style="text-align: right">
<small>TL;DR Vagrant boxes</small>
</p>

--

* Utilisation des scripts d'installation pour pré-provisinonner une machine
* Ajout de "helper" pour dev

--

### Mise en place

* Mise à disposition d'une `.box`
  * pb -> versionning
    * Pourra être résolu par vagrant cloud
* Repo git "devbox"
* Personnalisation

![devbox]({{ site.baseurl }}/assets/img/devbox.png)

---

## Isolation

<p style="text-align: right">
<small>TL;DR Vendoring</small>
</p>

--

* Utilisation du vendoring
  * bundler
  * virtualenv
  * gom / gopm
  * ...
* Définition fine des dépendances
  * Aïe...

--

```
**-common>=0.3.0-dev,<0.4.0
flufl.enum==4.0.1
ipaddress
locket==0.1.1
# Used by tornado
pycurl>=7.19.0,<7.19.3
pymodbus==1.2
pyserial==2.7
pyst2==0.4
pyudev==0.13
setproctitle==1.0.1
tornado>=3.0,<4.0
sleekxmpp>=1.3,<1.4
netifaces==0.10.4
phonenumbers
ovhapi==2.1
hl7==0.2.5
python-gsmmodem==0.9
sleekdigda==0.2.0
wsgiservice==0.4.0
thecallrapi==0.1.0
uwsgi==2.0.5.1
circus>=0.11,<0.12
```

---

## Définir une interface Dev / Ops

<p style="text-align: right">
<small>TL;DR Repo tout en 1</small>
</p>

--

### Installation

Utilisation d'un outil de lancement de taches : `make`, `invoke`, `rake`...

Exemple : `make prod`, `make dev`

--

### Test/Ci

Utilisation d'un fichier de formalisation : `.travis.ci`, `.ci.yml`

<small>ou de l'outil de lancement de taches</small>

--

### Packaging

Integration du packaging dans le repo du logiciel

---

## Modifications logiciel

<p style="text-align: right">
<small>TL;DR Kill it with fire</small>
</p>

--

### Simplification des configurations

* Options en ligne de commande

* Syslog

* Ident Pg

* Surcharge par variables d'environnement

--

### Architecture produit

Utilisation de bibliothèques partagées pour casser la dépendance croisée.

--

### SOI

Communication via API Rest

--

### Composants standards

* Réutilisation de composants depuis la "forge"
* Ouverture de composants

--

### Versionning

`semver` everywhere

--

### Supprimer l'adhérance système

Délégation des taches à des agents dédiés

Exemple : `tentacool`

--

### Resultat

![3.0]({{ site.baseurl }}/assets/img/3.0.png)

--

### Futur

![3.0+]({{ site.baseurl }}/assets/img/3.0+.png)

---

## Adapter les outils

<p style="text-align: right">
<small>TL;DR Rendre votre workflows "upstream"</small>
</p>

--

### Gestion de conf

* Dependances
* Modules

--

### Création d'environements

Pipeline de création

--

### Packaging

* Travail sur les "helpers" (`dh_virtualenv`)
* Gestion des dépots

--

### CI

* Automatisation via plugins

---

Efficacité ?

---

Question ?
