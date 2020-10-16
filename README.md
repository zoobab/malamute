[![noswpatv3](http://zoobab.wdfiles.com/local--files/start/noupcv3.jpg)](https://ffii.org/donate-now-to-save-europe-from-software-patents-says-ffii/)
# Malamute

[![Build Status](https://travis-ci.org/zeromq/malamute.svg?branch=master)](https://travis-ci.org/zeromq/malamute)

All the enterprise messaging patterns in one box.

![Malamute](https://github.com/malamute/malamute-core/blob/master/malamute.jpg)

[Read the whitepaper](MALAMUTE.md)

[Protocol wireframe](https://github.com/malamute/malamute-core/blob/master/src/mlm_proto.bnf)

[Stream protocol](STREAM.md)

## Building Malamute

To use or contribute to Malamute, build and install this stack:

    git clone git://github.com/jedisct1/libsodium.git
    git clone git://github.com/zeromq/libzmq.git
    git clone git://github.com/zeromq/czmq.git
    git clone git://github.com/zeromq/malamute.git
    for project in libsodium libzmq czmq malamute; do
        cd $project
        ./autogen.sh
        ./configure && make check
        sudo make install
        sudo ldconfig
        cd ..
    done

To run Malamute, issue this command:

    malamute [name]

Where 'name' is the name of the Malamute instance, and must be unique on any given host. The default name is 'local'. To end the broker, send a TERM or INT signal (Ctrl-C).

## How to Help

1. Use Malamute in a real project.
2. Identify problems that you face, using it.
3. Work with us to fix the problems, or send us patches.

## Ownership and Contributing

The contributors are listed in AUTHORS. This project uses the MPL v2 license, see LICENSE.

The contribution policy is the standard ZeroMQ [C4.1 process](http://rfc.zeromq.org/spec:22). Please read this RFC if you have never contributed to a ZeroMQ project.
