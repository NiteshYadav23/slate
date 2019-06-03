---
title: EyeCareLive API Docs

language_tabs: # must be one of https://git.io/vQNgJ
  - shell: cURL
 

toc_footers:
 

includes:
  - existingpatient
  - patientdashboard
  - videovisits
  - visiontest
  - appointmentrelated
  - scheduleappointment
  - finddoctor
  - patientuserprofile
  - callingnotification
  - treatmentplan
  - messaging
  - apidocinto
  - docathentication
  - docprofile
  - myappointments
  - pendingappointments
  - patientinfobyapp
  - manageschedule
  - doctormessaging
  - errors

search: true
---

# Patient API's Introduction

Patient is the main user of the Eyecarelive mobile app. Eyecarelive app is designed to guide the users to use the app for appropriate conditions only. There are four modules currently supported in the app. Each module addresses a specific type of a virtual visit and is backed by a self-guiding questionnaire to collect relevant information for the doctors. The modules in current release of the app are:

*  General consultation - Generic and non-urgent conditions such as garden variety pink eye or a quick question about trivial condition

* Dry eye visit - Patients take a validated SPEEDTM test to self-evaluate their dry eye condition. Doctors recommend patients to use the app for Dry eye test during their in-office visit. Dry eye test series can be tracked by the patients and the doctors by using the SPEED test scores.  
* Contact Lens consultation - Patients can use the app related to contact lens questions, concerns or follow-up with their doctors. Contact lens module is designed to collect subjective data from the patient which allows doctors to evaluate seriousness of their condition

#Patient Sign Up

## New User

```shell
curl -k -i -H "Content-Type: application/json" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/auth/signup/v3" -X POST -d '{"email":"patientuser1@eyecarelive.com","password":"demo1234","aboutMe":{"firstName":"Demo","lastName":"User"},"role":{"id":"551ad2a4e4b0b59ff0ccecc9","name":"patient"}}'
 
```
> The above command returns JSON structured like this:

```json
{
  "id": "5ceed13cf893f45b5812b8e1",
  "email": "patientuser1@eyecarelive.com",
  "pharmacyName": null,
  "pharmacyAddress": null,
  "aboutMe": {
    "id": "5ceed13cf893f45b5812b8de",
    "firstName": "Demo",
    "lastName": "User",
    "birthDate": "",
    "address": "",
    "city": "",
    "country": "",
    "pincode": "",
    "gender": null,
    "languagesSpeak": null,
    "additionalInfo": null,
    "state": "",
    "lat": null,
    "lang": null
  },
  "contactInfo": null,
  "patientInfo": null,
  "doctorInfo": null,
  "role": {
    "id": "551ad2a4e4b0b59ff0ccecc9",
    "name": "patient"
  },
  "timezone": {
    "id": "55f283b4e4b029528c27d0c5",
    "timezone": "Asia/Kolkata",
    "displayName": "India Standard Time"
  },
  "createdAt": "2019-05-29 11:36 AM PDT",
  "forgotPasswordToken": null,
  "familyMembers": null,
  "parentUser": null,
  "parentUserRelation": null,
  "password": null,
  "rating": null,
  "preferredPharmacies": null,
  "oldPassword": null,
  "loginStatus": null,
  "stripeCustId": null,
  "profileImagePath": null,
  "isReferredDoctor": null,
  "randomtoken": "BThd5P",
  "isEmailVerified": false,
  "preferredDoctors": null,
  "isAcceptTC": false,
  "insurenceCards": null,
  "notificationSettings": {
    "id": "5ceed13cf893f45b5812b8df",
    "email": true,
    "push": true,
    "sms": true,
    "sendReminderForMedicine": true,
    "addTestreport": true,
    "sentMessage": true,
    "addTreatmentPlan": true,
    "sendReminderForEyeTest": true
  },
  "clinics": null,
  "passCode": null,
  "emrId": null,
  "ssnId": null,
  "clinicInfo": null,
  "ref": null,
  "docOrg": null,
  "doctorsOrg": null,
  "twilioAccessToken": null,
  "bucket": null,
  "repoSub": false,
  "badge": null,
  "preferredEclClinics": null,
  "eclClinicId": null,
  "profileColor": null,
  "addedByCpm": false,
  "activated": true,
  "invited": false,
  "validated": true,
  "pilotDoc": false,
  "managedUser": false
}
```
> Make sure to replace `meowmeowmeow` with your API key.

Create new user with email address and password. This user is referred as Primary user of the app. Eyecarelive supports two roles of users - Patients and Doctors. When creating a new user, Role option must be specified. For creating a patient user, a fixed id# is required to be specified in the API

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/auth/signup/v3
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Email | User’s Email address | String | Required
Password | User’s Password | String | Required
  | **About Me** |   |
FirstName | User’s First Name | String | Required
LastName | User’s Last Name | String | Required
 | **Role** | |
ID | Role (ID) Always use “551ad2a4e4b0b59ff0ccecc9” | Integer | Required
Name | Role Name Always Use “patient” | String | Required
 
### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID | User id# | Integer
Email | User Email address | String
Preferred Pharmacy [{}] | Preferred Pharmacy | String
profileImagePath | Profile photo URL | String
About Me :[{}] | About me info for the user | String
Contact Info:[{}] | Contact person Info | String
Patient Info :[{}] | Patient info | String
Time zone | Time zone | String
Created At:[{}] | Date and Time Created at | String


<aside class="success">
Patient is signed up successfully!
</aside>



# Authentication

User authentication is implemented by email address and password

## Login - Login User - Logs the user in the app

```shell
curl -i -H "Content-Type: application/json" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/auth/login" -X POST -d '{"email" : "patientuser1@eyecarelive.com","password" : "demo1234"}'
```
> The above command returns JSON structured like this:

```json
{
  "id": "5ceed501f893f45b5812b912",
  "userId": "5ceed13cf893f45b5812b8e1",
  "token": "patientuser1@eyecarelive.com:patient:1561747969818:99d07cac156d195ff6a5900f29a7a9b8",
  "dateTime": "2019-05-29 11:52 AM PDT",
  "lastActiveTime": "2019-05-29 11:52 AM PDT"
}
```
### HTTP Request

`POST http://localhost:8080/DoctorOnDemand/api/auth/login
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Email | Patient’s Email address | String | Required
Password | Patient’s Password | String | Required

### Response

Parameter |  Description | Type 
--------- | ------------ | ---- 
ID | Internal system id#. Deprecated | Integer 
USER ID | User ID of Patient | Integer
TOKEN | Authentication Token | String
Date Time | User account created date and time | String

<aside class="success">
 Correct Email and Password leads to successful login!
</aside>

## Logout - User logout - Logs the user out of the patient app

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561747969818:99d07cac156d195ff6a5900f29a7a9b8" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/auth/logout"  -X POST
```
> The above command returns JSON structured like this:

```json
{"success":true}
```
### HTTP Request

`POST http://localhost:8080/DoctorOnDemand/api/auth/logout
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
ID | User’s ID | Integer | Required
Token | User’s authentication token | Integer | Required


### Response

Parameter |  Description | Type
--------- | ------------ | ----
Success | Logout successful True OR False | String

<aside class="notice">
ID and Token are must to be successfully logged out!
</aside>

