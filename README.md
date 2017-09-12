Ansible Role: Docker
====================

An Ansible Role that installs [Docker](https://www.docker.com) on Linux.


Requirements
------------

Compliant with :
- Debian 8 (Jessie)
- Debian 9 (Stretch)

Other:
- Fact gathering should be allowed in ansible-playbook (By default)
- The role require the superuser privileges. The task should be used with remote_user root or with a sudo/su grant


Role Variables
--------------

Available variables with defaults values are defined in `defaults/main.yml`.

Modifiables variables and possible values are listed below :

- docker_edition: 'ce' (Community Edition) or 'ee' (Entreprise Edition)
- docker_package: "docker-{{ docker_edition }}" (Latest version) or "docker-{{ docker_edition }}-<VERSION>" (Specific version)
- docker_apt_release_channel: 'stable' (Take packages from Stable channel) or 'edge' (From Edge channel)


Dependencies
------------

none


Example Playbook
----------------

How to use the role in your ansible playbook.

    - name: Playbook Task to install docker role
      hosts: docker-servers (Group of servers on which you want to install docker)
      roles:
         - { role: kabolt.docker, tags: [ 'docker' ] }


ToDo
----

- Add tests
- Add CI Integration
- Provide docker uninstall


License
-------

GPLv3


Author Information
------------------

This role is maintained by maximiliend. Issues and Merge Request are welcome.
