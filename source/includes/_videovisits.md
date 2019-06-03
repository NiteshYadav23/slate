# Create Appointment 


## Start New Consultation (Choose Doctor/Clinic, Patient & Payment)


```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/startConsultation/v3"
```
> The above command returns JSON structured like this:

```json
{
  "pendingAppointment": 0,
  "savedAppointment": 0,
  "followupAppointment": null,
  "treatmentPlanFlag": false,
  "testReportFlag": false,
  "savedAppointmentList": null,
  "prefferedDoctors": [
    {
      "id": "56fb7614e4b0d3123cea4925",
      "firstName": "Dr. John",
      "lastName": "Gelles",
      "profession": "Ophthalmologist",
      "profileImagePath": "https://s3.amazonaws.com/deveclprofimg/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/imgDefault.png",
      "paymentOptions": [
        "insurancepaid",
        "alreadypaid"
      ]
    },
    {
      "id": "56fbd63de4b0777c5a04f540",
      "firstName": "Dr. Moshe",
      "lastName": "Mendelson",
      "profession": "Ophthalmologist",
      "profileImagePath": null,
      "paymentOptions": null
    }
  ],
  "prefferedEclClinicBeans": [],
  "userId": "5ceed13cf893f45b5812b8e1",
  "familyMemberFlag": false,
  "messageCount": 0,
  "familyMembers": [
    {
      "id": "5cef956ef893f467ffa9ffcc",
      "email": "ddJdgVqM@eyecarelive.com",
      "firstName": "Slate",
      "lastName": "Member",
      "profileImagePath": null
    }
  ],
  "pendingTestAppointments": null
}
```

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/appointment/startConsultation/v3
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL for  | This API to get the response so need to use payload | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
pendingAppointment |Pending appointment count | String
savedAppointment | Save appointment  | String
followupAppointment | Follow up for appointment. | String
treatmentPlanFlag | Treatment plan by doctor | String
testReportFlag | Test reported by doctor’s | String
savedAppointmentList | Saved appointment data | String
prefferedDoctors | Preferred doctor ID | String
prefferedEclClinicBeans | Preferred clinic ID | String
userId | Patient’s user ID | Integer
familyMemberFlag | Deprecated | String
messageCount | Message count for unread | String
familyMembers[{}] | This will return the al family member details | String
pendingTestAppointments:[{}] | Eye tests recommendation  | String

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Dry Eye Consultation (Create an appointment with Chief complaint and Photos, Videos)


```shell
 curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X POST "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/doctor/createVisit/v3" -d '{"doctor":{"id":"56fb7614e4b0d3123cea4925"},"patient":null,"visitPurpose":"dryeye","diseaseImageFilePath":null,"symtons":"Dry Eye","paymentMode":"alreadypaid","questionaire":null,"chiefCompliant":"Testing Cheif","speciality":{"id":"55b7802be4b0b393bf91678e","questionnaire":null,"report":null},"visitType":"offline"}'
```

> The above command returns JSON structured like this:

