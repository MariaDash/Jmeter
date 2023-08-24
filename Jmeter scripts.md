# Jmeter Scripts
## We Will work with Java Groovy Language
### Creating first HTTP request with variables and environment
1. Open Test Plan
2. Create  HTTP Request Defaults add ip:`5.75.203.123 ` and port `5005`, protocol `HTTP`
3. Create Thread Group add 100 threads
4. Add Thread Group --> Add --> Sampler --> HTTP Request--> name it as `login`
5. In HTTP Request add path: `/login`    and parameters: `login`: `Mariia`, `password`: `123` and `method POST`
6. Add View Result tree
7. Run request
8. See results in View Result Tree
9. Get token
10. HTTP Request aka login --> Add --> Post Processors --> JSON Extractor
11. Open JSON Extractor-->
+ Add Name of created variables: `token`
+ Add JSON Path expressions: `$token`
+ Match No. : `1`
12. Sending a variable to the environment:
+ Thread Group    --> Add --> Assertions --> BeanShell Assertion --> `${__setProperty(token,${token})}`
### Creating second HTTP request with variables and environment
1. Create new Thread Group and new HTTP Request `new data`
2. Move HTTP Request Defaults to the top 
3. We need to get token for `new data` so we use PreProcessor:
+ new data (thread group) --> Add --> Pre Processors --> BeanShell Preprocessor--> move it `higher` than request
+ Add script:
```
String auth_token = props.get("token");
vars.put("token", auth_token);
```
### Additing `new data` request
+ Method POST
+ PATH: /new_data
+ Parameters: `authtoken`: `${token}`
              `name`: `Mariia`
              `age`: `35`
              `salary`:`1500`
+ Add View Results Tree and run
+ See the results
+ Add Summary Report       
So on so forth see [Summary Report](https://github.com/MariaDash/Jmeter/blob/main/summary_scripts.csv) and [.jmx file](https://github.com/MariaDash/Jmeter/blob/main/Script.jmx)                
