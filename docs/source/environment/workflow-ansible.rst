.. _environment-workflow-ansible:

Workflow: Ansible
=================

.. include:: /environment/partials/workflow-prerequisites.rst

Configure Environment
---------------------

- Install ansible (>v2.8.0)::

    $ yum install -y epel-release
    $ yum install -y ansible

- Create hosts file::

    $ cat << EOF > /etc/ansible/hosts
    [gateway]
    gateway1

    [compute]
    node01
    node02
    EOF

- Setup playbook::

    $ yum install -y git
    $ git clone https://github.com/openflighthpc/openflight-ansible-playbook

.. warning:: It is highly recommended to inspect all roles and edit them to your requirement or, alternatively, write your own roles. These roles are provided "as is" and no guarantee is made that the roles will function properly in environments different to that of the example environment used in this documentation.

- Run playbook::

    $ cd openflight-ansible-playbook
    $ ansible-playbook openflight.yml

.. note:: The playbook may hang trying to verify the SSH fingerprints of the hosts if none of them have been logged into before from the ansible host. It is recommended to have already established a trusted SSH connection to all systems first.