```json
{
  "id": "5cf50de1f893f42a2c442349",
  "startDate": "2019-06-03 05:09 AM PDT",
  "endDate": "2019-06-03 05:24 AM PDT",
  "doctor": {
    "id": "56fb7614e4b0d3123cea4925",
    "email": "nitesh.yadav@cupertinosoft.com",
    "pharmacyName": null,
    "pharmacyAddress": null,
    "aboutMe": {
      "id": "56fb7614e4b0d3123cea4923",
      "firstName": "Dr. John",
      "lastName": "Gelles",
      "birthDate": "xCbUo9+vCO6W+uI8luz3YA==",
      "address": "8L10iLEjsRBVkFaI1gu4bw==",
      "city": "8L10iLEjsRBVkFaI1gu4bw==",
      "country": "rwq24J1FnEhqovLa/bo5uQ==",
      "pincode": "+ffKFHCfLQG2vGeutdG6BQ==",
      "gender": "male",
      "languagesSpeak": [
        "English",
        "",
        ""
      ],
      "additionalInfo": "Hi I plays cricket",
      "state": "tdK26+Dp5ks9TH9wFlmgDA==",
      "lat": null,
      "lang": null
    },
    "contactInfo": {
      "id": "56fb7614e4b0d3123cea4924",
      "email": "nakulypatil@gmail.com",
      "phone": "Hj+M0AnqV5zonFbsdcSXUw==",
      "smsNotification": true,
      "countryCode": "+376",
      "country": "USA",
      "emlNt": true
    },
    "patientInfo": null,
    "doctorInfo": {
      "id": "56fb7614e4b0d3123cea4925",
      "educationList": [
        {
          "id": "5cd16094f893f460b09abd74",
          "degree": "MBBS(MD)",
          "university": "Oxford",
          "yearOfPasssing": "2018"
        }
      ],
      "hospitalAttachedWithList": [
        {
          "id": "5cd16cb7f893f460b09abeed",
          "name": "eyecarelivedemo1",
          "city": "NewYork",
          "country": "USA"
        }
      ],
      "awardsReceivedList": [
        {
          "id": "5ce40145f893f43cc2a09260",
          "name": "Test",
          "description": "demo",
          "date": "May 21, 2019"
        }
      ],
      "specialities": [
        {
          "id": "55b78065e4b0b393bf91678f",
          "name": "general physician",
          "questionnaire": null
        }
      ],
      "licencedState": [
        {
          "id": "5665a2cb9a87399fa0b9ba34",
          "state": "AK"
        },
        {
          "id": "5665a2cb9a87399fa0b9ba35",
          "state": "AZ"
        },
        {
          "id": "5665a2cb9a87399fa0b9ba36",
          "state": "AR"
        }
      ],
      "registrationNumber": "44444444",
      "whyCoolDoctors": null,
      "bio": "Bio testingiii",
      "profession": "Ophthalmologist",
      "availabilityTimeZone": "Asia/Kabul",
      "npi": "1234",
      "availabilityStatus": "On",
      "availabilityMsg": "",
      "passwardChanged": false,
      "consultationFees": null,
      "paymentOptions": null,
      "appCountEmail": false,
      "monthlyCharge": false
    },
    "role": {
      "id": "551ad2ffe4b0b59ff0cceccb",
      "name": "doctor"
    },
    "timezone": {
      "id": "55f283b4e4b029528c27d0c5",
      "timezone": "Asia/Kolkata",
      "displayName": "India Standard Time"
    },
    "createdAt": "2016-03-29 11:45 PM PDT",
    "forgotPasswordToken": "6466",
    "familyMembers": null,
    "parentUser": null,
    "parentUserRelation": null,
    "password": null,
    "rating": null,
    "preferredPharmacies": null,
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": "W2iBDJ6LU434JDk4LCyUdqpe2ooWTqPdMvxS8yYrpjg=",
    "profileImagePath": "https://s3.amazonaws.com/deveclprofimg/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/imgDefault.png",
    "isReferredDoctor": null,
    "randomtoken": "esnckN",
    "isEmailVerified": false,
    "preferredDoctors": [
      "59a6456fe4b0be451171721c",
      "59a7c9a5e4b0be4511718cb8"
    ],
    "isAcceptTC": true,
    "insurenceCards": null,
    "notificationSettings": null,
    "clinics": [
      "58f9d4a7e4b07023de8c0d64"
    ],
    "passCode": null,
    "emrId": null,
    "ssnId": null,
    "clinicInfo": null,
    "ref": null,
    "docOrg": null,
    "doctorsOrg": {
      "id": "59cb5445e4b0fa09b42591b7",
      "orgName": "Paragon"
    },
    "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlIiwiZXhwIjoxNTU5NTU4MDg0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NWNlYTZkOThmODkzZjQwYTVmMDM5NWIxIn19LCJqdGkiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlLTE1NTk1NTQ0MzIiLCJzdWIiOiJBQ2M5MGJmNjdhODk0YjA0YjA2NTdkMjJkN2FlOTQ5ZDk3In0.TEVWwtIrp5WPOBfSUgA1cieTPxTkhzK_2WsdZkTCkPE",
    "bucket": null,
    "repoSub": false,
    "badge": null,
    "preferredEclClinics": null,
    "eclClinicId": null,
    "profileColor": null,
    "activated": true,
    "invited": false,
    "validated": true,
    "pilotDoc": true,
    "managedUser": false,
    "addedByCpm": false
  },
  "patient": {
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
    "forgotPasswordToken": "7099",
    "familyMembers": [
      {
        "id": "5cef956ef893f467ffa9ffcc",
        "email": "ddJdgVqM@eyecarelive.com",
        "pharmacyName": null,
        "pharmacyAddress": null,
        "aboutMe": {
          "id": "5cef956ef893f467ffa9ffc9",
          "firstName": "Slate",
          "lastName": "Member",
          "birthDate": "",
          "address": "qbNrHbKolNuq9+DQCMrbNw==",
          "city": "28L8jdmZdw/TOE19cYNfyg==",
          "country": "eGcNxOZVnF4jlkABhqaIAQ==",
          "pincode": "Zf6QZAhj9x3iULdEWv9pfA==",
          "gender": "male",
          "languagesSpeak": null,
          "additionalInfo": null,
          "state": "wPCNRzWVjd+MXrn0+dB4Cg==",
          "lat": null,
          "lang": null
        },
        "contactInfo": {
          "id": "5cef956ef893f467ffa9ffca",
          "email": "patientuser1@eyecarelive.com",
          "phone": "X025s2zeUri6K/6HA21+UA==",
          "smsNotification": false,
          "countryCode": null,
          "country": null,
          "emlNt": false
        },
        "patientInfo": null,
        "doctorInfo": null,
        "role": {
          "id": "551ad2a4e4b0b59ff0ccecc9",
          "name": "patient"
        },
        "timezone": null,
        "createdAt": "2019-05-30 01:33 AM PDT",
        "forgotPasswordToken": null,
        "familyMembers": null,
        "parentUser": null,
        "parentUserRelation": "brother",
        "password": null,
        "rating": null,
        "preferredPharmacies": null,
        "oldPassword": null,
        "loginStatus": null,
        "stripeCustId": null,
        "profileImagePath": null,
        "isReferredDoctor": null,
        "randomtoken": null,
        "isEmailVerified": false,
        "preferredDoctors": null,
        "isAcceptTC": false,
        "insurenceCards": null,
        "notificationSettings": null,
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
        "activated": true,
        "invited": false,
        "validated": true,
        "pilotDoc": false,
        "managedUser": true,
        "addedByCpm": false
      }
    ],
    "parentUser": null,
    "parentUserRelation": null,
    "password": null,
    "rating": null,
    "preferredPharmacies": [
      {
        "id": "5cefff05f893f4052b1271ec",
        "name": "Mediplus store",
        "address": "hinjewadi phase-1",
        "email": "niteshy2391@gmail.com",
        "city": "pune",
        "state": "Maharashtra",
        "country": null,
        "zipCode": "411007",
        "phoneNumber": "9423505079",
        "validated": false
      }
    ],
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": "6yZMnuPs8a4fXTM8EgbceG9D9mDKC7Rs7SN+oIXZTdQ=",
    "profileImagePath": null,
    "isReferredDoctor": null,
    "randomtoken": "BThd5P",
    "isEmailVerified": false,
    "preferredDoctors": [
      "56fb7614e4b0d3123cea4925",
      "56fbd63de4b0777c5a04f540"
    ],
    "isAcceptTC": false,
    "insurenceCards": null,
    "notificationSettings": {
      "id": "5ceed13cf893f45b5812b8df",
      "email": true,
      "sendReminderForMedicine": true,
      "addTestreport": true,
      "sentMessage": true,
      "addTreatmentPlan": true,
      "sendReminderForEyeTest": true,
      "push": true,
      "sms": true
    },
    "clinics": null,
    "passCode": null,
    "emrId": null,
    "ssnId": null,
    "clinicInfo": null,
    "ref": null,
    "docOrg": null,
    "doctorsOrg": null,
    "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlIiwiZXhwIjoxNTU5MjUwNDgwLCJncmFudHMiOnsiaWRlbnRpdHkiOiI1Y2VlZDEzY2Y4OTNmNDViNTgxMmI4ZTEiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NWNlZWQxM2NmODkzZjQ1YjU4MTJiOGUxIn19LCJqdGkiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlLTE1NTkyNDY5NzYiLCJzdWIiOiJBQ2M5MGJmNjdhODk0YjA0YjA2NTdkMjJkN2FlOTQ5ZDk3In0._OzAiloA2trSDKPE4HAhP3WIvjvfWkYbWd_zav_pQpQ",
    "bucket": null,
    "repoSub": false,
    "badge": null,
    "preferredEclClinics": null,
    "eclClinicId": null,
    "profileColor": null,
    "activated": true,
    "invited": false,
    "validated": true,
    "pilotDoc": false,
    "managedUser": false,
    "addedByCpm": false
  },
  "questionaire": null,
  "todos": null,
  "speciality": {
    "id": "55b7802be4b0b393bf91678e",
    "name": null,
    "questionnaire": null
  },
  "createdAt": "2019-06-03 05:09 AM PDT",
  "appointmentPrice": 0,
  "status": "pending",
  "waitId": 0,
  "currentLocationState": null,
  "isReferredDoctorAvailable": null,
  "diseaseImageFilePath": null,
  "contactlenseImageFilePath": null,
  "patientPreferredVisitLanguage": null,
  "symtons": "Dry Eye",
  "createdBy": "5ceed13cf893f45b5812b8e1",
  "paymentStatus": null,
  "visionTest": null,
  "videoVisitPath": null,
  "remark": null,
  "callReceivedStatus": false,
  "files": null,
  "needFollowUp": false,
  "pharmacy": [
    {
      "id": "5cefff05f893f4052b1271ec",
      "name": "Mediplus store",
      "address": "hinjewadi phase-1",
      "email": "niteshy2391@gmail.com",
      "city": "pune",
      "state": "Maharashtra",
      "country": null,
      "zipCode": "411007",
      "phoneNumber": "9423505079",
      "validated": false
    }
  ],
  "visitType": "offline",
  "visitPurpose": "dryeye",
  "availabilityTimeSlot": null,
  "availability": null,
  "lasikSurgery": null,
  "closedOrCanceledAt": null,
  "convertedStartDate": null,
  "medicinePrescriptions": null,
  "eyeTest": null,
  "coverageParam": null,
  "clinic": null,
  "checkinForms": null,
  "paymentMode": "alreadypaid",
  "solutionBottleImage": null,
  "videoMessage": null,
  "eclClinic": null,
  "chiefCompliant": "Testing Cheif",
  "testStatus": null,
  "eyeProblems": null,
  "recomendedTests": {
    "id": "5cf50de1f893f42a2c442348",
    "dryEye": "1",
    "contactLens": "0",
    "visionTest": "1",
    "userId": "5ceed13cf893f45b5812b8e1",
    "createdAt": null
  },
  "callImages": null,
  "codes": null,
  "physicalExam": null,
  "dryEyeTestId": null,
  "contactLensTestId": null,
  "visionTestId": null,
  "clinicVisit": false,
  "cancelled": false,
  "finished": false,
  "inProgress": false,
  "notifiedForPendingVisit": false,
  "reminderSend": false,
  "notifiedForTwoDaysPendingVisit": false,
  "followUp": false,
  "chargeble": false,
  "symtonUpdated": false,
  "eclClinicVisit": false
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Create a request for new visit. User will chose visit type and a doctor and submit answers to series of questions presented for that visit type.

Since this API supports variety of visit types, certain request parameters become mandatory or optional based on the visit type. 

* visitPurpose :

visitPrupose |  Parameter  
------------ |  ----------- 
Dry Eye | dryeye
General Consultation | normalsymtons
Contact Lens visit | contactlens

* availabilityTimeSlot :

availabilityTimeSlot |  Parameter  
------------ |  ----------- 
Send info to doctor | “AvailabilityTimeSlot":null
Book an Appointment | “AvailabilityTimeSlot":{“id”:”Pass ID here as per doctor’s availability”}

* Symtons : 

Symtons |  Parameter  
------------ |  ----------- 
Pass visit name | “Symtons”:Dry Eye
Pass visit name | “Symtons”:Contact Lens
Pass visit name | “Symtons”:General Consult

* visitType :

visitType |  Parameter  
------------ |  ----------- 
Pass visitType | “visitType”:”offline”

* doctor  : 

doctor |  Parameter  
------------ |  ----------- 
doctor | “doctor”:Selected doctor ID

* patient :

patient |  Parameter  
------------ |  ----------- 
patient | “patient”:”offline”



### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/doctor/createVisit/v3
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
  | **Doctor** |   |
doctor | Doctor ID | Integer | Required
visitPurpose | visitPurpose parameter need fixed values, Please check visitPurpose table. | String | Required
diseaseImageFilePath | In this parameter need to pass if user uploading diseaseimages | String | Optional
symtons | In this parameter, need to pass symptoms name like Eye Pain  | String | Required
paymentMode | Payment mode, Credit card, Insurance, AlreadyPaid | String | Required
treatment[{}] | It’s for dry eye | String | Optional
visitType |  offline | String | Required
chiefCompliant |  need to pass Cheif complaint | String | Required
  | **Speciality** |   |
ID | ID of Speciality | String | Required
Appointment | Appointment | String | Optional
availabilityTimeSlot | Availability time should be pass as per doctor avaibility time. | String | Optional

### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | Appointment ID created by database | Integer
Start date | Start date of created | String
End Date | End date of created | String
Doctor | doctor name info | String
Patient | Patient name Info | String
ID | user id# | Integer
Email | User’s Email address | String
Pharmacy Name | Pharmacy name deprecated | String
pharmacy Address | Pharmacy address deprecated | String
profile Image Id | Profile photo ID deprecated | Integer
profile Image Name | Profile photo Name deprecated | .jpg,etc
About Me :[{}] | about me for User’s details | String
Contact Info:[{}] | Contact person Info | String
Patient Info :[{}] | Patient info | String
Doctor Info :[{}] | Doctor info | String
Hospital Attached With List :[{}] | Hospital Attached with list | String
Family History:[{}] | Array of the family history | String
Awards Received List | Awards received list | String
Prescription | Prescription | String
Questionnaire | Questionnaire details | String
TODO | Treatment plan details | String
Specialities | Specialities Details | String
Appointment | Appointment details | String
Report | Report | String
Created At :[{}] | Array of the created at | String




`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Update Dry Eye Test (update the dry eye test with previous appointment ID)


