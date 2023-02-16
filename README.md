# RabbitMQ

## Install guide

### on Ubuntu

`wget -O- https://www.rabbitmq.com/rabbitmq-release-signing-key.asc | sudo apt-key add - `

`echo "deb https://dl.bintray.com/rabbitmq-erlang/debian $(lsb_release -sc) erlang" | sudo tee /etc/apt/sources.list.d/bintray.erlang.list`

`echo "deb https://dl.bintray.com/rabbitmq/debian $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/bintray.rabbitmq.list`


`sudo apt-get update`

`sudo apt-get install rabbitmq-server`

(`apt list --installed | grep rabbit`)

libssl install error? ->

`echo "deb http://security.ubuntu.com/ubuntu focal-security main" | sudo tee /etc/apt/sources.list.d/focal-security.list`

`sudo apt-get update`

`sudo apt-get install libssl1.1`

### on MacOS

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

`brew update`

`brew install rabbitmq`

## How to start rabbitmq-server (& status)

### on Linux

`sudo service rabbitmq-server start`

`sudo service rabbitmq-server status`

### on MacOS

`brew services start rabbitmq`

`brew services stop rabbitmq`

`rabbitmqctl status`
# RabbitMQ

## Install guide

### on Ubuntu

`wget -O- https://www.rabbitmq.com/rabbitmq-release-signing-key.asc | sudo apt-key add - `
`echo "deb https://dl.bintray.com/rabbitmq-erlang/debian $(lsb_release -sc) erlang" | sudo tee /etc/apt/sources.list.d/bintray.erlang.list`
`echo "deb https://dl.bintray.com/rabbitmq/debian $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/bintray.rabbitmq.list`

`sudo apt-get update`
`sudo apt-get install rabbitmq-server`
(`apt list --installed | grep rabbit`)

libssl install error? ->
`echo "deb http://security.ubuntu.com/ubuntu focal-security main" | sudo tee /etc/apt/sources.list.d/focal-security.list`
`sudo apt-get update`
`sudo apt-get install libssl1.1`

### on MacOS

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
`brew update`
`brew install rabbitmq`

## How to start rabbitmq-server (& status)

### on Linux

`sudo service rabbitmq-server start`

`sudo service rabbitmq-server status`

### on MacOS

`brew services start rabbitmq`

`brew services stop rabbitmq`

`rabbitmqctl status`

## rabbitmqctl commands

- list queues

    `sudo rabbitmqctl list_queues`

- debug

    `sudo rabbitmqctl list_queues name messages_ready messages_unacknowledged`

- see log and export the output

    `python receive_logs.py > logs_from_rabbit.log`

- list_bindings

    `rabbitmqctl list_bindings`

- save only 'warning' and 'error' (and not 'info') log messages to a file

    `python receive_logs_direct.py warning error > logs_from_rabbit.log`
-
## rabbitmqctl commands

- list queues

    `sudo rabbitmqctl list_queues`

- debug

    `sudo rabbitmqctl list_queues name messages_ready messages_unacknowledged`

- see log and export the output

    `python receive_logs.py > logs_from_rabbit.log`

- list_bindings

    `rabbitmqctl list_bindings`

- save only 'warning' and 'error' (and not 'info') log messages to a file

    `python receive_logs_direct.py warning error > logs_from_rabbit.log`
-