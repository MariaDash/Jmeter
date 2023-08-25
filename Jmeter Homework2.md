# Jmeter Homework 2
1) http://162.55.220.72:5005/user_info
req. (RAW JSON)
POST
age: int
salary: int
name: str
auth_token


resp.
{'start_qa_salary':salary,
  'qa_salary_after_6_months': salary * 2,
  'qa_salary_after_12_months': salary * 2.9,
  'person': {'u_name':[user_name, salary, age],
                                 'u_age':age,
                                 'u_salary_1.5_year': salary * 4}
                                 }

Actions:
1) Get the value from the 'qa_salary_after_6_months' field from Respose and pass it to the salary field of the request http://162.55.220.72:5005/new_data
===================

2) http://162.55.220.72:5005/new_data
req.
POST
age: int
salary: int
name: str
auth_token

Resp.
{'name':name,
   'age': int(age),
   'salary': [salary, str(salary*2), str(salary*3)]}

Actions:
1) Get the value from the 'name' field from Respose and pass it to the name field of the request http://162.55.220.72:5005/new_data

===================

3) http://162.55.220.72:5005/test_pet_info
req.
POST
age: int
weight: int
name: str
auth_token


Resp.
{'name': name,
  'age': age
  'daily_food':weight * 0.012,
  'daily_sleep': weight * 2.5}


Tests:
1) Get the value from the age field from Respose and pass it to the age field of the request http://162.55.220.72:5005/get_test_user


Exercise ***
0) Learn how Response Assertion works.
1) Make an Assertion to check status code 200
2) Make an Assertion to check 'daily_food':weight * 0.012

===================

4) http://162.55.220.72:5005/get_test_user
req.
POST
age: int
salary: int
name: str
auth_token

Resp.
{'name': name,
  'age':age,
  'salary': salary,
  'family':{'children':[['Alex', 24],['Kate', 12]],
  'u_salary_1.5_year': salary * 4}
   }

Tests:
Exercise ***
0) Learn how Response Assertion works.
1) Make an Assertion to check status code 200
2) Make an Assertion to check 'salary': salary
