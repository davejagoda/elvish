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
latex one_ring_inscription.tex
xdvi one_ring_inscription.dvi
pdflatex one_ring_inscription.tex
```
