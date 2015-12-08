pip_lock_down Docs
=============

Role to lock pip down to a particular links repo. This will create a
``.pip.conf`` which will ensure that the only python packages installed when
using pip are from a known repository of packages.


Basic Role Example
^^^^^^^^^^^^^^^^^^

.. code-block:: yaml

    - name: Basic lxc host setup
      hosts: host_group
      user: root
      roles:
        - { role: "pip_lock_down", tags: [ "pip-lock-down" ] }
      vars:
        pip_links:
          name: openstack-release
          link: https://openstack-hostname.something/python_packages/master
