﻿# Requirements
MonAutopsy requires [Python 3](https://www.python.org/downloads/) to run.

[pip](https://pip.pypa.io/en/stable/) is also required to install all the dependencies. (pip is already installed if you are using Python 2 >=2.7.9 or Python 3 >=3.4)

# Installation
Install the dependencies to execute the program.

Windows:
```sh
> py -m pip install -r requirements.txt
```
Linux:
```sh
$ python3 -m pip install -r requirements.txt
```

# Execution

MonAutopsy starts by calling monitor.py

Windows:
```sh
> py monitor.py
```
Linux:
```sh
$ python3 monitor.py
```

# Json File
MonAutopsy uses a JSON file to store all the parameters necessary for it's correct execution

- CPU and memory Usage

|                |Min                            |Max						   |
|----------------|-------------------------------|-----------------------------|
|CPU Usage		 | Minimum CPU usage for a notification to be triggered           | Maximum CPU usage for a notification to be triggered           
|Memory          | Minimum memory usage for a notification to be triggered           |Maximum memory usage for a notification to be triggered            

# 

- Notifications Setting

|      |SMTP Server                |Sender Email|Receiver Email| 
|------|---------------------------|------------------------------------------|---
|Notify|SMTP Server URL            |Server username and sender email for all emails sent by the program|Receiver email for all emails sent by the program|
#
 - Time intervals for monitorization and statistics

|      |Process                |Report| 
|------|---------------------------|------------------------------------------
|Time Interval|Interval (in seconds) for monitorization operations            |Interval (in seconds) in which the periodic report is sent to the receiver email

### Example:
```json
{
	"cpu_usage": {
		"min": "20",
		"max": "70"
	},
	"memory": {
		"min": "1000",
		"max": "5000"
	},
	"notify": {
		"SMTPServer": "smtp.gmail.com",
		"senderEmail": "monautopsy.notify@gmail.com",
		"receiverEmail": "12345@mail.pt"
	},
	"time_interval":{
		"process": "5",
		"report": "120"
	}
}
```
