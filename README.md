netpd2
======

development setup
------

  netpd2/
  netpd2-patches/
 
- cd netpd2
- git checkout develop
- mv abs/.gitignore ../netpd2-patches/abs/.gitignore
- mv patches/.gitignore ../netpd2-patches/patches/.gitignore
- rm abs
- rm patches
- ln -s ../netpd2-patches/abs
- ln -s ../netpd2-patches/patches

