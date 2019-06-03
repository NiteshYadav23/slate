

# Patient's Dashboard

## Dashboard of API

Verify if the patient is an existing registered user and has credentials. 


```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/getDashboardInfo/v3"

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
  "prefferedDoctors": null,
  "prefferedEclClinicBeans": null,
  "userId": "5ceed13cf893f45b5812b8e1",
  "familyMemberFlag": false,
  "messageCount": 0,
  "familyMembers": null,
  "pendingTestAppointments": [
    {
      "id": "5ceff9b9f893f4052b127143",
      "startDate": "2019-05-30 08:41 AM PDT",
      "endDate": "2019-05-30 08:56 AM PDT",
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
            },
            {
              "id": "5ce40145f893f43cc2a0925f",
              "degree": "Oxford12",
              "university": "fdfdfdf",
              "yearOfPasssing": ""
            },
            {
              "id": "5cebff52f893f467fffdc9d5",
              "degree": "BCA",
              "university": "University",
              "yearOfPasssing": "2019"
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
          "paymentOptions": [
            "insurancepaid",
            "alreadypaid"
          ],
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
        "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlIiwiZXhwIjoxNTU5MzIzNzU0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NWNlYTZkOThmODkzZjQwYTVmMDM5NWIxIn19LCJqdGkiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlLTE1NTkzMjAxOTIiLCJzdWIiOiJBQ2M5MGJmNjdhODk0YjA0YjA2NTdkMjJkN2FlOTQ5ZDk3In0.o07Jg3GdSM3huqQUXrtOMXdKcWTcaxUu5Ta9buV5xyo",
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
        "forgotPasswordToken": null,
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
        "stripeCustId": null,
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
      "todos": [
        {
          "id": "5ceff9b9f893f4052b127143",
          "patient": "5ceed13cf893f45b5812b8e1",
          "status": 0,
          "appointment": "5ceff9b9f893f4052b127143",
          "assessment": "demo",
          "diagnosis": "demo",
          "treatmentPlan": null,
          "updatedAt": "2019-05-30 09:00 AM PDT",
          "updatedById": null,
          "updatedByName": null
        }
      ],
      "speciality": {
        "id": "55b78065e4b0b393bf91678f",
        "name": "general physician",
        "questionnaire": null
      },
      "createdAt": "2019-05-30 08:41 AM PDT",
      "appointmentPrice": 0,
      "status": "complete",
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
      "pharmacy": null,
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
      "chiefCompliant": "Test API for user",
      "testStatus": "1",
      "eyeProblems": null,
      "recomendedTests": {
        "id": "5ceff9b9f893f4052b127142",
        "dryEye": "1",
        "contactLens": "0",
        "visionTest": "1",
        "userId": "5ceed13cf893f45b5812b8e1",
        "createdAt": null
      },
      "callImages": null,
      "codes": null,
      "physicalExam": null,
      "clinicVisit": false,
      "cancelled": false,
      "finished": true,
      "inProgress": false,
      "reminderSend": false,
      "notifiedForTwoDaysPendingVisit": false,
      "followUp": false,
      "chargeble": false,
      "notifiedForPendingVisit": false,
      "symtonUpdated": false,
      "eclClinicVisit": false
    }
  ]
}
```
### HTTP Request

`POST http://localhost:8080/DoctorOnDemand/api/patient/appointment/getDashboardInfo/v3
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL for  | This is for GET only use the API URL | String | Required

### Response

Parameter |  Description | Type 
--------- | ------------ | ---- 
pendingAppointment | Pending appointment count | String
savedAppointment |Save appointment | String
followupAppointment | Follow up for appointment | String
treatmentPlanFlag | Treatment plan by doctor | String
testReportFlag | Test reported by doctor’s | String
savedAppointmentList | Saved appointment data | String
prefferedDoctors | Preferred doctor ID | String
prefferedEclClinicBeans | Preferred clinic ID | String
userId | Patient’s user ID | String
familyMemberFlag | Deprecated | String
messageCount | Message count for unread | String
familyMembers | Deprecated | String
pendingTestAppointments:[{}] | Eye tests recommendation | String
patient:[{}] | Patient user infromation | String
notificationSettings:[{}] | Deprecated | String
questionaire:[{}] | Deprecated |String
OTHER all perameter  | Deprecated | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>


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


## Start New Consultation (Create an appointment with Chief complaint and Photos, Videos)


