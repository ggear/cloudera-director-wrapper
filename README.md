# Cloudera Director Wrapper

Provide a thin, convenience wrapper around the Cloudera Director Client

## Requirements

* Python 2.6+
* Cloudera Manager Python Client 5+
* Cloudera Director Client 1.0+

## Installation

The Cloudera Director Client installation:

http://www.cloudera.com/content/cloudera/en/documentation/cloudera-director/latest/topics/director_install_client_task.html

The Cloudera Manager python client installation (requires Python):

```bash
git clone git://github.com/cloudera/cm_api.git
cd cm_api/python
python setup.py install
```

The Cloudera Director wrapper build and installation:

```bash
git clone https://github.com/ggear/cloudera-director-wrapper.git
cd cloudera-director-wrapper
mvn clean install
mkdir -p /usr/lib64/cloudera-director/wrapper
tar xvzf target/cloudera-director-wrapper-*-bin.tar.gz -C /usr/lib64/cloudera-director/wrapper --strip 1
```

The shell environment should include home directories pointing to the Director and Wrapper installs: 

```bash
export DIRECTOR_CLIENT_HOME=/usr/lib64/cloudera-director/client
export DIRECTOR_CLIENT_WRAPPER_HOME=/usr/lib64/cloudera-director/wrapper
```

## Configuration

The Director Client Wrapper is driven by a single configuration file, an example of which ships with the install:

```bash
vi /usr/lib64/cloudera-director/wrapper/cfg/cluster.conf
```

## Running

The Director Client Wrapper runs transparently over a local Director Client:

```bash
cloudera-director clean
cloudera-director bootstrap
cloudera-director client
```

or can be run from a remote machine (bootstrap is run as a resumable deamon processs):

```bash
cloudera-director-remote my-user@my.host.com clean
cloudera-director-remote my-user@my.host.com bootstrap
cloudera-director-remote my-user@my.host.com client
```
