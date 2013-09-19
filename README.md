Python OTR
==========
This is a pure Python OTR implementation; it does not bind to libotr.

Included in this package is a Gajim Python plugin to enable OTR support
in the Gajim XMPP/Jabber client. This plugin is called gotr.

Install the potr Python module:

    sudo python setup.py install

Note that this will install (but not activate) the gajim-otr plugin if a
gajim directory can be found in $PREFIX/share/gajim.

__Dependencies__: pycrypto >= 2.1 (see [dlitz/pycrypto](https://github.com/dlitz/pycrypto))

Usage Notes
===========
This module uses pycrypto's RNG. If you use this package in your application and your application
uses `os.fork()`, make sure to call `Crypto.Random.atfork()` in both the parent and the child process.

Gajim OTR Plugin
================
As mentioned above, a gajim-otr plugin is provided in src/gajim-plugin and
can be installed using distutils.

The gajim search path can be changed manually by specifiying `--gajim-dir` to
the install commmand:

    sudo python setup.py install --gajim-dir=~/gajim

After installing, the plugin must be manually enabled in the Gajim plugin
interface.

Reporting bugs
==============
Please read the [FAQ](https://github.com/afflux/pure-python-otr/wiki) before submitting your
issue to the [tracker](https://github.com/afflux/pure-python-otr/issues).

libotr SWIG bindings
====================
python-otr.pentabarf.de and pyotr.pentabarf.de redirect here.
If you are still looking for the old C library bindings, they have moved
to <http://python-otr-old.pentabarf.de/>
