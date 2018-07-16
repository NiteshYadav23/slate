

# Pending Appointments

## Get First Pending Appointment

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/firstTen/pending"

```

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/nextTen/1/pending"

```


> The above command returns JSON structured like this:

```json
[
  {
    "id": "5a37b5f6e4b00ad7ad9bf261",
    "startDate": "2017-12-18 04:35 AM PST",
    "endDate": "2017-12-18 04:50 AM PST",
    "doctor": {
      "id": "56fb7614e4b0d3123cea4925",
      "email": "nitesh.yadav@cupertinosoft.com",
      "pharmacyName": null,
      "pharmacyAddress": null,
      "profileImageId": null,
      "profileImageName": null,
      "aboutMe": {
        "id": "56fb7614e4b0d3123cea4923",
        "firstName": "Paul",
        "lastName": "Super",
        "birthDate": "03/22/2016",
        "address": "1010 W Fremont Ave # 200",
        "city": "Sunnyvale",
        "country": "United States",
        "pincode": "94087",
        "gender": " Male",
        "languagesSpeak": [
          "English",
          "",
          ""
        ],
        "additionalInfo": null,
        "state": "ca"
      },
      "contactInfo": {
        "id": "56fb7614e4b0d3123cea4924",
        "email": "nitesh.yadav@cupertinosoft.com",
        "phone": "8055802119",
        "smsNotification": false,
        "countryCode": "+91",
        "country": "USA",
        "emlNt": false
      },
      "patientInfo": null,
      "doctorInfo": {
        "id": "5823018fe4b0242bf4219c2d",
        "educationList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c3",
            "degree": "Bca",
            "university": "un",
            "yearOfPasssing": "88778"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c4",
            "name": "tt",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c5",
            "name": "q",
            "description": "Description",
            "date": "11/11/1991"
          }
        ],
        "specialities": [
          {
            "id": "55b78065e4b0b393bf91678f",
            "name": "general physician",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba33",
            "state": "AL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba37",
            "state": "CA"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba40",
            "state": "IL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba41",
            "state": "IN"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba42",
            "state": "IA"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "",
        "profession": "Optometrist",
        "availabilityTimeZone": "Asia/Kolkata",
        "npi": "0123456789778"
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
      "forgotPasswordToken": "4691",
      "familyMembers": null,
      "parentUser": null,
      "parentUserRelation": null,
      "password": null,
      "rating": null,
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser1",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser1@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsuper.png",
      "isReferredDoctor": null,
      "randomtoken": "esnckN",
      "isEmailVerified": false,
      "doctorsGroups": [
        {
          "id": "56d01388e4b0cd1739f0e076",
          "groupName": "Silicon Valley Eye Physicians"
        }
      ],
      "preferredDoctors": [
        "56fbd63de4b0777c5a04f540",
        "595a0d97e4b0c065c25684ea"
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
      "twilioAccessToken": null,
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "patient": {
      "id": "5742c31ae4b0e03acf77f054",
      "email": "bhagwant.sangvikar@cupertinosoft.com",
      "pharmacyName": null,
      "pharmacyAddress": null,
      "profileImageId": null,
      "profileImageName": null,
      "aboutMe": {
        "id": "5742c31ae4b0e03acf77f052",
        "firstName": "Bhagwant",
        "lastName": "Sangvikar",
        "birthDate": "01/01/1991",
        "address": "Pune",
        "city": "Pune",
        "country": "USA",
        "pincode": "12345",
        "gender": "Male",
        "languagesSpeak": null,
        "additionalInfo": null,
        "state": "India"
      },
      "contactInfo": {
        "id": "5742c31ae4b0e03acf77f053",
        "email": "bhagwant.sangvikar@cupertinosoft.com",
        "phone": "8800000000",
        "smsNotification": false,
        "countryCode": null,
        "country": null,
        "emlNt": false
      },
      "patientInfo": {
        "id": "580788abe4b0d95797e2339e",
        "lifeStyle": {
          "id": "5742c376e4b0e03acf77f0d8",
          "medication": "Koo",
          "alcoholUse": "yes",
          "allergiesToMedication": "Hhj",
          "alcoholDrinksPerWeek": "7-14",
          "medicalCondition": "High Cholesterol,Cancer",
          "allergies": null,
          "vitaminSupplements": "Iuu",
          "smoke": "7788",
          "contactlenses": "Hard"
        },
        "familyHistory": {
          "id": "580788abe4b0d95797e2339d",
          "description": null,
          "diseaseRelation": [
            {
              "conditions": "Allergic reaction",
              "relationship": "Aunt"
            }
          ]
        }
      },
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
      "createdAt": "2016-05-23 01:45 AM PDT",
      "forgotPasswordToken": null,
      "familyMembers": [
        {
          "id": "57fbc8f9e4b0a73bcaeb22eb",
          "email": "BeUcYTxn@cooldoctors.io",
          "pharmacyName": null,
          "pharmacyAddress": null,
          "profileImageId": null,
          "profileImageName": null,
          "aboutMe": {
            "id": "57fbc8f9e4b0a73bcaeb22e9",
            "firstName": "Nitin",
            "lastName": "Patil",
            "birthDate": "02/04/2009",
            "address": "Thug",
            "city": "Thus",
            "country": "Albania",
            "pincode": "56777",
            "gender": "Male",
            "languagesSpeak": null,
            "additionalInfo": null,
            "state": "Fiji"
          },
          "contactInfo": {
            "id": "57fbc8f9e4b0a73bcaeb22ea",
            "email": "bhagwant.sangvikar@cupertinosoft.com",
            "phone": "765544567788",
            "smsNotification": false,
            "countryCode": null,
            "country": null,
            "emlNt": true
          },
          "patientInfo": null,
          "doctorInfo": null,
          "role": {
            "id": "551ad2a4e4b0b59ff0ccecc9",
            "name": "patient"
          },
          "timezone": null,
          "createdAt": "2016-10-10 09:59 AM PDT",
          "forgotPasswordToken": null,
          "familyMembers": null,
          "parentUser": null,
          "parentUserRelation": "Brother",
          "password": null,
          "rating": null,
          "preferredPharmacies": null,
          "kandyUserName": null,
          "kandyUserPassword": null,
          "kandyFullUserId": null,
          "oldPassword": null,
          "loginStatus": null,
          "stripeCustId": null,
          "profileImagePath": "https://eyes.cooldoctors.io/PRDIMAGE/doctor/57fbc8f9e4b0a73bcaeb22eb/ProfileImage/FamilyPro_img_349887.jpg",
          "isReferredDoctor": null,
          "randomtoken": null,
          "isEmailVerified": false,
          "doctorsGroups": null,
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
          "doctorsOrg": {
            "id": "59cb542de4b0fa09b42591b5",
            "orgName": "EyecareLive"
          },
          "twilioAccessToken": null,
          "invited": false,
          "validated": true,
          "activated": true,
          "managedUser": true,
          "addedByCpm": false,
          "pilotDoc": true
        },
        {
          "id": "57fbca38e4b0a73bcaeb24e4",
          "email": "thzNKyTN@cooldoctors.io",
          "pharmacyName": null,
          "pharmacyAddress": null,
          "profileImageId": null,
          "profileImageName": null,
          "aboutMe": {
            "id": "57fbca38e4b0a73bcaeb24e2",
            "firstName": "Thuggish",
            "lastName": "Taught ",
            "birthDate": "03/03/2009",
            "address": "Gagging",
            "city": "Gygguhg",
            "country": "Andorra",
            "pincode": "56778",
            "gender": "Male",
            "languagesSpeak": null,
            "additionalInfo": null,
            "state": "Fgjjggjnj"
          },
          "contactInfo": {
            "id": "57fbca38e4b0a73bcaeb24e3",
            "email": "bhagwant.sangvikar@cupertinosoft.com",
            "phone": "5667788885667",
            "smsNotification": false,
            "countryCode": null,
            "country": null,
            "emlNt": true
          },
          "patientInfo": {
            "id": "5939265ae4b0ec2ca8986591",
            "lifeStyle": {
              "id": "5939265ae4b0ec2ca898658f",
              "medication": "",
              "alcoholUse": "no",
              "allergiesToMedication": "",
              "alcoholDrinksPerWeek": "",
              "medicalCondition": "",
              "allergies": "",
              "vitaminSupplements": "",
              "smoke": "",
              "contactlenses": ""
            },
            "familyHistory": {
              "id": "5939265ae4b0ec2ca8986590",
              "description": null,
              "diseaseRelation": []
            }
          },
          "doctorInfo": null,
          "role": {
            "id": "551ad2a4e4b0b59ff0ccecc9",
            "name": "patient"
          },
          "timezone": null,
          "createdAt": "2016-10-10 10:04 AM PDT",
          "forgotPasswordToken": null,
          "familyMembers": null,
          "parentUser": null,
          "parentUserRelation": "Brother",
          "password": null,
          "rating": null,
          "preferredPharmacies": null,
          "kandyUserName": null,
          "kandyUserPassword": null,
          "kandyFullUserId": null,
          "oldPassword": null,
          "loginStatus": null,
          "stripeCustId": null,
          "profileImagePath": null,
          "isReferredDoctor": null,
          "randomtoken": null,
          "isEmailVerified": false,
          "doctorsGroups": null,
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
          "doctorsOrg": {
            "id": "59cb542de4b0fa09b42591b5",
            "orgName": "EyecareLive"
          },
          "twilioAccessToken": null,
          "invited": false,
          "validated": true,
          "activated": true,
          "managedUser": true,
          "addedByCpm": false,
          "pilotDoc": true
        }
      ],
      "parentUser": null,
      "parentUserRelation": null,
      "password": null,
      "rating": null,
      "preferredPharmacies": null,
      "kandyUserName": null,
      "kandyUserPassword": null,
      "kandyFullUserId": null,
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": null,
      "isReferredDoctor": null,
      "randomtoken": "w3asmJ",
      "isEmailVerified": false,
      "doctorsGroups": null,
      "preferredDoctors": [
        "56fb7614e4b0d3123cea4925",
        "56fbd63de4b0777c5a04f540"
      ],
      "isAcceptTC": false,
      "insurenceCards": [
        {
          "name": "cool",
          "files": [
            "1475740716507,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/insurencecard/1475740716507/img_366725front.jpg",
            "1475740716603,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/insurencecard/1475740716603/img_906231dback.jpg"
          ],
          "memberId": null,
          "payerId": null
        }
      ],
      "notificationSettings": null,
      "clinics": null,
      "passCode": null,
      "emrId": null,
      "ssnId": null,
      "clinicInfo": null,
      "ref": null,
      "docOrg": null,
      "doctorsOrg": {
        "id": "59cb542de4b0fa09b42591b5",
        "orgName": "EyecareLive"
      },
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzMzQ3OTMyLCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NzQyYzMxYWU0YjBlMDNhY2Y3N2YwNTQiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwNTc0MmMzMWFlNGIwZTAzYWNmNzdmMDU0In19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTMzNDQzODQiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0._SDBBFF5s7xKbOLIi2IFv3weEDOxKr3D0zITfEwuDHk",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "prescription": null,
    "questionaire": {
      "id": "5a37b5f6e4b00ad7ad9bf260",
      "questions": [
        {
          "id": "5a37b5f6e4b00ad7ad9bf25e",
          "question": "Snellen chart Right Eye vision test",
          "answerType": "String",
          "answer": "20/40",
          "param1": null,
          "param2": null,
          "param3": null
        },
        {
          "id": "5a37b5f6e4b00ad7ad9bf25f",
          "question": "Snellen chart Left Eye vision test",
          "answerType": "String",
          "answer": "20/50",
          "param1": null,
          "param2": null,
          "param3": null
        }
      ],
      "symptoms": null,
      "frequency": null,
      "severity": null,
      "treatment": null,
      "appointment": null,
      "lasikQuestionnaire": null,
      "contactLenseQuestions": null
    },
    "report": null,
    "todos": null,
    "speciality": {
      "id": "55b7802be4b0b393bf91678e",
      "name": "eye care",
      "questionnaire": null,
      "report": null
    },
    "createdAt": "2017-12-18 04:35 AM PST",
    "appointmentPrice": 0,
    "status": "pending",
    "waitId": 0,
    "currentLocationState": "NY",
    "isReferredDoctorAvailable": null,
    "diseaseImageFilePath": null,
    "contactlenseImageFilePath": null,
    "patientPreferredVisitLanguage": null,
    "symtons": "Distorted vision",
    "createdBy": "5742c31ae4b0e03acf77f054",
    "paymentStatus": null,
    "visionTest": null,
    "videoVisitPath": null,
    "remark": null,
    "callReceivedStatus": false,
    "files": null,
    "needFollowUp": false,
    "pharmacy": null,
    "visitType": "offline",
    "visitPurpose": "normalsymtons",
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
    "followUp": false,
    "clinicVisit": false,
    "cancelled": false,
    "inProgress": false,
    "finished": false,
    "chargeble": false,
    "notifiedForPendingVisit": false,
    "reminderSend": false,
    "notifiedForTwoDaysPendingVisit": false
  }
]
```
> Make sure to replace `X-Auth-Token` with your API key.

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/firstTen/pending
`

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/nextTen/{NumberOfPage}/pending
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Use URL | Use URL for Get the pending appointments | String | Required

### Response

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
ID |Appointment ID created by database | Integer
Start date | Start date of created | String
End Date | End Date of created | String
Doctor | Doctor name info | String
Patient | Patient name info | String
ID | user id# | Integer
Email | User's Email ID | String
Pharmacy Name | Pharmacy name deprecated | String
pharmacy Address | pharmacy Address deprecated | String
profile Image Id | Profile image ID deprecated | Integer
profile Image Name | Profile image Name | .jpg,etc
About Me :[{}] | about me for User’s details  | String
Contact Info:[{}] | Contact person Info | String
Patient Info :[{}] | Patient info | String
Doctor Info :[{}] | Doctor info | String
Hospital Attached With List :[{}] | Hospital Attached with list | String
Family History:[{}] | Array of the family history | String
Awards Received List | Awards Received List | String
Prescription | Prescription | String
Questionnaire | Questionnaire details | String
TODO | Treatment plan details | String
Specialities | Specialities Details | String
Appointment | Appointment details | String
Report | Report | String
Created At:[{}] | Date and Time Created at | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Mark as Canceled Appointment

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X POST "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/cancel/5a37b5f6e4b00ad7ad9bfsadad1"
```
> The above command returns JSON structured like this:

```json
{
  200 ok
}
```
> Make sure to replace `X-Auth-Token` with your API key.


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/cancel/{AppointmentID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Appointment ID | For cancel Appoint. | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
200 Ok | It’s means successfully canceled | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Mark as Completed Appointment

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:niteshy2391@gmail.com:doctor:1444571988519:ba0069c205bfdb49b41fb903599a1449" -X POST "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/end/55f28629e4b029528c27d0d8
```
> The above command returns JSON structured like this:

```json
{
  "success": true
}
```
> Make sure to replace `X-Auth-Token` with your API key.


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/end/{AppointmentID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Appointment ID | For complete  Appointment | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
200 Ok | It’s means successfully completed | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>








