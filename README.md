Nova Documentation
View on GitHub (opens new window)
Nova
Installation
Installation
Quickstart
Usage
Desired Version
Contributin
#Installation
#From GitHub Releases
Visit the releases page (opens new window)to find the release that's right for your environment. For example, on Linux:
'''
curl -L "https://github.com/FairwindsOps/nova/releases/download/3.2.0/nova_3.2.0_linux_amd64.tar.gz" > nova.tar.gz
tar -xvf nova.tar.gz
sudo mv nova /usr/local/bin/
'''

#asdf-vm
'''
asdf plugin-add nova
asdf install nova latest
asdf local nova latest
'''

#Homebrew
'''
brew tap fairwindsops/tap
brew install fairwindsops/tap/nova
'''

#From source
'''
go get github.com/fairwindsops/nova
'''


#Quickstart
Install the golang binary and run it against your cluster.

$ go get github.com/fairwindsops/nova
'''
$ nova find
'''

To check for outdated container images, instead of helm releases:
'''
$ nova find --containers
'''

#Usage
'''
nova find --wide

nova find --containers --show-errored-containers

nova --format=table find --helm --containers
'''

#Using a Config File
'''nova.yaml

desired-versions:
  metrics-server: 6.0.0
'''
'''
  Example run with config:

  $ nova find --config nova.yaml
'''
'''
Using the CLI
$ nova find --desired-versions='metrics-server=6.0.0,vpa=12.0.0'
'''

#More
visit:https://nova.docs.fairwinds.com/desired-versions/#using-a-config-file



