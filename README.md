Cobalt resource plugin for OpenStack Heat
===========

Overview
--------

This plugin provides a new resource type (`OS::Cobalt::Instance`) which largely imitates the `AWS::EC2::Instance` resource type. Rather than boot instances from scratch, Heat templates using this plugin can launch [Cobalt live-images](https://github.com/gridcentric/cobalt), taking advantage of Gridcentric's [Virtual Memory Streaming](http://gridcentric.com/technology/vms/) technology for faster application readyness and lower resource consumption.

Installation
------------

Heat plugins must reside in the `plugins_dir` directory defined in [the Heat Engine configuration file](https://wiki.openstack.org/wiki/Heat/Plugins#Installation_and_Configuration). By default, the directories `/usr/lib64/heat` and `/usr/lib/heat` are searched.

To install the Cobalt resource plugin to an unmodified Heat installation using setuptools:

    sudo python setup.py install --install-purelib=/usr/lib/heat


Note that you can also install the Cobalt resource plugin via pip:

    sudo pip install --install-option="--install-purelib=/usr/lib/heat" cobalt-heat


Examples
--------

See the directory [examples/](examples/) for examples.
