elvish
======

On the host
-----------

```
vagrant up
DISPLAY=:0 vagrant ssh -- -X
```

On the guest
------------

```
cd /vagrant/
latex elvish_test.tex
xdvi elvish_test.dvi
```
