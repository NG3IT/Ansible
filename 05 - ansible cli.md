# Ansible cli

---

<br>

## Exemples

```bash
$ ansible -i "<dns or ip>," all -u <user> -m <modul>
# Avec password
$ ansible -i "<dns or ip>," all -u <user> -k -m <modul>

$ ansible -i "machinetest," all -u user -m ping
```

<br>

## Dry run

```bash
# Dry run
$ ansible -i "<dns or ip>," all -u <user> --check --diff -m <modul>
$ ansible -i "<dns or ip>," all -u <user> -C -D -m <modul>
```

---

<br>

## Exemples des modules

```bash
$ ansible -i "<dns or ip>," all -u <user> -m command -a <command>
$ ansible -i "<dns or ip>," all -u <user> -m command -a uptime
$ ansible -i "<dns or ip>," all -u <user> -m command -a ps

$ ansible -i "<dns or ip>," all -u <user> -m shell -a <command>
$ ansible -i "<dns or ip>," all -u <user> -m shell -a "ps -ef | grep nginx"

$ ansible -i "<dns or ip>," all -u <user> -m apt -a <command>
$ ansible -i "<dns or ip>," all -u <user> -m apt -a "name=nginx state=latest"

$ ansible -i "<dns or ip>," all -u <user> -m service -a <command>
$ ansible -i "<dns or ip>," all -u <user> -m service -a "name=nginx state=started"

$ ansible -i "<dns or ip>," all -u <user> -m copy -a <command>
$ ansible -i "<dns or ip>," all -u <user> -m copy -a "src=<file> dest=/tmp/<file>"

# Lister tous les gather facts
$ ansible -i "<dns or ip>," all -u <user> -m setup
# Filter les gather facts
$ ansible -i "<dns or ip>," all -u <user> -m setup -a <command>
$ ansible -i "<dns or ip>," all -u <user> -m setup -a "filter=ansible_distribution*"
```

---

<br>

## Utilisation de Ansible sans Python

```bash
$ ansible -i "<dns or ip>," all -u <user> -d -K -m raw -a <command>
$ ansible -i "<dns or ip>," all -u <user> -d -K -m raw -a "apt install -y python"
```