```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X POST "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/doctor/updateVisit/v3/5cf50de1f893f42a2c442349" -d '{"questionaire":{"questions":null,"symptoms":[{"question":"Dryness, Grittiness or Scratchiness: At this Visit","answerType":"String","answer":"Yes","param1":null,"param2":null,"param3":null},{"question":"Dryness, Grittiness or Scratchiness: Within past 72 hours","answerType":"String","answer":"No","param1":null,"param2":null,"param3":null},{"question":"Dryness, Grittiness or Scratchiness: Within past 3 mos","answerType":"String","answer":"No","param1":null,"param2":null,"param3":null},{"question":"Soreness or Irritation: At this Visit","answerType":"String","answer":"No","param1":null,"param2":null,"param3":null},{"question":"Soreness or Irritation: Within past 72 hours","answerType":"String","answer":"Yes","param1":null,"param2":null,"param3":null},{"question":"Soreness or Irritation: Within past 3 mos","answerType":"String","answer":"No","param1":null,"param2":null,"param3":null},{"question":"Burning or Watering: At this Visit","answerType":"String","answer":"No","param1":null,"param2":null,"param3":null},{"question":"Burning or Watering: Within past 72 hours","answerType":"String","answer":"No","param1":null,"param2":null,"param3":null},{"question":"Burning or Watering: Within past 3 mos","answerType":"String","answer":"Yes","param1":null,"param2":null,"param3":null},{"question":"Eye Fatigue: At this Visit","answerType":"String","answer":"No","param1":null,"param2":null,"param3":null},{"question":"Eye Fatigue: Within past 72 hours","answerType":"String","answer":"No","param1":null,"param2":null,"param3":null},{"id":"5cf50ea9f893f42a2c4423ad","question":"Eye Fatigue: Within past 3 mos","answerType":"String","answer":"No","param1":null,"param2":null,"param3":null}],"frequency":[{"question":"Dryness, Grittiness or Scratchiness","answerType":"String","answer":"1","param1":null,"param2":null,"param3":null},{"question":"Soreness or Irritation","answerType":"String","answer":"1","param1":null,"param2":null,"param3":null},{"question":"Burning or Watering","answerType":"String","answer":"2","param1":null,"param2":null,"param3":null},{"question":"Eye Fatigue","answerType":"String","answer":"0","param1":null,"param2":null,"param3":null}],"severity":[{"question":"Dryness, Grittiness or Scratchiness","answerType":"String","answer":"1","param1":null,"param2":null,"param3":null},{"question":"Soreness or Irritation","answerType":"String","answer":"2","param1":null,"param2":null,"param3":null},{"question":"Burning or Watering","answerType":"String","answer":"2","param1":null,"param2":null,"param3":null},{"question":"Eye Fatigue","answerType":"String","answer":"1","param1":null,"param2":null,"param3":null}],"treatment":[{"question":"Medication","answerType":"String","answer":"yes","param1":null,"param2":null,"param3":null},{"id":"5cf50ea9f893f42a2c4423b7","question":"Supplements","answerType":"String","answer":"the","param1":null,"param2":null,"param3":null},{"question":"WarmCompresses","answerType":"String","answer":"Yes","param1":null,"param2":null,"param3":null},{"question":"EyeDrop","answerType":"String","answer":"Restasis","param1":null,"param2":null,"param3":null}],"appointment":null,"lasikQuestionnaire":null,"contactLenseQuestions":null},"todos":null,"speciality":{"name":"general physician","questionnaire":null}}'
```

> The above command returns JSON structured like this:

