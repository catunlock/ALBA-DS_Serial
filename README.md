# ALBA Python Serial DeviceServer

[![ALBA Python Serial DeviceServer](https://img.shields.io/pypi/v/tangods_serialline.svg)](https://pypi.python.org/pypi/tangods_serialline)


[![ALBA Python Serial DeviceServer updates](https://pyup.io/repos/github/catunlock/tangods_serialline/shield.svg)](https://pyup.io/repos/github/catunlock/tangods_serialline/)


ALBA Python Serial device server for tango. with the aim to be API compatible
with the C++ Tango Serial device server extending its functionality.

This device server internally uses [pyserial](https://pythonhosted.org/pyserial/) meaning that supports the same serial protocols, like rfc2217:// socket:// loop:// hwgrep:// spy:// alt://

## Installation

From within your favorite python environment type:

`$ pip install tangods_serialline`



### Tango server

Register a Serial tango server in the tango database:
```
$ tangoctl server add -s Serial/test -d Serial test/tangods_serialline/1
$ tangoctl device property write -d test/tangods_serialline/1 -p serialline -v "rfc2217://192.168.123:5000"
```

(the above example uses [tangoctl](https://pypi.org/project/tangoctl/). You would need
to install it with `pip install tangoctl` before using it. You are free to use any other
tango tool like [fandango](https://pypi.org/project/fandango/) or Jive)

Launch the server with:

```terminal
$ Serial test
```


## Credits

### Development Lead

* Alberto López Sánchez <alopez@cells.es>
* CTBeamlines (ctbeamlines@cells.es)

### Contributors

None yet. Why not be the first?
