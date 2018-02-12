# Ansible Role: Install Docker CE

Install the latest version of [Docker CE](https://www.docker.com/community-edition) and [Docker Compose](https://docs.docker.com/compose/) on Ubuntu, following these [instructions](https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-using-the-repository). 

Tested on Ubuntu 16.04.

## Role Variables

The following variables can be used to customize the role:

    docker_users: []

A list of users that will be added to the `docker` group.

    docker_repository: stable

Select the repository to install from (choose from stable, edge, and test).

## Example Playbook

    - hosts: all
      become: yes
      roles:
        
        - role: docker-ce
          docker_users:
            - foo
            - bar

## License

MIT