```json
{
  "id": "5cf50de1f893f42a2c442349",
  "startDate": "2019-06-03 05:09 AM PDT",
  "endDate": "2019-06-03 05:24 AM PDT",
  "doctor": {
    "id": "56fb7614e4b0d3123cea4925",
    "email": "nitesh.yadav@cupertinosoft.com",
    "pharmacyName": null,
    "pharmacyAddress": null,
    "aboutMe": {
      "id": "56fb7614e4b0d3123cea4923",
      "firstName": "Dr. John",
      "lastName": "Gelles",
      "birthDate": "xCbUo9+vCO6W+uI8luz3YA==",
      "address": "8L10iLEjsRBVkFaI1gu4bw==",
      "city": "8L10iLEjsRBVkFaI1gu4bw==",
      "country": "rwq24J1FnEhqovLa/bo5uQ==",
      "pincode": "+ffKFHCfLQG2vGeutdG6BQ==",
      "gender": "male",
      "languagesSpeak": [
        "English",
        "",
        ""
      ],
      "additionalInfo": "Hi I plays cricket",
      "state": "tdK26+Dp5ks9TH9wFlmgDA==",
      "lat": null,
      "lang": null
    },
    "contactInfo": {
      "id": "56fb7614e4b0d3123cea4924",
      "email": "nakulypatil@gmail.com",
      "phone": "Hj+M0AnqV5zonFbsdcSXUw==",
      "smsNotification": true,
      "countryCode": "+376",
      "country": "USA",
      "emlNt": true
    },
    "patientInfo": null,
    "doctorInfo": {
      "id": "56fb7614e4b0d3123cea4925",
      "educationList": [
        {
          "id": "5cd16094f893f460b09abd74",
          "degree": "MBBS(MD)",
          "university": "Oxford",
          "yearOfPasssing": "2018"
        }
      ],
      "hospitalAttachedWithList": [
        {
          "id": "5cd16cb7f893f460b09abeed",
          "name": "eyecarelivedemo1",
          "city": "NewYork",
          "country": "USA"
        }
      ],
      "awardsReceivedList": [
        {
          "id": "5ce40145f893f43cc2a09260",
          "name": "Test",
          "description": "demo",
          "date": "May 21, 2019"
        }
      ],
      "specialities": [
        {
          "id": "55b78065e4b0b393bf91678f",
          "name": "general physician",
          "questionnaire": null
        }
      ],
      "licencedState": [
        {
          "id": "5665a2cb9a87399fa0b9ba34",
          "state": "AK"
        },
        {
          "id": "5665a2cb9a87399fa0b9ba35",
          "state": "AZ"
        },
        {
          "id": "5665a2cb9a87399fa0b9ba36",
          "state": "AR"
        }
      ],
      "registrationNumber": "44444444",
      "whyCoolDoctors": null,
      "bio": "Bio testingiii",
      "profession": "Ophthalmologist",
      "availabilityTimeZone": "Asia/Kabul",
      "npi": "1234",
      "availabilityStatus": "On",
      "availabilityMsg": "",
      "passwardChanged": false,
      "consultationFees": null,
      "paymentOptions": null,
      "appCountEmail": false,
      "monthlyCharge": false
    },
    "role": {
      "id": "551ad2ffe4b0b59ff0cceccb",
      "name": "doctor"
    },
    "timezone": {
      "id": "55f283b4e4b029528c27d0c5",
      "timezone": "Asia/Kolkata",
      "displayName": "India Standard Time"
    },
    "createdAt": "2016-03-29 11:45 PM PDT",
    "forgotPasswordToken": "6466",
    "familyMembers": null,
    "parentUser": null,
    "parentUserRelation": null,
    "password": null,
    "rating": null,
    "preferredPharmacies": null,
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": "W2iBDJ6LU434JDk4LCyUdqpe2ooWTqPdMvxS8yYrpjg=",
    "profileImagePath": "https://s3.amazonaws.com/deveclprofimg/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/imgDefault.png",
    "isReferredDoctor": null,
    "randomtoken": "esnckN",
    "isEmailVerified": false,
    "preferredDoctors": [
      "59a6456fe4b0be451171721c",
      "59a7c9a5e4b0be4511718cb8"
    ],
    "isAcceptTC": true,
    "insurenceCards": null,
    "notificationSettings": null,
    "clinics": [
      "58f9d4a7e4b07023de8c0d64"
    ],
    "passCode": null,
    "emrId": null,
    "ssnId": null,
    "clinicInfo": null,
    "ref": null,
    "docOrg": null,
    "doctorsOrg": {
      "id": "59cb5445e4b0fa09b42591b7",
      "orgName": "Paragon"
    },
    "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlIiwiZXhwIjoxNTU5NTU4MDg0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NWNlYTZkOThmODkzZjQwYTVmMDM5NWIxIn19LCJqdGkiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlLTE1NTk1NTQ0MzIiLCJzdWIiOiJBQ2M5MGJmNjdhODk0YjA0YjA2NTdkMjJkN2FlOTQ5ZDk3In0.TEVWwtIrp5WPOBfSUgA1cieTPxTkhzK_2WsdZkTCkPE",
    "bucket": null,
    "repoSub": false,
    "badge": null,
    "preferredEclClinics": null,
    "eclClinicId": null,
    "profileColor": null,
    "activated": true,
    "invited": false,
    "validated": true,
    "pilotDoc": true,
    "managedUser": false,
    "addedByCpm": false
  },
  "patient": {
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
    "forgotPasswordToken": "7099",
    "familyMembers": [
      {
        "id": "5cef956ef893f467ffa9ffcc",
        "email": "ddJdgVqM@eyecarelive.com",
        "pharmacyName": null,
        "pharmacyAddress": null,
        "aboutMe": {
          "id": "5cef956ef893f467ffa9ffc9",
          "firstName": "Slate",
          "lastName": "Member",
          "birthDate": "",
          "address": "qbNrHbKolNuq9+DQCMrbNw==",
          "city": "28L8jdmZdw/TOE19cYNfyg==",
          "country": "eGcNxOZVnF4jlkABhqaIAQ==",
          "pincode": "Zf6QZAhj9x3iULdEWv9pfA==",
          "gender": "male",
          "languagesSpeak": null,
          "additionalInfo": null,
          "state": "wPCNRzWVjd+MXrn0+dB4Cg==",
          "lat": null,
          "lang": null
        },
        "contactInfo": {
          "id": "5cef956ef893f467ffa9ffca",
          "email": "patientuser1@eyecarelive.com",
          "phone": "X025s2zeUri6K/6HA21+UA==",
          "smsNotification": false,
          "countryCode": null,
          "country": null,
          "emlNt": false
        },
        "patientInfo": null,
        "doctorInfo": null,
        "role": {
          "id": "551ad2a4e4b0b59ff0ccecc9",
          "name": "patient"
        },
        "timezone": null,
        "createdAt": "2019-05-30 01:33 AM PDT",
        "forgotPasswordToken": null,
        "familyMembers": null,
        "parentUser": null,
        "parentUserRelation": "brother",
        "password": null,
        "rating": null,
        "preferredPharmacies": null,
        "oldPassword": null,
        "loginStatus": null,
        "stripeCustId": null,
        "profileImagePath": null,
        "isReferredDoctor": null,
        "randomtoken": null,
        "isEmailVerified": false,
        "preferredDoctors": null,
        "isAcceptTC": false,
        "insurenceCards": null,
        "notificationSettings": null,
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
        "activated": true,
        "invited": false,
        "validated": true,
        "pilotDoc": false,
        "managedUser": true,
        "addedByCpm": false
      }
    ],
    "parentUser": null,
    "parentUserRelation": null,
    "password": null,
    "rating": null,
    "preferredPharmacies": [
      {
        "id": "5cefff05f893f4052b1271ec",
        "name": "Mediplus store",
        "address": "hinjewadi phase-1",
        "email": "niteshy2391@gmail.com",
        "city": "pune",
        "state": "Maharashtra",
        "country": null,
        "zipCode": "411007",
        "phoneNumber": "9423505079",
        "validated": false
      }
    ],
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": "6yZMnuPs8a4fXTM8EgbceG9D9mDKC7Rs7SN+oIXZTdQ=",
    "profileImagePath": null,
    "isReferredDoctor": null,
    "randomtoken": "BThd5P",
    "isEmailVerified": false,
    "preferredDoctors": [
      "56fb7614e4b0d3123cea4925",
      "56fbd63de4b0777c5a04f540"
    ],
    "isAcceptTC": false,
    "insurenceCards": null,
    "notificationSettings": {
      "id": "5ceed13cf893f45b5812b8df",
      "email": true,
      "sendReminderForMedicine": true,
      "addTestreport": true,
      "sentMessage": true,
      "addTreatmentPlan": true,
      "sendReminderForEyeTest": true,
      "push": true,
      "sms": true
    },
    "clinics": null,
    "passCode": null,
    "emrId": null,
    "ssnId": null,
    "clinicInfo": null,
    "ref": null,
    "docOrg": null,
    "doctorsOrg": null,
    "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlIiwiZXhwIjoxNTU5MjUwNDgwLCJncmFudHMiOnsiaWRlbnRpdHkiOiI1Y2VlZDEzY2Y4OTNmNDViNTgxMmI4ZTEiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NWNlZWQxM2NmODkzZjQ1YjU4MTJiOGUxIn19LCJqdGkiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlLTE1NTkyNDY5NzYiLCJzdWIiOiJBQ2M5MGJmNjdhODk0YjA0YjA2NTdkMjJkN2FlOTQ5ZDk3In0._OzAiloA2trSDKPE4HAhP3WIvjvfWkYbWd_zav_pQpQ",
    "bucket": null,
    "repoSub": false,
    "badge": null,
    "preferredEclClinics": null,
    "eclClinicId": null,
    "profileColor": null,
    "activated": true,
    "invited": false,
    "validated": true,
    "pilotDoc": false,
    "managedUser": false,
    "addedByCpm": false
  },
  "questionaire": {
    "id": "5cf514cef893f42a2c3e0e1a",
    "questions": null,
    "symptoms": [
      {
        "id": "5cf514cef893f42a2c3e0e04",
        "question": "Dryness, Grittiness or Scratchiness: At this Visit",
        "answerType": "String",
        "answer": "Yes",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e05",
        "question": "Dryness, Grittiness or Scratchiness: Within past 72 hours",
        "answerType": "String",
        "answer": "No",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e06",
        "question": "Dryness, Grittiness or Scratchiness: Within past 3 mos",
        "answerType": "String",
        "answer": "No",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e07",
        "question": "Soreness or Irritation: At this Visit",
        "answerType": "String",
        "answer": "No",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e08",
        "question": "Soreness or Irritation: Within past 72 hours",
        "answerType": "String",
        "answer": "Yes",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e09",
        "question": "Soreness or Irritation: Within past 3 mos",
        "answerType": "String",
        "answer": "No",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e0a",
        "question": "Burning or Watering: At this Visit",
        "answerType": "String",
        "answer": "No",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e0b",
        "question": "Burning or Watering: Within past 72 hours",
        "answerType": "String",
        "answer": "No",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e0c",
        "question": "Burning or Watering: Within past 3 mos",
        "answerType": "String",
        "answer": "Yes",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e0d",
        "question": "Eye Fatigue: At this Visit",
        "answerType": "String",
        "answer": "No",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e0e",
        "question": "Eye Fatigue: Within past 72 hours",
        "answerType": "String",
        "answer": "No",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf50ea9f893f42a2c4423ad",
        "question": "Eye Fatigue: Within past 3 mos",
        "answerType": "String",
        "answer": "No",
        "param1": null,
        "param2": null,
        "param3": null
      }
    ],
    "frequency": [
      {
        "id": "5cf514cef893f42a2c3e0e0f",
        "question": "Dryness, Grittiness or Scratchiness",
        "answerType": "String",
        "answer": "1",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e10",
        "question": "Soreness or Irritation",
        "answerType": "String",
        "answer": "1",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e11",
        "question": "Burning or Watering",
        "answerType": "String",
        "answer": "2",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e12",
        "question": "Eye Fatigue",
        "answerType": "String",
        "answer": "0",
        "param1": null,
        "param2": null,
        "param3": null
      }
    ],
    "severity": [
      {
        "id": "5cf514cef893f42a2c3e0e13",
        "question": "Dryness, Grittiness or Scratchiness",
        "answerType": "String",
        "answer": "1",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e14",
        "question": "Soreness or Irritation",
        "answerType": "String",
        "answer": "2",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e15",
        "question": "Burning or Watering",
        "answerType": "String",
        "answer": "2",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e16",
        "question": "Eye Fatigue",
        "answerType": "String",
        "answer": "1",
        "param1": null,
        "param2": null,
        "param3": null
      }
    ],
    "treatment": [
      {
        "id": "5cf514cef893f42a2c3e0e17",
        "question": "Medication",
        "answerType": "String",
        "answer": "yes",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf50ea9f893f42a2c4423b7",
        "question": "Supplements",
        "answerType": "String",
        "answer": "the",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e18",
        "question": "WarmCompresses",
        "answerType": "String",
        "answer": "Yes",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf514cef893f42a2c3e0e19",
        "question": "EyeDrop",
        "answerType": "String",
        "answer": "Restasis",
        "param1": null,
        "param2": null,
        "param3": null
      }
    ],
    "appointment": null,
    "lasikQuestionnaire": null,
    "contactLenseQuestions": null
  },
  "todos": null,
  "speciality": {
    "id": "55b7802be4b0b393bf91678e",
    "name": "eye care",
    "questionnaire": null
  },
  "createdAt": "2019-06-03 05:09 AM PDT",
  "appointmentPrice": 0,
  "status": "pending",
  "waitId": 0,
  "currentLocationState": null,
  "isReferredDoctorAvailable": null,
  "diseaseImageFilePath": null,
  "contactlenseImageFilePath": null,
  "patientPreferredVisitLanguage": null,
  "symtons": "Dry Eye",
  "createdBy": "5ceed13cf893f45b5812b8e1",
  "paymentStatus": null,
  "visionTest": null,
  "videoVisitPath": null,
  "remark": null,
  "callReceivedStatus": false,
  "files": null,
  "needFollowUp": false,
  "pharmacy": [
    {
      "id": "5cefff05f893f4052b1271ec",
      "name": "Mediplus store",
      "address": "hinjewadi phase-1",
      "email": "niteshy2391@gmail.com",
      "city": "pune",
      "state": "Maharashtra",
      "country": null,
      "zipCode": "411007",
      "phoneNumber": "9423505079",
      "validated": false
    }
  ],
  "visitType": "offline",
  "visitPurpose": "dryeye",
  "availabilityTimeSlot": null,
  "availability": null,
  "lasikSurgery": null,
  "closedOrCanceledAt": null,
  "convertedStartDate": null,
  "medicinePrescriptions": null,
  "eyeTest": null,
  "coverageParam": null,
  "clinic": null,
  "checkinForms": null,
  "paymentMode": "alreadypaid",
  "solutionBottleImage": null,
  "videoMessage": null,
  "eclClinic": null,
  "chiefCompliant": "Testing Cheif",
  "testStatus": null,
  "eyeProblems": null,
  "recomendedTests": {
    "id": "5cf50de1f893f42a2c442348",
    "dryEye": "2",
    "contactLens": "0",
    "visionTest": "1",
    "userId": "5ceed13cf893f45b5812b8e1",
    "createdAt": null
  },
  "callImages": null,
  "codes": null,
  "physicalExam": null,
  "dryEyeTestId": null,
  "contactLensTestId": null,
  "visionTestId": null,
  "clinicVisit": false,
  "cancelled": false,
  "finished": false,
  "inProgress": false,
  "notifiedForPendingVisit": false,
  "reminderSend": false,
  "notifiedForTwoDaysPendingVisit": false,
  "followUp": false,
  "chargeble": false,
  "symtonUpdated": false,
  "eclClinicVisit": false
}
```

