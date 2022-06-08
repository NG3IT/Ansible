# Installation 

---

<br>

## Installation (pip)

```bash
$ sudo apt install -y python3-pip
$ pip3 install ansible
# Specify version 
$ pip3 install ansible==<version>
```

<br>

## Python interpreter

```bash
# Sur le managed node
$ ansible_python_interpreter=/usr/bin/python3
```

```bash
# Installation de python à distance
$ ansible myhost --besome -m raw -a "yum install python3"
```

