# ansible-flat-inventory

Print a list of hosts in an Ansible inventory, one per line, followed by all
their groups.

# Example

Given the following inventory:

```
[eastcoast]
a.localdomain.com
c.localdomain.com
e.localdomain.com

[westcoast]
b.localdomain.com
d.localdomain.com
f.localdomain.com

[apache]
a.localdomain.com
b.localdomain.com

[database]
c.localdomain.com
d.localdomain.com

[cache]
e.localdomain.com
f.localdomain.com

[frontend]
a.localdomain.com
b.localdomain.com

[backend]
c.localdomain.com
d.localdomain.com
e.localdomain.com
f.localdomain.com
```

afi prints the following:

```
% afi 
a.localdomain.com apache eastcoast frontend
b.localdomain.com apache frontend westcoast
c.localdomain.com backend database eastcoast
d.localdomain.com backend database westcoast
e.localdomain.com backend cache eastcoast
f.localdomain.com backend cache westcoast
```

afi is useful when working with large, especially dynamically generated,
inventories e.g., from cloud providers like OpenStack, GCP, etc.

# Todo

* Pad the hostnames with whitespace to align and separate the groups.
