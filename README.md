grabserial
==========

Grabserial - python-based serial dump and timing program - good for
embedded Linux development

See http://elinux.org/Grabserial for documentation and examples.

For help with command line options, use: grabserial -h

Installation
------------
If you have the python 'serial' module, you can just place grabserial
in a directory on your path, or add the directory containing grabserial
to your path, or just invoke grabserial directly.

This should work:

    $ sudo cp grabserial /usr/local/bin
    $ grabserial

You can also install this as a python module with: 'python setup.py install'
(Some users have reported problems with this - let me know if it doesn't
work for you.)

Example
-------

    $ `grabserial -d COM42 -a -b 115200 -e 5 -Q -o "%" -T`

Log with timestamp (-T) from COM42 with 115200:8N1:xonxoff=0:rtscts=0
Without serial data on stdout (-Q), for 1 hour (-e)
to "2017-06-13T22:45:08" (-o "%") and then restart (-a) to create new log.