> Make sure to replace `X-Auth-Token` with your API key.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/doctor/createVisit/v3
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
  | ** Questionnaire 
     array has  all questions and answers sendt in the visit to the doctor** |   |
questionaire | Questions | String | Required
questions | ID | Integer | Optional
symptoms:[{}] | Questions | String | Required
severity:[{}] | Questions | String | Required
frequency:[{}] | Questions | String | Required
treatment:[{}] | Questions | String | Required
AnswerType | Answer Type | Boolean | Required
Answer | answer (Y/N) | String | Optional

### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | Appointment ID created by database | Integer
Start date | Start date of created | String
End Date | End date of created | String
Doctor | doctor name info | String
Patient | Patient name Info | String
ID | user id# | Integer
Email | User’s Email address | String
Pharmacy Name | Pharmacy name deprecated | String
pharmacy Address | Pharmacy address deprecated | String
profile Image Id | Profile photo ID deprecated | Integer
profile Image Name | Profile photo Name deprecated | .jpg,etc
About Me :[{}] | about me for User’s details | String
Contact Info:[{}] | Contact person Info | String
Patient Info :[{}] | Patient info | String
Doctor Info :[{}] | Doctor info | String
Hospital Attached With List :[{}] | Hospital Attached with list | String
Family History:[{}] | Array of the family history | String
Awards Received List | Awards received list | String
Prescription | Prescription | String
Questionnaire | Questionnaire details | String
TODO | Treatment plan details | String
Specialities | Specialities Details | String
Appointment | Appointment details | String
Report | Report | String
Created At :[{}] | Array of the created at | String




`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Contact Lens Consultation (Create an appointment with Chief complaint and Photos, Videos)

```shell
 curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X POST "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/doctor/createVisit/v3" -d '{"doctor":{"id":"56fb7614e4b0d3123cea4925"},"patient":null,"visitPurpose":"contactlens","diseaseImageFilePath":null,"symtons":"Contact lens","paymentMode":"alreadypaid","questionaire":null,"chiefCompliant":"Testing Cheif","speciality":{"id":"55b7802be4b0b393bf91678e","questionnaire":null,"report":null},"visitType":"offline"}'
