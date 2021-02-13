
# netpd

![netpd in action](https://www.netpd.org/netpd-in-action.png "netpd in action")

is a CRNMME (Collaborative Realtime Networked Music Making Environment)
written in Pure Data. It allows many users to have a realtime jam
sessions with each other, connected over the internet.
Users might contribute their own netpd-ized patches a.k.a. instruments
or use pre-existing ones. The set of instruments and the state of
each one is synchronized between clients in order to provide identical
experience for every connected user.

  * Find more detailed information on  
    https://netpd.org
    
  * Discuss related matters on  
    https://untalk.netpd.org

**NOTE**:  
This repository contains only the netpd framework. The
netpd-instruments are hosted separately on:  
https://github.com/reduzent/netpd-instruments

You may want to clone everything at once by doing:

```
git clone --recursive https://github.com/reduzent/netpd.git
```

## supported platforms

netpd runs on any platform [Pure Data](https://puredata.info) runs on. This includes **Linux**, **macOS**,
**Windows**.

## prerequisites

Before runnning netpd you need to install [Pure Data](https://puredata.info) (Pd) (>= 0.51.0) from
[here](http://msp.ucsd.edu/software.html). You also need to install a few additional libraries.
They can be installed from Pd through the menu *Help* -> *Find externals*. Search for their names
and click on the appropriate choice. Be careful to pick the one with the right name, if several
similarly named choices are presented:

  * binfile
  * else
  * iemnet
  * iemlib
  * osc
  * slip
  * zexy

**NOTE**: pd-l2ork is not supported (and support is not planned) because it
 has some incompatibilities with Pure Data.

## intro

* Open `netpd/main.pd` with Pd.  
  chat automatically connects to the server and you can
  now talk to other users.  
  Click *list* to get a list of currently connnected users.

* Click the *unpatch* button in chat to launch the unpatch instrument
  manager. If there is already a session going on, the instru-
  ments used in the ongoing session are automatically loaded (they
  are first downloaded from other users, if necessary).

* Load instruments with unpatch by clicking the square button next
  to the *netload instrument* label. Browse to `netpd/instruments` and pick
  an instrument (if your netpd/instruments directory is empty, you need
  to get some instruments first. Read above).
  Alternatively, just type the name of the instrument (without the
  extension .pd) into the symbol box and hit enter.

* Play an instrument by clicking its name in unpatch. The instru-
  ment's GUI pops up and you can now manipulate the instrument
  at your will. Beware other users are able (and supposed) to
  manipulate the instrument to their will as well.

* Create your own instrument by typing `/new mysupersynth` into
  unpatch's symbol box. A new instrument named *mysupersynth*
  shows up in unpatch's instrument list. Edit *mysupersynth.pd* and
  save it. You might want to check existing instruments to get an
  idea of how to cook your own instrument. There will be section
  about this topic on https://netpd.org/docs .  
  **NOTE**: instruments belong to `netpd/instruments`, their abstractions to
  `netpd/instruments/abs`.
 
## server

For online jams, netpd needs to connect to a netpd-server. A public netpd-server
is running at **netpd.org** on port **3025**. This is the default server in
netpd's configuration. The netpd-server software is available here:  
https://github.com/reduzent/netpd-server. 


## copyright

2008-2021, Roman Haefeli <roman@netpd.org>  
Published under the GNU Public License (GPL-2)

