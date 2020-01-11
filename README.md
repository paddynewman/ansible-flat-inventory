# ansible-flat-inventory

Print a list of hosts in an Ansible inventory, one per line, followed by all
their groups.

# Example

Give the inventory that's defined in the "inventory" directory, which is
configured in the ansible.cfg file, aft prints the following:

```
% afi 
a.localdomain.com apache eastcoast frontend
b.localdomain.com apache frontend westcoast
c.localdomain.com backend database eastcoast
d.localdomain.com backend database westcoast
e.localdomain.com backend cache eastcoast
f.localdomain.com backend cache westcoast
```

# Todo

* Add support for a "-i/--inventory" command line argument.
