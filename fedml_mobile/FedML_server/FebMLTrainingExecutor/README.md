# FebMLTrainingExecutor
> EMQ X,Docker,Flask,Gunicorn

# 1 Install EMQ X
You can go to [EMQ X Docs](https://docs.emqx.io/broker/latest/en/) for other questions
## 1.1 MacOS Install EMQ X
```shell script
# Add EMQ X tap
brew tap emqx/emqx
# Install EMQ X Broker
brew install emqx
# 
```
# 2 EMQ X Instructions
## 2.1 Start EMQ X
### 2.1.1 Start EMQ X broker in the background
```shell script
$ emqx start
EMQ X Broker v4.1.1 is started successfully!
```
## 2.1.2 systemctl start
```shell script
$ sudo systemctl start emqx
EMQ X Broker v4.1.1 is started successfully!
```
### 2.1.3 service start
```shell script
$ sudo service emqx start
EMQ X Broker v4.1.1 is started successfully!
```
## 2.2 Check the status of EMQ X Broker
### 2.2.1 Check Broker status
```shell script
$ emqx_ctl status
Node 'emqx@127.0.0.1' is started
emqx 4.1.1 is running
```
### 2.2.2 Ping EMQ X Broker
```shell script
$ emqx ping
pong
```
## 2.3 Other Basic command
### 2.3.1 Stop EMQ X Broker
```shell script
$ emqx stop
ok
```
### 2.3.2 Restart EMQ X Broker
```shell script
emqx restart
EMQ X Broker v4.1.1 is stopped: !!!!
EMQ X Broker v4.1.1 is started successfully!
```
### 2.3.3 Start EMQ X Broker with console
```shell script
emqx console
```
### 2.3.4 Start EMQ X Broker with console
```shell script
emqx foreground
```
## 2.4 View Dashboard
EMQ X Dashboard is a web application, and you can access it directly through the browser without installing
 any other software.
When EMQ X Broker runs successfully on your local computer and EMQ X Dashboard is enabled by default, 
you can visit http://localhost:18083 to view your Dashboard. The default user name is admin and the password is public .
# 3 Quick Start FebMLTrainingExecutor
## 3.1 install dependencies
```bash
pip install -r requirements.txt
```
gunicorn maybe need add to PATH:
```bash
echo 'export PATH="/{your machine path}}/Python/3.7/bin:$PATH"' >> ~/.bash_profile
```
## 3.2 start FebMLTrainingExecutor
```bash
# start TrainingExecutor server
sh svr_ctrl.sh start
# stop TrainingExecutor server
sh svr_ctrl.sh stop
# restart TrainingExecutor server
sh svr_ctrl.sh restart
# query the server status
sh svr_ctrl.sh status
```