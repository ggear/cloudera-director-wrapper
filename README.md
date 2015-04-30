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

The Cloudera Director wrapper installation:

```bash
mkdir -p /usr/lib64/cloudera-director
cd /usr/lib64/cloudera-director
git clone https://github.com/ggear/cloudera-director-wrapper.git wrapper
```

The shell environment should include home directories pointing to the Director and Wrapper installs: 

```bash
export DIRECTOR_CLIENT_HOME=/usr/lib64/cloudera-director/client
export DIRECTOR_CLIENT_WRAPPER_HOME=/usr/lib64/cloudera-director/wrapper
```
