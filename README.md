
![netpd](https://www.netpd.org/netpd-logo.png "netpd")


is a CRNMME (**C**ollaborative **R**ealtime **N**etworked **M**usic **M**aking **E**nvironment)
written in Pure Data. It allows many users to have a real time jam
sessions with each other, connected over the internet.
Users might contribute their own *netpd*ized patches a.k.a. instruments
or use pre-existing ones. The set of [instruments](https://www.netpd.org/Instruments) and the state of
each one is synchronized between clients in order to provide identical
experience for every connected user.

  * Find more detailed information on  
    https://netpd.org
    
  * Discuss related matters on  
    https://untalk.netpd.org

**NOTE**:  
This repository contains only the netpd framework. The instruments are hosted separately on:  
https://github.com/reduzent/netpd-instruments

You may want to clone everything at once by doing:

```
git clone --recursive https://github.com/reduzent/netpd.git
```

## supported platforms

netpd runs on any platform [Pure Data](https://puredata.info) runs on. This includes **Linux**, **macOS**,
**Windows**.

For [macOS](https://www.netpd.org/software/netpd-current-macos.dmg) and
[Windows](https://www.netpd.org/software/netpd-current-windows.zip) there are
batteries-included standalone apps available that should get you going quickly.

## prerequisites

Before runnning netpd you need to install [Pure Data](https://puredata.info) (Pd) (>= 0.52.0) from
[here](http://msp.ucsd.edu/software.html). You also need to install a few additional libraries.
They can be installed from Pd through the menu *Help* -> *Find externals*. The following libraries
need to be searched and installed:

  * iemlib
  * iemnet
  * osc
  * slip

**NOTE**: pd-l2ork is not supported (and support is not planned) because it
 has some incompatibilities with Pure Data.

## intro

* Open `netpd/main.pd` with Pd.  
  [chat](https://www.netpd.org/Chat) automatically connects to the server and you can
  now chat with other users currently online.  
  Click *list* to get a list all connnected users.

* Click the [unpatch](https://www.netpd.org/Unpatch) button in chat to launch
  the unpatch instrument manager. If there is already a session going on,
  the instruments used in the ongoing session are automatically loaded (they
  are first downloaded from other users, if necessary).

* Load instruments into the current session by clicking on any of the
  instrument names in the upper scroll list.  
  Alternatively, just type the name of the instrument (without the
  extension `.pd`) into the input box and hit enter.

* Show an instrument's GUI by clicking on its name in unpatch's lower section.
  You can now manipulate the instrument's parameters. Any changes are instantaneously
  synchronized between clients. Anyone can manipulate anything, so please be
  cautious and considerate when joining an ongoing session.

If you're lucky, someone is online and might help you get started. This is the easiest
and fastest way to get accustomed to all the instruments and how they interact with each
other. Of course, you can explore the instruments on your own as well. Maybe start
with [master](https://www.netpd.org/master) and [sine](https://www.netpd.org/sine).


## server

For online jams, netpd needs to connect to a [netpd-server](https://www.netpd.org/Server).
A public netpd-server is running at **netpd.org** on port **3025**.
This is the default server in netpd's configuration. The netpd-server software is available
here:  
https://github.com/reduzent/netpd-server.


## copyright

2008-2022, Roman Haefeli <roman@netpd.org>  
Published under the GNU Public License (GPL-2)
