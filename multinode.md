Multinode configuration
=======================


Generate the default answerfile on the controller node

```
$ packstack --gen-answer-file=/root/answer_file.txt
```

Update the following in the answerfile

```
CONFIG_CONTROLLER_HOSTS=192.168.1.205
CONFIG_COMPUTE_HOSTS=192.168.1.206
CONFIG_NETWORK_HOSTS=192.168.1.207
CONFIG_STORAGE_HOST=192.168.1.205
CONFIG_HORIZON_SSL=y
CONFIG_PROVISION_DEMO=n
```

Install OpenStack using the answerfile

```
$ packstack --answer-file=/root/answer_file.txt
```

In case you do not want to run the installation on already configured servers, add the following to the answerfile:

```
EXCLUDE_SERVERS=<serverIP>,<serverIP>,...
```
