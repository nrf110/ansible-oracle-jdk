Ansible Oracle JDK for Ubuntu
==

Installs Oracle JDK on Ubuntu 16.04 (may work on other versions, but not tested)

**Example Play**:
```
---
- hosts: all
  roles: 
    - role: ansible-oracle-jdk
      java:
        temp_dir: '/opt'
```

Requirements
------------
* Ubuntu 16.04 comes with python3 by default.  You will either need to specify the path to the python executable, or install python 2.7.x

Variables
---------
```
# NOTE: This role uses configuration hash instead of namespacing keys.  Overriding values will require either using set_fact with the combine filter, or setting `hash_behiavor = merge` in ansible.cfg
java:
  home: '/usr/lib/java'
  alternative: '/usr/bin/java'
  version: 'jdk1.8.0_72'
  archive: 'jdk-8u72-linux-x64.tar.gz'
  source_url: 'http://download.oracle.com/otn-pub/java/jdk/8u72-b15'
```

Dependencies
------------
None

