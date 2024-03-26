goto aws
create a free tier account.
sign into console as root user
add MFA for root user (one user with complete access)
goto iam -> users -> add user
name: itadmin
check : provide access to the AWS managment console
under the user type:
    select: i want to create an IAM user
    keep auto generated password
    check for user must create password at next login
click next

By default this user don't have any permission , so we need to set up some policies for the user.

click on attach policy directly
select administrator access then go next.
click on create user and download the csv file.
click on return to user list
set MFA for the user.
click on the user go to security credentials scroll down look for assign mfa and follow the process.

### Setting up billing Alarm using the cloud watch ###
go to billing dashboard
go to billing prefrences
enable 
    Invoice delivery preferences
    Recieve AWS free tier alerts
    Receive CloudWatch billing alerts
update and click on the aws logo

Now search for the service  "Cloudwatch" in the search bar, click on it.
Cloudwatch is a aws monitoring service.

now make sure you're in the north vergenia region
click on alarms
all alarms
slect metrics  with filter name space = AWS/Billing
    Total Estimated Charge
    select usd and click on select metric
    define the threshold value say like 5 click next
    click on crate new topic give name and email to recive notifications. click next
    give the alarm name 
    Create the alarm

### Creating public certificate for the domain ###
Go to ACM(Amazon Certificate Manager)
Click on request a certificate
Domain : www.example.com (replace with your own domain)
Validation method : DNS
DNS : add the CNAME record provided by acm to your dns server.
wait until the status of the certificate turns green.


