# Cloudera Launchpad Wrapper

Provide a thin, convenience wrapper around Cloudera Launchpad

## Requirements

The following environment variables are required to be set up on both the local and remote host:

* LAUNCHPAD_HOME
* LAUNCHPAD_WRAPPER_HOME

Python 2.6+ is also required as well as the Cloudera Manager python client:

```bash
git clone git://github.com/cloudera/cm_api.git
cd cm_api/python
python setup.py install
```

