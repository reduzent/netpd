
netpd
=====

is a CRNMME (Collaborative Realtime Networked Music Making Environment)
written in Pure Data. It allows many users to have a realtime jam
sessions with each other, connected over the net.
Users might contribute their own netpd-ized patches a.k.a. instruments
or use pre-existing ones. The set of patches, as well as the state of
each is synchronized between clients in order to provide identical
experience for every connected user.

  Read more:
  http://www.netpd.org

NOTE: This repository|archive contains only the netpd framework. The
netpd-instruments are hosted separately on:

  https://github.com/reduzent/netpd-instruments

You may want to clone all at once by doing:

  git clone --recursive https://github.com/reduzent/netpd.git


prerequisites
=============

You need to have Pure Data (>= 0.45) installed. The following Pd
externals are needed, too. You can install them through the Pd menu
'Help' -> 'Find externals':

  * binfile
  * ggee
  * iemnet
  * iemlib
  * readdir
  * osc
  * slip
  * zexy

NOTE: pd-l2ork is not supported (and support is not planned) because it
      has some incompatibilities with Pure Data.

NOTE: Support for Pd-extended is going to fade out slowly as netpd is going
      to use new features of Pure Data.


intro
=====

* Open netpd/main.pd with Pd
  chat automatically connects to the server and you can
  now talk to other users.
  Click 'list' to get a list of currently connnected users.

* Click the 'unpatch' button in chat to launch the unpatch instru-
  ment manager. If there is already a session going on, the instru-
  ments used in the ongoing session are automatically loaded (they
  are first downloaded from other users, if necessary).

* Load instruments with unpatch by clicking the square button next
  to the 'netload instrument' label. Browse to netpd/instruments and pick
  an instrument (if your netpd/instruments directory is empty, you need
  to get some instruments first. Read above).
  Alternatively, just type the name of the instrument (without the
  extension .pd) into the symbol box and hit enter.

* Play an instrument by clicking its name in unpatch. The instru-
  ment's GUI pops up and you can now manipulate the instrument
  at your will. Beware other users are able (and supposed) to
  manipulate the instrument to their will as well.

* Create your own instrument by typing '/new mysupersynth' into
  unpatch's symbol box. A new instrument named 'mysupersynth'
  shows up in unpatch's instrument list. Edit mysupersynth.pd and
  save it. You might want to check existing instruments to get an
  idea of how to cook your own instrument. There will be section
  about this topic on http://www.netpd.org/docs .
  NOTE: instruments belong to netpd/instruments, their abstractions to
  netpd/instruments/abs.


copyright
=========

2008-2015, Roman Haefeli <roman@netpd.org>
Published under the Gnu Public License (GPL-2)


releases
========

2.1
  * Improved reliability of finding a sync peer (breaks
    compatibility with v2.0)
  * Added non-blocking until [netpd-nb-until]
  * Turning DSP off on dynamic creation is now a
    configurable option (see chat's preferences)
  * Prevent errors when checking for non-existing files
    (adds more dependencies, though)
  * Automatically load unpatch by cmdline option (useful
    for -nogui)
  * Turn on/off printing of all incoming and outgoing OSC
    message with cmdline option
  * Turn on/off state messages for testing and debugging
    with cmdline option

2.0
  * Complete rewrite
  * Messaging layer based on OSC
  * Consequent use of namespaces
  * Improved and more reliable state synchronization
  * Faster patch synchronization
  * More intelligent dependency resolving
  * Multiple instances of the same instrument
  * Non-blocking network layer (less audio drop-outs)
  * Lots of bugfixes

