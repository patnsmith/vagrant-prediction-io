# vagrant-prediction-io

## Overview

This is a Vagrantfile to provision a box with a test PIO environment based on the docker-prediction-io repo.

## How to use

Download and install vagrant:

```sudo apt-get install vagrant```

Clone this repo and cd into the folder:

```git clone https://github.com/patnsmith/vagrant-prediction-io.git```
```cd vagrant-prediction-io```

To create a new VM:

```vagrant up```

To provision the VM with the necessary files:

```vagrant provision```

To ssh into the vm:

```vagrant ssh```

## Building and launching PIO

To build the test environment:

```sudo docker-compose -p TestEnv build```

To launch the test environment: 

```screen sudo docker-compose -p TestEnv up```

Once PIO is launched press "Ctrl + a + d" to detach the screen and check the services are still running: 

```sudo docker-compose -p TestEnv ps```
