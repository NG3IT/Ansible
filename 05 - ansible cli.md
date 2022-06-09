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
