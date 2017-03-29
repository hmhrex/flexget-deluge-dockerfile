# Flexget Docker container (w/ Deluge support)

In order to use [Deluge](http://deluge-torrent.org/) with [Flexget](https://flexget.com/) you have to have local copies of the Deluge python modules. This container has the Deluge packages installed but doesn't run Deluge. It is intended to be used alongside a separate Deluge docker container.

## Installation

```
docker create \
  --name flexget \
  --net=host \
  -v </path/to/your/configuration/files>:/flexget \
  hmhrex/flexget-deluge
```
  
Parameters:

- --net=host - Shares host networking with container, required.
- -v /flexget - Deluge configuration files directory

## Configuration

To understand how to configure Flexget, I recomment their [documentation](https://flexget.com/Configuration).
