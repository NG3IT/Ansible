# Definitions

---

## Inventaire 

<br>

## Control node

This is the central machine for Ansible. This machine is a centralyzed node for repo, secret. Use the control node for deploy.
 
<br>

## Managed nodes

Ce sont les serveurs cibles. Il est nécessaire de pouvoir se connecter en SSH avec un utilisateur qui a la possibilité de faire une élévation de privilège.

<br>

## Inventory

C'est l'inventaire des machines (ip, dns), des variables (host_vars, group_vars). Ces fichiers sont au format plat ou yaml.

L'inventaire peut être statique (fichiers) ou dynamique (script).

Il y a également la possibilité d'utiliser des patterns (srv-linux[0-10])

<br>

## Groupes

Cela permet de regrouper des machines au niveau de l'inventaire machine. 

Il y a la possibilitté de créer différents niveaux hiérarchique (parents/enfants).

Le groupe racine est : all

<br>

## Groups Vars

Il s'agit d'un répertoire spécifique ou d'un fichier (fichier central d'inventory) dans lequel les variables de groupes vont être stockées.

<br>

## Host Vars

Il s'agit d'une variable spécifique à une machine.

Cette variable surcharge d'autres variables définies plus haut (comme les Groups Vars).

<br>

## Exemple d'inventory

```bash
inventory.yml
host_vars/
group_vars/
```

<br>

---

## Actions

<br>

## Tasks

Fichier yaml dans lequel on retrouve diverses actions (user, group, command, module).

<br>

## Modules

Un module est composée d'un ensemble d'actions regroupé autour d'un thème (outils spécifiques par exemple).

Chacune de ces actions est utilisable via une task.

<br>

## Rôles

C'est un ensemble d'actions pour réaliser un ensemble cohérent (installer nginx par exemple).

<br>

## Playbooks

Il s'agit d'un fichier qui va appliquer des rôles à un inventaire.

inventory -> playbook <- rôles

<br>

## Plugins

Permet d'augmenter les capacités d'Ansible (output, inventory dynmaqieu, tests, ...)





