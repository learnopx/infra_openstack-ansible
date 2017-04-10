OpenStack Neutron
#################
:tags: openstack, neutron, cloud, ansible
:category: \*nix

Role for deployment, setup and installation of Neutron.

This role will install the following:
    * neutron-server
    * neutron-agents

.. code-block:: yaml

    - name: Installation and setup of Neutron
      hosts: neutron_all
      user: root
      roles:
        - { role: "os_neutron", tags: [ "os-neutron" ] }
      vars:
        neutron_galera_address: "{{ internal_lb_vip_address }}"
