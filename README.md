# spring-cloud-task-sink
To navigate to the management console, Log into rabbitmq image docker exec -it 192.168.99.100 bash
run all this commands
1.- echo "deb http://www.rabbitmq.com/debian/ testing main" > /etc/apt/sources.list.d/rabbitmq.list
2.- apt-get -qq update > /dev/null
3.- apt-get -qq -y install rabbitmq-server > /dev/null
4.- /usr/sbin/rabbitmq-plugins enable rabbitmq_management
5.- echo "[{rabbit, [{loopback_users, []}]}]." > /etc/rabbitmq/rabbitmq.config

To log into management console
user:guest
password:guest

Notes
Add a new user, say user ‘test’ and password ‘test’
rabbitmqctl add_user test test
Give administrative access to the new access
rabbitmqctl set_user_tags test administrator
Set permission to newly created user
rabbitmqctl set_permissions -p / test ".*" ".*" ".*"

log into docker image docker exec -it <containerIdOrName> bash