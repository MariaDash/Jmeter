# Jmeter Sniffing
## Creating Sniffing to the whole website
1. Right mouse click on `Test Plan` --> `Add` --> `None-test elements` --> `HTTP(S) Test script Recorder` 
2. Right mouse click on `Test Plan` --> `Add` -->`Test Fragment` --> `Test Fragment`
3. Right mouse click on `Test Fragment` --> `Add` --> `Logic Controller --> `Recording Controller`
4. In  `HTTP(S) Test script Recorder` push `Start` button.
5. Allow access(on Windows)
## Creating a certificate:
+ Opened Creating certificate banner --> OK
+ Stop Recording controller
+ Look if system folder Jmeter for the certificate click on it   --> install certificate --> current user -->next -->browse--> trust root  --> finish --> Security warning--> OK
+ Then click on certificate again   --> install certificate --> local machine --> yes --> place --> browse --> trust root --> finish.
## Go to Firefox browser
Go to Settings --> General --> Network Settings --> Settings ( open it) --> click Radiobutton Manual Proxy Configuration Check for `local host` and port `8888` written there. Put a tick at Also use for HTTPS  --> OK.

Go to Privacy & Security --> Certificates --> View Certificates--> lokk for `Authorities` --> import --> import Jmeter certificate from the folder --> Trust, trust two times check in checkboxes --> OK.
## 
