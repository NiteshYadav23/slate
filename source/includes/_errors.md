# Errors

<aside class="notice">This error section is stored in a separate file in `includes/_errors.md`. Slate allows you to optionally separate out your docs into many files...just save them to the `includes` folder and add them to the top of your `index.md`'s frontmatter. Files are included in the order listed.</aside>

The API uses the following error codes:


Error Code | Meaning | API
---------- | ------- | -----
400 | Bad Request -- Your request sucks. | Common for All
401 | Unauthorized -- Your API key is wrong. | Common for All
404 | Not Found -- The specified kitten could not be found. | Common for All
405 | Method Not Allowed -- You tried to access with an invalid method. | Common for All
1004 | Email Id is missing or not specified | http://localhost:8080/DoctorOnDemand/api/auth/signup
 | Invalid email id or not specified
 | Password is missing or not specified
 | Role is missing or not specified
 | First Name is missing or not specified
 | Last Name is missing or not specified
 | City is missing or not specified
 | Pincode is missing or not specified
 | About Me is missing or not specified
 | Id should be null on signup
 | Email Id is missing or not specified | http://localhost:8080/DoctorOnDemand/api/auth/login
 | Invalid email id or not specified
 | Password is missing or not specified
 | Invalid email id or not specified | http://localhost:8080/DoctorOnDemand/api/patient/user/familyMember
 | Parent user relation is missing or not specified
 | Role is missing or not specified
 | First Name is missing or not specified
 | Last Name is missing or not specified
 | City is missing or not specified
 | State is missing or not specified
 | Country is missing or not specified
 | About Me is missing or not specified
 | Invalid email id or not specified
 | Phone number is missing or not specified
1012 | ROLE_VALIDATION_FOR_SIGNUP_ERROR_MSG
 | Invalid email/password | http://localhost:8080/DoctorOnDemand/api/auth/login
 | Invalid user | http://localhost:8080/DoctorOnDemand/api/auth/logout
 | Invalid user | http://localhost:8080/DoctorOnDemand/api/auth/forgotpassword
 | | http://localhost:8080/DoctorOnDemand/api/auth/changeforgotpassword
 | Pharmacy name is missing | http://localhost:8080/DoctorOnDemand/api/patient/pharmacy
 | Appointment id is not available | http://localhost:8080/DoctorOnDemand/api/patient/appointment/cancel/{appointmentId}
 | | http://localhost:8080/DoctorOnDemand/api/patient/appointment/reschedule/{AppointmentID}
1002 | Invalid Credentials
 

