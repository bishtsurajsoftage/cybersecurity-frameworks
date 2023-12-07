# cybersecurity-frameworks

# D.A.R.W.I.N 

Darwin is an open souce **Artificial Intelligence Framework for CyberSecurity**. It can be compiled and run on **both FreeBSD and Linux**.

We provide packages and support for FreeBSD.

Darwin is:
  - A multi-threaded C++ engine that runs **security filters** that work together to improve your network security
  - A collection of **agents** that use the DARWIN protocol to query the security filters accordingly

Darwin is still in an alpha stage, so few filters are available at this time.

Using the provided documentation and SDK you can develop your own Darwin Filters.

We are seeking help! Testers and volunteers are welcome!

Advens (www.advens.fr) also provides commercial filters for Darwin !

## Filters

### Compilation 
To compile all the filters available, please enter the following:

```sh
cmake .
make -j4
```
To compile a specific filter:
```sh
cmake . -DFILTER=FILTER_NAME
make -j4
```

you can choose a filter from this set:
```sh
cmake . -DFILTER="FILTER_NAME1;FILTER_NAME2"
make -j4
```

Don't forget to unset the 'filter' variable if you want to compile all the filters available afterwards:
```sh
cmake . -UFILTER
make -j4
```

The compiled filter will be named 'darwin_filter_name'

### Usage

Positional arguments:
 - 'filter_name' Specify the name of this filter in the logs
 - 'socket_path' Specify the path to the unix socket for the main connection
 - 'config_file' Specify the path to the configuration file
 - 'pid_file' Specify the path to  the containing the pid of the process
 - 'output' Specify the filter's output
 - 'cache_size' Integer specifying cache's size
 - 'threshold' Integer specifying the filter's threshold

### Python Version
Compatible with python 3.5.3 and later.

### Usage
Usage:
Positional arguments:
'config_file'  the config file to use

Optional arguments

'-h', '--help' show this help message and exit

## The Service
In the service directory is a rc script named 'darwin' that is the service script. It handles the following commands: 'start', 'stop', 'status', and 'restart'.


## Usage
*Use this for debug purpose only.*

Usage: 'manager.py [-h] [-l {DEBUG,INFO,WARNING,ERROR,CRITICAL}] CONFIG_FILE'

















 












































