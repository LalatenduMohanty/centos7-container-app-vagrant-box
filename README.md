#CentOS Vagrant box with container tools.

`This branch i.e. UTB(Upstream Tracker Build) will have changes to build Vagrant images to include latest upstream bits i.e. docker, k8s, atomic etc.`

##Building the Vagrant box in CBS(CentOS build system)
* Get access for building images in CBS. Refer http://wiki.centos.org/HowTos/CommunityBuildSystem
* Checkout/git clone this repository
* Run the ```do_vagrant_cbs.sh```

```Here is the latest koji scratch build I did : <todo>`

##Running the Vagrant box
I used Fedora 21 and libvirt backend to run the vagrant box. 
##Setting up Vagrant on Fedora 21
To install Vagrant on Fedora 21
```yum/dnf install -y vagrant-libvirt vagrant```
##Running the Vagrant box on Fedora21 with Vagrant and libvirt

The image is available in https://atlas.hashicorp.com/atomicapp/boxes/dev-testing

`Step-1` : Initialising a new Vagrant environment by creating a Vagrantfile
```
    vagrant init atomicapp/dev-testing
```
`Step-2` : To start the vagrant image and ssh in to it, please run following command
```
    vagrant up
    vagrant ssh
```
`vagrant ssh` should take you inside of the Vagrant box

###To destroy the Vagrant box
```vagrant destroy```

##Running atomic app inside the vagrant box
Login to the vagrant box using `vagrant ssh` command. 

Then follow the below link for running an example atomic application
Refer: https://registry.hub.docker.com/u/aweiteka/helloapache/

Atomicapp: https://github.com/projectatomic/atomicapp
Nulecule: https://github.com/projectatomic/nulecule
 
##What does this vagrant box contains?
* docker
* @development
* deltarpm
* rsync
* git
* kubernetes
* etcd
* flannel
* bash-completion
* man-pages
* atomic
* docker-registry
* nfs-utils
* PyYAML
* libyaml-devel

##Future roadmap

`You are welcome to send pull requests too.`
