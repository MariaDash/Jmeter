# Jmeter Homework
## Open `jmeter.bat` file to open Jmeter.
## Threade Group
To create `Thread Group` do right mouse click on `Test Plan`--> `Add` --> `Threade (Users)` --> `Thread Group`
## Configuring `Threade Group`. Adding info
+ Number of threads (users)
+ Rump-up period (seconds)
+ Loop count infinite or particular number
## Add request
1. To create `HTTP request` do right mouse click on `Thread Group` --> `Add` --> `Sampler` --> `HTTP Request`
2. Add info:
+ `Protocol`
+ `IP`
+ `Port Number`
+ `Method`
+ `Path`
## When everything added --> push `run` button.
## When everything done push `stop` button.
## To see `analytics`:
+ Right mouse click on `Thread Group`--> `Add` --> `Listener` --> `View Result Tree`
+ Right mouse click on `Thread Group`--> `Add` --> `Listener` --> `Summary Report`
+ Right mouse click on `Thread Group`--> `Add` --> `Listener` --> `View Results in table`
