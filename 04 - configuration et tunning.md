# Fichiers de configuration

---

<br>

## Hiérarchie de configuration 

Fichier de configuration Ansible -> ansible.cfg

```bash
# 1. Variable
$ export ANSIBLE_CONFIG=<file>

# 2. ansible.cfg à l'endroit où se situe le playbook

# 3. ~/.ansible/ansible.cfg

# 4. /etc/ansible/ansible.cfg
```

---

<br>

## Commandes

```bash
# Voir le fichier de config prit en compte
$ ansible-config view 

# Voir les variables et leurs valeurs
$ ansible-config list
```

---

<br>

## Misc

```bash
# Dans le fichier ansible.cfg prit en compte

# Désactiver le fingreprint
[defaults]
host_key_checking = False

# Avoir le temps d'exécution par action
[defaults]
callback_whitelist = profile_tasks

# Permet d'exécuter via le stdin pour l'exécution via ssh (à l'inverse du comportement par défaut)
[ssh_connection]
pipelining = True

# Augmenter la persistence de la connexion
[ssh_connection]
ssh_args = -o ControlMaster=auto -o ControlPersist=60s

# Spécifier une méthode d'authentification
[ssh_connection]
ssh_args = -o ControlMaster=auto -o ControlPersist=60s -p PreferredAuthentications=publickey

# Forks
[defaults]
forks = 20

# Pas de récupération des gather facts
gather_facts: no

# Cache de gather facts (exemple : valide pendant 1 heure)
fact_caching = jsonfile
fact_caching_timeout = 3600
fact_caching_connection = /tmp/mycachedir

# Cache de gather facts avec une base redis
fact_caching = redis
fact_caching_timeout = 3600
fact_caching_connection = localhost:6379:0
```
