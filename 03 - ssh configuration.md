# SSH Configuration 

---

<br>

## Generer une paire de clé SSH

```bash
$ ssh-keygen -t ecdsa -b 521
```

---

<br>
    
## Déployer la clé publique

```bash
$ ssh-copy-id <user>@<machine_distante>:<path>
```
  
--- 
  
<br>
  
## Renforcer la sécurité 
  
Rajouter au début de la clé

```bash
from="<ip>"  
```

---

<br>

## Agent SSH

```bash
# Lister la ou les clés embarquées
$ ssh-add -l

# Ajouter une clé à l'agent SSH
$ eval `ssh-agent`
$ ssh-add
$ ssh-add -l
```

---

<br>

## Test de la connection au managed node

```bash
$ ansible -i "<hostname-node>," all -m ping
```
