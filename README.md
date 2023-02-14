# RabbitMQ

## Installguide on Ubuntu

`wget -O- [https://www.rabbitmq.com/rabbitmq-release-signing-key.asc](https://www.rabbitmq.com/rabbitmq-release-signing-key.asc) | sudo apt-key add -
echo "deb [https://dl.bintray.com/rabbitmq-erlang/debian](https://dl.bintray.com/rabbitmq-erlang/debian) $(lsb_release -sc) erlang" | sudo tee /etc/apt/sources.list.d/bintray.erlang.list
echo "deb [https://dl.bintray.com/rabbitmq/debian](https://dl.bintray.com/rabbitmq/debian) $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/bintray.rabbitmq.list`

`sudo apt-get update
sudo apt-get install rabbitmq-server`

## How to start rabbitmq-server (& status)

### on Linux

`sudo service rabbitmq-server start`

`sudo service rabbitmq-server status`

### on MacOS

`brew services start rabbitmq`

`brew services stop rabbitmq`

`rabbitmqctl status`

## rabbitmqctl commands

`sudo rabbitmqctl list_queues`