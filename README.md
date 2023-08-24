# [Jmeter Homework](https://github.com/MariaDash/Jmeter/blob/main/Jmeter_homework.md)
# [Jmeter Sniffing&Plugins](https://github.com/MariaDash/Jmeter/blob/main/Jmeter_sniffing&plugins.md)
# [Jmeter Scripts]()
# Jmeter Common features:
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
+ Add `Parameters` if you want to add some parameters to `GET` request
+ Add `Parameters`and put a `tick` to `Use multipart/form data` if you want to add some parameters to `POST` request in `form data`
+ ` Body Data` in `JSON` if you want to add body request in json format  for POST request
## 5. When everything added --> push `run` button.
## 6. When everything done push `stop` button.
## 7. To see `analytics`:
+ Right mouse click on `Thread Group`--> `Add` --> `Listener` --> `View Result Tree`
+ Right mouse click on `Thread Group`--> `Add` --> `Listener` --> `Summary Report`
+ Right mouse click on `Thread Group`--> `Add` --> `Listener` --> `View Results in table`
### In `View Result tree` we can see the result of request and its request ans response data
### In `View Results in Table` we can see a table with additional information about request.
### In `Summary Report` we can see the report and save it.
### For clearing Statistics use `Brush` button.
### Note! If you want your request to be counted in analytics, put them `higher` in a Test Plan tree than `statistics counters`
### Analysing summary report:
+ if Error% is less than 3% - server is Ok.
+ if Error% is in between 3 and 5 % - it is an error there you should work in here
+ if Error% is more than 5% - server is in danger, big problem here.
  

