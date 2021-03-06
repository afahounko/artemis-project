# Introduction

Artemis aims to automate the deployment and the documentation of a cloud infrastructure (cluster, hypervisors, virtual machines, routers, switches...).
  
# Purpose of Artemis

It will help to:

* automate processes
* deploy and maintain cloud infrastructure (Origin-OpenShift, OpenStack, Satellite, Kubernetes, Docker containers ...)
* document the infrastructure
* plan resources exhausion
* master changes with a continuis integration (CI) and a continious deployment (CD)

# Tools in place

  * Netdot (IPAM)
  * FreeIPA
  * GitLab
  * GitLab-runner
  * OpenvSwitch as Software Defined Network (SDN)
  * LibVirt as Hypervisor module
  * Ansible for the automation tool
  * Git for local config file storage and versionning
  * Python and Jinja2  will be the scripting languages


# Requirements

  Device with a chips compatible with Linux Kernel. In our case we use Redhat 7, CentOS 7 or Fedora 27

~~~
  RAM : 8  GB
  HDD:  40 GB
  vCPU: 4
~~~


# Troubleshooting

~~~

docker stop $(docker ps -a -q) # stop all docker containers
docker rm -f $(docker ps -a -q) # remove all docker containers
docker images -q | xargs docker rmi -f # remove all docker images
sudo pip uninstall docker-compose # uninstall docker-compose

Then reinstalled docker-compose:
sudo pip install -U docker-compose
~~~