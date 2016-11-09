# Vagrant Box for the demonstration of CouchDB 2.0.0 Clustering

## Have fun with Couchdb 2.0.0

The purpose of this repo is to provide a way to start three independent CouchDB nodes on a local machine. With the release of
[CouchDB 2.0](http://couchdb.apache.org) clustering was added. Unfortunately it is a bit tricky to run three
independent Docker CouchDB's - for example with the excellent [CouchDB Docker images from Clemens Stolle](https://hub.docker.com/r/klaemo/couchdb/). There is in fact an image you can use to simulate the clsutering, but
we wanted to have three IP adresses.

## Get started

This guide assumes you are running Mac OS X. But it should be the same for any Linux system.

1. Download and install [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
2. Download and install [Virtualbox-Extension-Pack] (http://download.virtualbox.org/virtualbox/5.1.8/Oracle_VM_VirtualBox_Extension_Pack-5.1.8-111374.vbox-extpack)
3. Download and install [Vagrant](https://www.vagrantup.com/downloads.html) - For the time of writing there is a major bug with Vagrant 1.8.7 so please use 1.8.6 unless you don't care fixing the installation.
4. Clone this repository

        git clone https://github.com/sumcumo/couch-vagrant.git

5. Change into the directory couch-vagrant

        cd couch-vagrant

6. Run the Vagrantfile

        vagrant up

The last step will look for a Vagrant Box at [https://atlas.hashicorp.com/sc-weatherhog/boxes/vagrant-couch/]  (https://atlas.hashicorp.com/sc-weatherhog/boxes/vagrant-couch/), (don't follow the steps in the README there please), will download it and start three instances.

### Configuration

Vagrant will start 3 machines with the IP addresses configured in the Vagrantfile. The IP addresses are for:

    couch1 : 172.28.128.111
    couch2 : 172.28.128.121
    couch3 : 172.28.128.132

You will have to start CouchDB on each Vagrant box by hand. For the start Simply run:

    sudo /opt/couchdb/bin/couchdb couchdb -b

CouchDB 2.0.0 will be reachable via port 5984

## Open CouchDB

If you made it to this point, you will now be able top open each running CouchDB and its Webinterface Fauxton in the browser.

## Contributing

This is a first try. We are really happy about contributions. If you find a problem or have ideas for features, please add an issue.

## Thanks

Many thanks to [Lucas](https://github.com/orgs/sumcumo/people/lucasweatherhog) for putting the Vagrant stuff together.
