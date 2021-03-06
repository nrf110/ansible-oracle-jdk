Ansible Oracle JDK for Ubuntu
==

Installs Oracle JDK on Ubuntu 16.04 (may work on other versions, but not tested)

**Example Play**:
```
---
- hosts: all
  roles:
    - role: ansible-oracle-jdk
      java_temp_dir: '/opt'
```

Requirements
------------
* Ubuntu 16.04 comes with python3 by default.  You will either need to specify the path to the python executable, or install python 2.7.x

Variables
---------
```
java_version: 'jdk1.8.0_72'
java_install_dir: '/usr/share/java'
java_temp_dir: '/tmp'
java_archive: 'jdk-8u72-linux-x64.tar.gz'
java_source_url: 'http://download.oracle.com/otn-pub/java/jdk/8u72-b15'
java_alternative: '/usr/bin/java'
java_home: '/usr/lib/java'
java_real_home: "{{ java_install_dir }}/{{ java_version }}"
```

Dependencies
------------
None