```

> The above command returns JSON structured like this:

```json
{
  "id": "5cf51a4df893f42a2c872058",
  "startDate": "2019-06-03 06:02 AM PDT",
  "endDate": "2019-06-03 06:17 AM PDT",
  "doctor": {
    "id": "56fb7614e4b0d3123cea4925",
    "email": "nitesh.yadav@cupertinosoft.com",
    "pharmacyName": null,
    "pharmacyAddress": null,
    "aboutMe": {
      "id": "56fb7614e4b0d3123cea4923",
      "firstName": "Dr. John",
      "lastName": "Gelles",
      "birthDate": "xCbUo9+vCO6W+uI8luz3YA==",
      "address": "8L10iLEjsRBVkFaI1gu4bw==",
      "city": "8L10iLEjsRBVkFaI1gu4bw==",
      "country": "rwq24J1FnEhqovLa/bo5uQ==",
      "pincode": "+ffKFHCfLQG2vGeutdG6BQ==",
      "gender": "male",
      "languagesSpeak": [
        "English",
        "",
        ""
      ],
      "additionalInfo": "Hi I plays cricket",
      "state": "tdK26+Dp5ks9TH9wFlmgDA==",
      "lat": null,
      "lang": null
    },
    "contactInfo": {
      "id": "56fb7614e4b0d3123cea4924",
      "email": "nakulypatil@gmail.com",
      "phone": "Hj+M0AnqV5zonFbsdcSXUw==",
      "smsNotification": true,
      "countryCode": "+376",
      "country": "USA",
      "emlNt": true
    },
    "patientInfo": null,
    "doctorInfo": {
      "id": "56fb7614e4b0d3123cea4925",
      "educationList": [
        {
          "id": "5cd16094f893f460b09abd74",
          "degree": "MBBS(MD)",
          "university": "Oxford",
          "yearOfPasssing": "2018"
        }
      ],
      "hospitalAttachedWithList": [
        {
          "id": "5cd16cb7f893f460b09abeed",
          "name": "eyecarelivedemo1",
          "city": "NewYork",
          "country": "USA"
        }
      ],
      "awardsReceivedList": [
        {
          "id": "5ce40145f893f43cc2a09260",
          "name": "Test",
          "description": "demo",
          "date": "May 21, 2019"
        }
      ],
      "specialities": [
        {
          "id": "55b78065e4b0b393bf91678f",
          "name": "general physician",
          "questionnaire": null
        }
      ],
      "licencedState": [
        {
          "id": "5665a2cb9a87399fa0b9ba34",
          "state": "AK"
        },
        {
          "id": "5665a2cb9a87399fa0b9ba35",
          "state": "AZ"
        },
        {
          "id": "5665a2cb9a87399fa0b9ba36",
          "state": "AR"
        }
      ],
      "registrationNumber": "44444444",
      "whyCoolDoctors": null,
      "bio": "Bio testingiii",
      "profession": "Ophthalmologist",
      "availabilityTimeZone": "Asia/Kabul",
      "npi": "1234",
      "availabilityStatus": "On",
      "availabilityMsg": "",
      "passwardChanged": false,
      "consultationFees": null,
      "paymentOptions": null,
      "appCountEmail": false,
      "monthlyCharge": false
    },
    "role": {
      "id": "551ad2ffe4b0b59ff0cceccb",
      "name": "doctor"
    },
    "timezone": {
      "id": "55f283b4e4b029528c27d0c5",
      "timezone": "Asia/Kolkata",
      "displayName": "India Standard Time"
    },
    "createdAt": "2016-03-29 11:45 PM PDT",
    "forgotPasswordToken": "6466",
    "familyMembers": null,
    "parentUser": null,
    "parentUserRelation": null,
    "password": null,
    "rating": null,
    "preferredPharmacies": null,
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": "W2iBDJ6LU434JDk4LCyUdqpe2ooWTqPdMvxS8yYrpjg=",
    "profileImagePath": "https://s3.amazonaws.com/deveclprofimg/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/imgDefault.png",
    "isReferredDoctor": null,
    "randomtoken": "esnckN",
    "isEmailVerified": false,
    "preferredDoctors": [
      "59a6456fe4b0be451171721c",
      "59a7c9a5e4b0be4511718cb8"
    ],
    "isAcceptTC": true,
    "insurenceCards": null,
    "notificationSettings": null,
    "clinics": [
      "58f9d4a7e4b07023de8c0d64"
    ],
    "passCode": null,
    "emrId": null,
    "ssnId": null,
    "clinicInfo": null,
    "ref": null,
    "docOrg": null,
    "doctorsOrg": {
      "id": "59cb5445e4b0fa09b42591b7",
      "orgName": "Paragon"
    },
    "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlIiwiZXhwIjoxNTU5NTU4MDg0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NWNlYTZkOThmODkzZjQwYTVmMDM5NWIxIn19LCJqdGkiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlLTE1NTk1NTQ0MzIiLCJzdWIiOiJBQ2M5MGJmNjdhODk0YjA0YjA2NTdkMjJkN2FlOTQ5ZDk3In0.TEVWwtIrp5WPOBfSUgA1cieTPxTkhzK_2WsdZkTCkPE",
    "bucket": null,
    "repoSub": false,
    "badge": null,
    "preferredEclClinics": null,
    "eclClinicId": null,
    "profileColor": null,
    "activated": true,
    "invited": false,
    "validated": true,
    "pilotDoc": true,
    "managedUser": false,
    "addedByCpm": false
  },
  "patient": {
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
    "forgotPasswordToken": "7099",
    "familyMembers": [
      {
        "id": "5cef956ef893f467ffa9ffcc",
        "email": "ddJdgVqM@eyecarelive.com",
        "pharmacyName": null,
        "pharmacyAddress": null,
        "aboutMe": {
          "id": "5cef956ef893f467ffa9ffc9",
          "firstName": "Slate",
          "lastName": "Member",
          "birthDate": "",
          "address": "qbNrHbKolNuq9+DQCMrbNw==",
          "city": "28L8jdmZdw/TOE19cYNfyg==",
          "country": "eGcNxOZVnF4jlkABhqaIAQ==",
          "pincode": "Zf6QZAhj9x3iULdEWv9pfA==",
          "gender": "male",
          "languagesSpeak": null,
          "additionalInfo": null,
          "state": "wPCNRzWVjd+MXrn0+dB4Cg==",
          "lat": null,
          "lang": null
        },
        "contactInfo": {
          "id": "5cef956ef893f467ffa9ffca",
          "email": "patientuser1@eyecarelive.com",
          "phone": "X025s2zeUri6K/6HA21+UA==",
          "smsNotification": false,
          "countryCode": null,
          "country": null,
          "emlNt": false
        },
        "patientInfo": null,
        "doctorInfo": null,
        "role": {
          "id": "551ad2a4e4b0b59ff0ccecc9",
          "name": "patient"
        },
        "timezone": null,
        "createdAt": "2019-05-30 01:33 AM PDT",
        "forgotPasswordToken": null,
        "familyMembers": null,
        "parentUser": null,
        "parentUserRelation": "brother",
        "password": null,
        "rating": null,
        "preferredPharmacies": null,
        "oldPassword": null,
        "loginStatus": null,
        "stripeCustId": null,
        "profileImagePath": null,
        "isReferredDoctor": null,
        "randomtoken": null,
        "isEmailVerified": false,
        "preferredDoctors": null,
        "isAcceptTC": false,
        "insurenceCards": null,
        "notificationSettings": null,
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
        "activated": true,
        "invited": false,
        "validated": true,
        "pilotDoc": false,
        "managedUser": true,
        "addedByCpm": false
      }
    ],
    "parentUser": null,
    "parentUserRelation": null,
    "password": null,
    "rating": null,
    "preferredPharmacies": [
      {
        "id": "5cefff05f893f4052b1271ec",
        "name": "Mediplus store",
        "address": "hinjewadi phase-1",
        "email": "niteshy2391@gmail.com",
        "city": "pune",
        "state": "Maharashtra",
        "country": null,
        "zipCode": "411007",
        "phoneNumber": "9423505079",
        "validated": false
      }
    ],
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": "6yZMnuPs8a4fXTM8EgbceG9D9mDKC7Rs7SN+oIXZTdQ=",
    "profileImagePath": null,
    "isReferredDoctor": null,
    "randomtoken": "BThd5P",
    "isEmailVerified": false,
    "preferredDoctors": [
      "56fb7614e4b0d3123cea4925",
      "56fbd63de4b0777c5a04f540"
    ],
    "isAcceptTC": false,
    "insurenceCards": null,
    "notificationSettings": {
      "id": "5ceed13cf893f45b5812b8df",
      "email": true,
      "sendReminderForMedicine": true,
      "addTestreport": true,
      "sentMessage": true,
      "addTreatmentPlan": true,
      "sendReminderForEyeTest": true,
      "push": true,
      "sms": true
    },
    "clinics": null,
    "passCode": null,
    "emrId": null,
    "ssnId": null,
    "clinicInfo": null,
    "ref": null,
    "docOrg": null,
    "doctorsOrg": null,
    "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlIiwiZXhwIjoxNTU5MjUwNDgwLCJncmFudHMiOnsiaWRlbnRpdHkiOiI1Y2VlZDEzY2Y4OTNmNDViNTgxMmI4ZTEiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NWNlZWQxM2NmODkzZjQ1YjU4MTJiOGUxIn19LCJqdGkiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlLTE1NTkyNDY5NzYiLCJzdWIiOiJBQ2M5MGJmNjdhODk0YjA0YjA2NTdkMjJkN2FlOTQ5ZDk3In0._OzAiloA2trSDKPE4HAhP3WIvjvfWkYbWd_zav_pQpQ",
    "bucket": null,
    "repoSub": false,
    "badge": null,
    "preferredEclClinics": null,
    "eclClinicId": null,
    "profileColor": null,
    "activated": true,
    "invited": false,
    "validated": true,
    "pilotDoc": false,
    "managedUser": false,
    "addedByCpm": false
  },
  "questionaire": null,
  "todos": null,
  "speciality": {
    "id": "55b7802be4b0b393bf91678e",
    "name": null,
    "questionnaire": null
  },
  "createdAt": "2019-06-03 06:02 AM PDT",
  "appointmentPrice": 0,
  "status": "pending",
  "waitId": 0,
  "currentLocationState": null,
  "isReferredDoctorAvailable": null,
  "diseaseImageFilePath": null,
  "contactlenseImageFilePath": null,
  "patientPreferredVisitLanguage": null,
  "symtons": "Contact lens",
  "createdBy": "5ceed13cf893f45b5812b8e1",
  "paymentStatus": null,
  "visionTest": null,
  "videoVisitPath": null,
  "remark": null,
  "callReceivedStatus": false,
  "files": null,
  "needFollowUp": false,
  "pharmacy": [
    {
      "id": "5cefff05f893f4052b1271ec",
      "name": "Mediplus store",
      "address": "hinjewadi phase-1",
      "email": "niteshy2391@gmail.com",
      "city": "pune",
      "state": "Maharashtra",
      "country": null,
      "zipCode": "411007",
      "phoneNumber": "9423505079",
      "validated": false
    }
  ],
  "visitType": "offline",
  "visitPurpose": "contactlens",
  "availabilityTimeSlot": null,
  "availability": null,
  "lasikSurgery": null,
  "closedOrCanceledAt": null,
  "convertedStartDate": null,
  "medicinePrescriptions": null,
  "eyeTest": null,
  "coverageParam": null,
  "clinic": null,
  "checkinForms": null,
  "paymentMode": "alreadypaid",
  "solutionBottleImage": null,
  "videoMessage": null,
  "eclClinic": null,
  "chiefCompliant": "Testing Cheif",
  "testStatus": null,
  "eyeProblems": null,
  "recomendedTests": {
    "id": "5cf51a4df893f42a2c872057",
    "dryEye": "0",
    "contactLens": "1",
    "visionTest": "1",
    "userId": "5ceed13cf893f45b5812b8e1",
    "createdAt": "2019-06-03 06:02 AM PDT"
  },
  "callImages": null,
  "codes": null,
  "physicalExam": null,
  "dryEyeTestId": null,
  "contactLensTestId": null,
  "visionTestId": null,
  "clinicVisit": false,
  "cancelled": false,
  "finished": false,
  "inProgress": false,
  "notifiedForPendingVisit": false,
  "reminderSend": false,
  "notifiedForTwoDaysPendingVisit": false,
  "followUp": false,
  "chargeble": false,
  "symtonUpdated": false,
  "eclClinicVisit": false
}
```

> Make sure to replace `X-Auth-Token` with your API key.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/doctor/createVisit/v3
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
  | **Doctor** |   |
doctor | Doctor ID | Integer | Required
visitPurpose | visitPurpose parameter need fixed values, Please check visitPurpose table. | String | Required
diseaseImageFilePath | In this parameter need to pass if user uploading diseaseimages | String | Optional
symtons | In this parameter, need to pass symptoms name like Eye Pain  | String | Required
paymentMode | Payment mode, Credit card, Insurance, AlreadyPaid | String | Required
treatment[{}] | It’s for dry eye | String | Optional
visitType |  offline | String | Required
chiefCompliant |  need to pass Cheif complaint | String | Required
  | **Speciality** |   |
ID | ID of Speciality | String | Required
Appointment | Appointment | String | Optional
availabilityTimeSlot | Availability time should be pass as per doctor avaibility time. | String | Optional

### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | Appointment ID created by database | Integer
Start date | Start date of created | String
End Date | End date of created | String
Doctor | doctor name info | String
Patient | Patient name Info | String
ID | user id# | Integer
Email | User’s Email address | String
Pharmacy Name | Pharmacy name deprecated | String
pharmacy Address | Pharmacy address deprecated | String
profile Image Id | Profile photo ID deprecated | Integer
profile Image Name | Profile photo Name deprecated | .jpg,etc
About Me :[{}] | about me for User’s details | String
Contact Info:[{}] | Contact person Info | String
Patient Info :[{}] | Patient info | String
Doctor Info :[{}] | Doctor info | String
Hospital Attached With List :[{}] | Hospital Attached with list | String
Family History:[{}] | Array of the family history | String
Awards Received List | Awards received list | String
Prescription | Prescription | String
Questionnaire | Questionnaire details | String
TODO | Treatment plan details | String
Specialities | Specialities Details | String
Appointment | Appointment details | String
Report | Report | String
Created At :[{}] | Array of the created at | String




`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Update Contact Lens Test (update the dry eye test with previous appointment ID)

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X POST "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/doctor/updateVisit/v3/5cf51a4df893f42a2c872058" -d '{"questionaire":{"questions":null,"symptoms":null,"frequency":null,"severity":null,"treatment":null,"appointment":null,"lasikQuestionnaire":null,"contactLenseQuestions":[{"question":"Quality of your vision during day ?","answerType":"String","answer":"2","param1":null,"param2":null,"param3":null},{"question":"Quality of your vision during night ?","answerType":"String","answer":"6","param1":null,"param2":null,"param3":null},{"question":"Describe your comfort level with the lens - Beginning of day ?","answerType":"String","answer":"4","param1":null,"param2":null,"param3":null},{"question":"Describe your comfort level with the lens - Before wearing ?","answerType":"String","answer":"6","param1":null,"param2":null,"param3":null},{"question":"Describe your comfort level with the lens - After wearing ?","answerType":"String","answer":"7","param1":null,"param2":null,"param3":null},{"question":"Describe your comfort level with the lens - End of day ?","answerType":"String","answer":"2","param1":null,"param2":null,"param3":null},{"question":"How long do you wear your lens on average ?","answerType":"String","answer":"2 Hours","param1":null,"param2":null,"param3":null},{"question":"How long do you wear your lens today ?","answerType":"String","answer":"3 Hours","param1":null,"param2":null,"param3":null},{"question":"How old are your lens?","answerType":"String","answer":"2Days","param1":null,"param2":null,"param3":null},{"question":"How old are your lens?","answerType":"String","answer":"","param1":null,"param2":null,"param3":null},{"question":"Are you experiencing any of condition ?","answerType":"String","answer":"Redness","param1":null,"param2":null,"param3":null}]}}'
```

> The above command returns JSON structured like this:

```json
{
  "id": "5cf51a4df893f42a2c872058",
  "startDate": "2019-06-03 06:02 AM PDT",
  "endDate": "2019-06-03 06:17 AM PDT",
  "doctor": {
    "id": "56fb7614e4b0d3123cea4925",
    "email": "nitesh.yadav@cupertinosoft.com",
    "pharmacyName": null,
    "pharmacyAddress": null,
    "aboutMe": {
      "id": "56fb7614e4b0d3123cea4923",
      "firstName": "Dr. John",
      "lastName": "Gelles",
      "birthDate": "xCbUo9+vCO6W+uI8luz3YA==",
      "address": "8L10iLEjsRBVkFaI1gu4bw==",
      "city": "8L10iLEjsRBVkFaI1gu4bw==",
      "country": "rwq24J1FnEhqovLa/bo5uQ==",
      "pincode": "+ffKFHCfLQG2vGeutdG6BQ==",
      "gender": "male",
      "languagesSpeak": [
        "English",
        "",
        ""
      ],
      "additionalInfo": "Hi I plays cricket",
      "state": "tdK26+Dp5ks9TH9wFlmgDA==",
      "lat": null,
      "lang": null
    },
    "contactInfo": {
      "id": "56fb7614e4b0d3123cea4924",
      "email": "nakulypatil@gmail.com",
      "phone": "Hj+M0AnqV5zonFbsdcSXUw==",
      "smsNotification": true,
      "countryCode": "+376",
      "country": "USA",
      "emlNt": true
    },
    "patientInfo": null,
    "doctorInfo": {
      "id": "56fb7614e4b0d3123cea4925",
      "educationList": [
        {
          "id": "5cd16094f893f460b09abd74",
          "degree": "MBBS(MD)",
          "university": "Oxford",
          "yearOfPasssing": "2018"
        }
      ],
      "hospitalAttachedWithList": [
        {
          "id": "5cd16cb7f893f460b09abeed",
          "name": "eyecarelivedemo1",
          "city": "NewYork",
          "country": "USA"
        }
      ],
      "awardsReceivedList": [
        {
          "id": "5ce40145f893f43cc2a09260",
          "name": "Test",
          "description": "demo",
          "date": "May 21, 2019"
        }
      ],
      "specialities": [
        {
          "id": "55b78065e4b0b393bf91678f",
          "name": "general physician",
          "questionnaire": null
        }
      ],
      "licencedState": [
        {
          "id": "5665a2cb9a87399fa0b9ba34",
          "state": "AK"
        },
        {
          "id": "5665a2cb9a87399fa0b9ba35",
          "state": "AZ"
        },
        {
          "id": "5665a2cb9a87399fa0b9ba36",
          "state": "AR"
        }
      ],
      "registrationNumber": "44444444",
      "whyCoolDoctors": null,
      "bio": "Bio testingiii",
      "profession": "Ophthalmologist",
      "availabilityTimeZone": "Asia/Kabul",
      "npi": "1234",
      "availabilityStatus": "On",
      "availabilityMsg": "",
      "passwardChanged": false,
      "consultationFees": null,
      "paymentOptions": null,
      "appCountEmail": false,
      "monthlyCharge": false
    },
    "role": {
      "id": "551ad2ffe4b0b59ff0cceccb",
      "name": "doctor"
    },
    "timezone": {
      "id": "55f283b4e4b029528c27d0c5",
      "timezone": "Asia/Kolkata",
      "displayName": "India Standard Time"
    },
    "createdAt": "2016-03-29 11:45 PM PDT",
    "forgotPasswordToken": "6466",
    "familyMembers": null,
    "parentUser": null,
    "parentUserRelation": null,
    "password": null,
    "rating": null,
    "preferredPharmacies": null,
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": "W2iBDJ6LU434JDk4LCyUdqpe2ooWTqPdMvxS8yYrpjg=",
    "profileImagePath": "https://s3.amazonaws.com/deveclprofimg/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/imgDefault.png",
    "isReferredDoctor": null,
    "randomtoken": "esnckN",
    "isEmailVerified": false,
    "preferredDoctors": [
      "59a6456fe4b0be451171721c",
      "59a7c9a5e4b0be4511718cb8"
    ],
    "isAcceptTC": true,
    "insurenceCards": null,
    "notificationSettings": null,
    "clinics": [
      "58f9d4a7e4b07023de8c0d64"
    ],
    "passCode": null,
    "emrId": null,
    "ssnId": null,
    "clinicInfo": null,
    "ref": null,
    "docOrg": null,
    "doctorsOrg": {
      "id": "59cb5445e4b0fa09b42591b7",
      "orgName": "Paragon"
    },
    "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlIiwiZXhwIjoxNTU5NTU4MDg0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NWNlYTZkOThmODkzZjQwYTVmMDM5NWIxIn19LCJqdGkiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlLTE1NTk1NTQ0MzIiLCJzdWIiOiJBQ2M5MGJmNjdhODk0YjA0YjA2NTdkMjJkN2FlOTQ5ZDk3In0.TEVWwtIrp5WPOBfSUgA1cieTPxTkhzK_2WsdZkTCkPE",
    "bucket": null,
    "repoSub": false,
    "badge": null,
    "preferredEclClinics": null,
    "eclClinicId": null,
    "profileColor": null,
    "activated": true,
    "invited": false,
    "validated": true,
    "pilotDoc": true,
    "managedUser": false,
    "addedByCpm": false
  },
  "patient": {
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
    "forgotPasswordToken": "7099",
    "familyMembers": [
      {
        "id": "5cef956ef893f467ffa9ffcc",
        "email": "ddJdgVqM@eyecarelive.com",
        "pharmacyName": null,
        "pharmacyAddress": null,
        "aboutMe": {
          "id": "5cef956ef893f467ffa9ffc9",
          "firstName": "Slate",
          "lastName": "Member",
          "birthDate": "",
          "address": "qbNrHbKolNuq9+DQCMrbNw==",
          "city": "28L8jdmZdw/TOE19cYNfyg==",
          "country": "eGcNxOZVnF4jlkABhqaIAQ==",
          "pincode": "Zf6QZAhj9x3iULdEWv9pfA==",
          "gender": "male",
          "languagesSpeak": null,
          "additionalInfo": null,
          "state": "wPCNRzWVjd+MXrn0+dB4Cg==",
          "lat": null,
          "lang": null
        },
        "contactInfo": {
          "id": "5cef956ef893f467ffa9ffca",
          "email": "patientuser1@eyecarelive.com",
          "phone": "X025s2zeUri6K/6HA21+UA==",
          "smsNotification": false,
          "countryCode": null,
          "country": null,
          "emlNt": false
        },
        "patientInfo": null,
        "doctorInfo": null,
        "role": {
          "id": "551ad2a4e4b0b59ff0ccecc9",
          "name": "patient"
        },
        "timezone": null,
        "createdAt": "2019-05-30 01:33 AM PDT",
        "forgotPasswordToken": null,
        "familyMembers": null,
        "parentUser": null,
        "parentUserRelation": "brother",
        "password": null,
        "rating": null,
        "preferredPharmacies": null,
        "oldPassword": null,
        "loginStatus": null,
        "stripeCustId": null,
        "profileImagePath": null,
        "isReferredDoctor": null,
        "randomtoken": null,
        "isEmailVerified": false,
        "preferredDoctors": null,
        "isAcceptTC": false,
        "insurenceCards": null,
        "notificationSettings": null,
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
        "activated": true,
        "invited": false,
        "validated": true,
        "pilotDoc": false,
        "managedUser": true,
        "addedByCpm": false
      }
    ],
    "parentUser": null,
    "parentUserRelation": null,
    "password": null,
    "rating": null,
    "preferredPharmacies": [
      {
        "id": "5cefff05f893f4052b1271ec",
        "name": "Mediplus store",
        "address": "hinjewadi phase-1",
        "email": "niteshy2391@gmail.com",
        "city": "pune",
        "state": "Maharashtra",
        "country": null,
        "zipCode": "411007",
        "phoneNumber": "9423505079",
        "validated": false
      }
    ],
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": "6yZMnuPs8a4fXTM8EgbceG9D9mDKC7Rs7SN+oIXZTdQ=",
    "profileImagePath": null,
    "isReferredDoctor": null,
    "randomtoken": "BThd5P",
    "isEmailVerified": false,
    "preferredDoctors": [
      "56fb7614e4b0d3123cea4925",
      "56fbd63de4b0777c5a04f540"
    ],
    "isAcceptTC": false,
    "insurenceCards": null,
    "notificationSettings": {
      "id": "5ceed13cf893f45b5812b8df",
      "email": true,
      "sendReminderForMedicine": true,
      "addTestreport": true,
      "sentMessage": true,
      "addTreatmentPlan": true,
      "sendReminderForEyeTest": true,
      "push": true,
      "sms": true
    },
    "clinics": null,
    "passCode": null,
    "emrId": null,
    "ssnId": null,
    "clinicInfo": null,
    "ref": null,
    "docOrg": null,
    "doctorsOrg": null,
    "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlIiwiZXhwIjoxNTU5MjUwNDgwLCJncmFudHMiOnsiaWRlbnRpdHkiOiI1Y2VlZDEzY2Y4OTNmNDViNTgxMmI4ZTEiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NWNlZWQxM2NmODkzZjQ1YjU4MTJiOGUxIn19LCJqdGkiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlLTE1NTkyNDY5NzYiLCJzdWIiOiJBQ2M5MGJmNjdhODk0YjA0YjA2NTdkMjJkN2FlOTQ5ZDk3In0._OzAiloA2trSDKPE4HAhP3WIvjvfWkYbWd_zav_pQpQ",
    "bucket": null,
    "repoSub": false,
    "badge": null,
    "preferredEclClinics": null,
    "eclClinicId": null,
    "profileColor": null,
    "activated": true,
    "invited": false,
    "validated": true,
    "pilotDoc": false,
    "managedUser": false,
    "addedByCpm": false
  },
  "questionaire": {
    "id": "5cf51aaff893f42a2c872086",
    "questions": null,
    "symptoms": null,
    "frequency": null,
    "severity": null,
    "treatment": null,
    "appointment": null,
    "lasikQuestionnaire": null,
    "contactLenseQuestions": [
      {
        "id": "5cf51aaff893f42a2c87207b",
        "question": "Quality of your vision during day ?",
        "answerType": "String",
        "answer": "2",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf51aaff893f42a2c87207c",
        "question": "Quality of your vision during night ?",
        "answerType": "String",
        "answer": "6",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf51aaff893f42a2c87207d",
        "question": "Describe your comfort level with the lens - Beginning of day ?",
        "answerType": "String",
        "answer": "4",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf51aaff893f42a2c87207e",
        "question": "Describe your comfort level with the lens - Before wearing ?",
        "answerType": "String",
        "answer": "6",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf51aaff893f42a2c87207f",
        "question": "Describe your comfort level with the lens - After wearing ?",
        "answerType": "String",
        "answer": "7",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf51aaff893f42a2c872080",
        "question": "Describe your comfort level with the lens - End of day ?",
        "answerType": "String",
        "answer": "2",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf51aaff893f42a2c872081",
        "question": "How long do you wear your lens on average ?",
        "answerType": "String",
        "answer": "2 Hours",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf51aaff893f42a2c872082",
        "question": "How long do you wear your lens today ?",
        "answerType": "String",
        "answer": "3 Hours",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf51aaff893f42a2c872083",
        "question": "How old are your lens?",
        "answerType": "String",
        "answer": "2Days",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf51aaff893f42a2c872084",
        "question": "How old are your lens?",
        "answerType": "String",
        "answer": "",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5cf51aaff893f42a2c872085",
        "question": "Are you experiencing any of condition ?",
        "answerType": "String",
        "answer": "Redness",
        "param1": null,
        "param2": null,
        "param3": null
      }
    ]
  },
  "todos": null,
  "speciality": {
    "id": "55b7802be4b0b393bf91678e",
    "name": "eye care",
    "questionnaire": null
  },
  "createdAt": "2019-06-03 06:02 AM PDT",
  "appointmentPrice": 0,
  "status": "pending",
  "waitId": 0,
  "currentLocationState": null,
  "isReferredDoctorAvailable": null,
  "diseaseImageFilePath": null,
  "contactlenseImageFilePath": null,
  "patientPreferredVisitLanguage": null,
  "symtons": "Contact lens",
  "createdBy": "5ceed13cf893f45b5812b8e1",
  "paymentStatus": null,
  "visionTest": null,
  "videoVisitPath": null,
  "remark": null,
  "callReceivedStatus": false,
  "files": null,
  "needFollowUp": false,
  "pharmacy": [
    {
      "id": "5cefff05f893f4052b1271ec",
      "name": "Mediplus store",
      "address": "hinjewadi phase-1",
      "email": "niteshy2391@gmail.com",
      "city": "pune",
      "state": "Maharashtra",
      "country": null,
      "zipCode": "411007",
      "phoneNumber": "9423505079",
      "validated": false
    }
  ],
  "visitType": "offline",
  "visitPurpose": "contactlens",
  "availabilityTimeSlot": null,
  "availability": null,
  "lasikSurgery": null,
  "closedOrCanceledAt": null,
  "convertedStartDate": null,
  "medicinePrescriptions": null,
  "eyeTest": null,
  "coverageParam": null,
  "clinic": null,
  "checkinForms": null,
  "paymentMode": "alreadypaid",
  "solutionBottleImage": null,
  "videoMessage": null,
  "eclClinic": null,
  "chiefCompliant": "Testing Cheif",
  "testStatus": null,
  "eyeProblems": null,
  "recomendedTests": {
    "id": "5cf51a4df893f42a2c872057",
    "dryEye": "0",
    "contactLens": "2",
    "visionTest": "1",
    "userId": "5ceed13cf893f45b5812b8e1",
    "createdAt": "2019-06-03 06:02 AM PDT"
  },
  "callImages": null,
  "codes": null,
  "physicalExam": null,
  "dryEyeTestId": null,
  "contactLensTestId": null,
  "visionTestId": null,
  "clinicVisit": false,
  "cancelled": false,
  "finished": false,
  "inProgress": false,
  "notifiedForPendingVisit": false,
  "reminderSend": false,
  "notifiedForTwoDaysPendingVisit": false,
  "followUp": false,
  "chargeble": false,
  "symtonUpdated": false,
  "eclClinicVisit": false
}
```

> Make sure to replace `X-Auth-Token` with your API key.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/doctor/createVisit/v3
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
  | ** Questionnaire 
     array has  all questions and answers sendt in the visit to the doctor** |   |
questionaire | Questions | String | Required
questions | ID | Integer | Optional
symptoms:[{}] | Questions | String | Required
severity:[{}] | Questions | String | Required
frequency:[{}] | Questions | String | Required
treatment:[{}] | Questions | String | Required
AnswerType | Answer Type | Boolean | Required
Answer | answer (Y/N) | String | Optional

### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | Appointment ID created by database | Integer
Start date | Start date of created | String
End Date | End date of created | String
Doctor | doctor name info | String
Patient | Patient name Info | String
ID | user id# | Integer
Email | User’s Email address | String
Pharmacy Name | Pharmacy name deprecated | String
pharmacy Address | Pharmacy address deprecated | String
profile Image Id | Profile photo ID deprecated | Integer
profile Image Name | Profile photo Name deprecated | .jpg,etc
About Me :[{}] | about me for User’s details | String
Contact Info:[{}] | Contact person Info | String
Patient Info :[{}] | Patient info | String
Doctor Info :[{}] | Doctor info | String
Hospital Attached With List :[{}] | Hospital Attached with list | String
Family History:[{}] | Array of the family history | String
Awards Received List | Awards received list | String
Prescription | Prescription | String
Questionnaire | Questionnaire details | String
TODO | Treatment plan details | String
Specialities | Specialities Details | String
Appointment | Appointment details | String
Report | Report | String
Created At :[{}] | Array of the created at | String




`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

