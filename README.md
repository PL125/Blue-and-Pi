# fiatcan - Fiat Doblò Infotainment app

This repo documents with Python3 code the findings documented on [Medium](https://medium.com/@fmntf) regarding the CAN frames that you can observe in a Fiat Doblò type 263.

The goal is to prototype a reimplementation of the [Blue&Me](https://en.wikipedia.org/wiki/Blue%26Me) infotainment system, abandoned by FCA after the release of UConnect.

### Compatibility
Although the code has been tested only on Fiat Doblò (263), most of those information may be valid for similar FCA cars equipped with Blue&Me, like:
 * Fiat Punto (199)
 * Fiat Qubo (225)
 * Fiat Panda (312)
 * Alfa Romeo 147 (937)
 * Alfa Romeo 159 (939)
 * Alfa Romeo MiTo (955) 

### Current State
Most of the infotainment related CAN frames have been decoded:

 * network wakeup / shutdown
 * PROXI protocol validation
 * steering wheel buttons
 * Media Player, Voice, Phone, Navigation, FM radio audio channels
 * Bluetooth A2DP and HFP/HSP support
 * debug menu on the instrument panel display

### Build deb package

* build-essential debhelper dh-systemd are needed.

* Rasperry Pi OS doesn't have dh-systemd but the package is platform agnostic, so you can get the [Debian version](https://packages.debian.org/buster/all/dh-systemd/download) and install that.

* Create the package from the source using dpkg-buildpackage -us -uc
 






