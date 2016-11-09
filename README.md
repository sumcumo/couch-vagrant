# Vagrant Box for the demonstration of CouchDB 2.0.0 Clustering

## Have fun with Couchdb 2.0.0

The purpose of this repo is to provide a way to start three independent CouchDB nodes on a local machine. With the release of
[CouchDB 2.0](http://couchdb.apache.org) clustering was added. Unfortunately it is a bit tricky to run three
independent Docker CouchDB's - for example with the excellent [CouchDB Docker images from Clemens Stolle](https://hub.docker.com/r/klaemo/couchdb/). There is in fact an image you can use to simulate the clsutering, but
we wanted to have three IP adresses.

## Get started

This guide assumes you are running Mac OS X. But it should be the same for any Linux system.

1. Download and install [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
2. Download and install [Vagrant](https://www.vagrantup.com/downloads.html)
3. Clone this repository

        git clone https://github.com/sumcumo/couch-vagrant.git

4. Change into the directory couch-vagrant

        cd couch-vagrant

5. Run the Vagrantfile

        vagrant up

The last step will look for a Vagrant Box at [https://atlas.hashicorp.com/sc-weatherhog/boxes/vagrant-couch/]  (https://atlas.hashicorp.com/sc-weatherhog/boxes/vagrant-couch/), (don't follow the steps in the README there please), will download it and start three instances.

### Configuration

You have to decide to which interface on your local machine the Vagrant boxes will bridge to during the vagrant up command.

    ==> couch1: Available bridged network interfaces:
    1) en0: Wi-Fi (AirPort)
    2) en1: Thunderbolt 1
    3) en2: Thunderbolt 2
    4) p2p0
    5) awdl0
    6) bridge0
    ==> couch1: When choosing an interface, it is usually the one that is
    ==> couch1: being used to connect to the internet.
        couch1: Which interface should the network bridge to? 1

Now get the ip addresses - you will need them for opening each CouchDB webinterface via the browser. The port is always 5984. The names of the machines are: couch1, couch2, couch3

Connect to each of the three machines with:

    vagrant ssh couch1

Get the IP address with:

    sudo ifconfig

Finally, you will have to start CouchDB on each Vagrant box. Simply run:

    sudo /opt/couchdb/bin/couchdb couchdb -b

## Contributing

This is a first try. We are really happy about contributions. If you find a problem or have ideas for features, please add an issue.

## Thanks

Many thanks to [Lucas](https://github.com/orgs/sumcumo/people/lucasweatherhog) for putting together the Vagrant stuff.
