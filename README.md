# Jmeter Homework
## Common features:
## 1. Open `jmeter.bat` file to open Jmeter.
## 2. Threade Group
To create `Thread Group` do right mouse click on `Test Plan`--> `Add` --> `Threade (Users)` --> `Thread Group`
## 3. Configuring `Threade Group`. Adding info
+ Number of threads (users)
+ Rump-up period (seconds)
+ Loop count infinite or particular number
## 4. Add request
1. To create `HTTP request` do right mouse click on `Thread Group` --> `Add` --> `Sampler` --> `HTTP Request`
2. Add info:
+ `Protocol`
+ `IP`
+ `Port Number`
+ `Method`
+ `Path`
## 5. When everything added --> push `run` button.
## 6. When everything done push `stop` button.
## To see `analytics`:
+ Right mouse click on `Thread Group`--> `Add` --> `Listener` --> `View Result Tree`
+ Right mouse click on `Thread Group`--> `Add` --> `Listener` --> `Summary Report`
+ Right mouse click on `Thread Group`--> `Add` --> `Listener` --> `View Results in table`
### In `View Result tree` we can see the result of request and its request ans response data
### In `View Results in Table` we can see a table with additional information about request.
### In `Summary Report` we can see the report and save it.
## Note! If you want your request to be counted in analytics, put them `higher` in a Test Plan tree than `statistics counters`
