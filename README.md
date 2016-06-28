# docker-sinatra-hello-world

A simple "Hello World" app using Docker, Sinatra, rbenv and bundler.

## Installation

### OS X

- install [brew](http://brew.sh/#install)

    ```
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

- install software dependencies

    ```
    brew tap homebrew/bundle
    brew bundle
    ```

- setup project

    ```
    cd ~/Code
    git clone git@github.com:mdzhang/vagrant-docker-sinatra-hello-world.git
    cd vagrant-docker-sinatra-hello-world
    vagrant up
    ```

    - **N.B**: I encountered an issue after installing Docker on Ubuntu 14.14 with mounting and guest permissions. You may have to

        ```
        vagrant plugin install vagrant-vbguest
        vagrant ssh
        sudo apt-get install linux-headers-$(uname -r)
        # Ctrl-D to end session
        vagrant reload --provision
        ```


- view app

    ```
    open localhost:4567
    ```

## Resources

- http://brew.sh/#install
- https://caskroom.github.io/
- http://sourabhbajaj.com/mac-setup/Docker/README.html
- https://docs.docker.com/engine/getstarted/step_two/
- https://docs.docker.com/v1.10/engine/userguide/containers/dockervolumes/
- https://www.vagrantup.com/docs/getting-started/project_setup.html
- https://atlas.hashicorp.com/vagrant
- https://www.getconvey.com/devblog/mounting-errors-during-installing-docker-on-an-ubuntutrusty64-vagrant-vm/

## TODO

- .dockerignore is not working with Vagrant as we'd hope