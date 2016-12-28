# spring-cloud-task-sink
Log into rabbitmq image docker exec -it 192.168.99.100 bash
run all this commands
echo "deb http://www.rabbitmq.com/debian/ testing main" > /etc/apt/sources.list.d/rabbitmq.list
apt-get -qq update > /dev/null
apt-get -qq -y install rabbitmq-server > /dev/null
/usr/sbin/rabbitmq-plugins enable rabbitmq_management
echo "[{rabbit, [{loopback_users, []}]}]." > /etc/rabbitmq/rabbitmq.config