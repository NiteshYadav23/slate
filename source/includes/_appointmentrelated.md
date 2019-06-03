# Appointment related

## Cancel upcoming visit

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X POST "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/cancel/5a2c3534e4b0e4fa266e01cc"


```
> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

> Make sure to replace `X-Auth-Token` with your API key.


Cancel an already scheduled visit

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/cancel/{appointmentId}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{appointmentId} | For cancel appointment using URL and give ID | Integer | Required

### Response

Parameter | Description | Type
--------- | ----------- | ----
Success | True OR False | String




`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Save draft of the visit

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X POST "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/doctor/createVisitWithAvailability" -d '{"doctor":{"id":"56fb7614e4b0d3123cea4925"},"patient":null,"visitPurpose":"dryeye","diseaseImageFilePath":null,"symtons":"Dry Eye","paymentMode":"alreadypaid","questionaire":{"questions":[{"id":null,"answer":"20\/30","question":"Snellen chart Right Eye vision test","answerType":"String"},{"id":null,"answer":"20\/25","question":"Snellen chart Left Eye vision test","answerType":"String"}],"appointment":null,"treatment":[{"id":null,"answer":"","question":"Are you taking medications?","answerType":"String"},{"id":null,"answer":"","question":"Are you taking Omega 3 supplements?","answerType":"String"},{"id":null,"answer":"","question":"Are you doing warm compresses?","answerType":"String"},{"id":null,"answer":"","question":"Are you using eye drops?","answerType":"String"}]},"speciality":{"id":"55b7802be4b0b393bf91678e","questionnaire":null,"report":null},"status":"draft","visitType":"offline"}'
```

> The above command returns JSON structured like this:

```json
{
  "id": "5a2e646ae4b0e4fa266e1a83",
  "startDate": "2017-12-11 02:56 AM PST",
  "endDate": "2017-12-11 03:11 AM PST",
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
          "degree": "    Bca",
          "university": "   un",
          "yearOfPasssing": "   88778"
        }
      ],
      "hospitalAttachedWithList": [
        {
          "id": "59e09cbce4b0a70b0de5b0c4",
          "name": "   ng tt",
          "city": "    Pune",
          "country": "   India"
        }
      ],
      "awardsReceivedList": [
        {
          "id": "59e09cbce4b0a70b0de5b0c5",
          "name": "q",
          "description": "    • • • • • • •  •  •  •  Description",
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
      "bio": "Dr. Moshe Mendelson is one of the prominent optometrists based in the silicon valley and has over 25 years of experience. He is Fellow of the International Academy of Orthokeratology and has treated thousands of patients in his career. Dr. Mendelson received his doctorate from the University of California, Berkeley and trained at Veterans Administration Hospital at Stanford Medical Center, Oak Knoll Naval Hospital, Pacific Presbyterian Medical Center. Formerly, he was Adjunct Professor for the New England College of Optometry and Salus University. He is a sought after speaker and travels around the world to speak at conferences and teaches optometry students from colleges around the country.\n\n\n\"I am passionate about using technological advances in telemedicine to be able to treat patients at a fraction of the cost. Telemedicine allows us to treat patients around the world who don't have easy access to good eye care\"",
      "profession": "Optometrist",
      "availabilityTimeZone": "America/Los_Angeles",
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
    "preferredPharmacy": null,
    "kandyUserName": null,
    "kandyUserPassword": null,
    "kandyFullUserId": null,
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": null,
    "profileImagePath": "https://dev.api.cooldoctors.io:8443/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsuper.png",
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
    "id": "5a2c0a69e4b0e4fa266e0180",
    "email": "patientuser@cooldoctors.io",
    "pharmacyName": null,
    "pharmacyAddress": null,
    "profileImageId": null,
    "profileImageName": null,
    "aboutMe": {
      "id": "5a2c0a69e4b0e4fa266e017d",
      "firstName": "Patient",
      "lastName": "Name",
      "birthDate": null,
      "address": "Kallam Anji Reddy Campus, Banjara Hills",
      "city": "Hyderabad",
      "country": "India",
      "pincode": "500034",
      "gender": "Female",
      "languagesSpeak": null,
      "additionalInfo": null,
      "state": "Telangana"
    },
    "contactInfo": {
      "id": "5a2c0a69e4b0e4fa266e017f",
      "email": "patientuser@cooldoctors.io",
      "phone": "8806900740",
      "smsNotification": false,
      "countryCode": null,
      "country": null,
      "emlNt": false
    },
    "patientInfo": {
      "id": "5a2e1e23e4b0e4fa266e0805",
      "lifeStyle": {
        "id": "5a2e1e23e4b0e4fa266e0803",
        "medication": "Test",
        "alcoholUse": "yes",
        "allergiesToMedication": "Testing",
        "alcoholDrinksPerWeek": "Do not Drink",
        "medicalCondition": "Cancer",
        "allergies": "Pollen",
        "vitaminSupplements": "Test",
        "smoke": "1",
        "contactlenses": "Soft"
      },
      "familyHistory": {
        "id": "5a2e1e23e4b0e4fa266e0804",
        "description": null,
        "diseaseRelation": [
          {
            "conditions": "Cataract",
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
    "createdAt": "2017-12-09 08:08 AM PST",
    "forgotPasswordToken": null,
    "familyMembers": [
      {
        "id": "5a2c1827e4b0e4fa266e018f",
        "email": "ESa6zdCf@eyecarelive.com",
        "pharmacyName": null,
        "pharmacyAddress": null,
        "profileImageId": "5a2c31a9e4b0e4fa266e01bf",
        "profileImageName": "0-cus-d1-b928632e6fef67a90ca8ecd0121882bb.jpg",
        "aboutMe": {
          "id": "5a2c1827e4b0e4fa266e018d",
          "firstName": "neet",
          "lastName": "yadav",
          "birthDate": null,
          "address": "Pune",
          "city": "Pune",
          "country": "india",
          "pincode": "411039",
          "gender": "male",
          "languagesSpeak": null,
          "additionalInfo": null,
          "state": "MH"
        },
        "contactInfo": {
          "id": "5a2c1827e4b0e4fa266e018e",
          "email": "Neet@gmail.com",
          "phone": "8055802119",
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
        "createdAt": "2017-12-09 09:06 AM PST",
        "forgotPasswordToken": null,
        "familyMembers": null,
        "parentUser": null,
        "parentUserRelation": "brother",
        "password": null,
        "rating": null,
        "preferredPharmacy": null,
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
        "doctorsOrg": null,
        "twilioAccessToken": null,
        "invited": false,
        "validated": true,
        "activated": true,
        "managedUser": true,
        "addedByCpm": false,
        "pilotDoc": false
      },
      {
        "id": "5a2e4470e4b0e4fa266e0efe",
        "email": "8BQH25JS@eyecarelive.com",
        "pharmacyName": null,
        "pharmacyAddress": null,
        "profileImageId": null,
        "profileImageName": null,
        "aboutMe": {
          "id": "5a2e4470e4b0e4fa266e0efc",
          "firstName": "neet",
          "lastName": "yadav",
          "birthDate": null,
          "address": "Pune",
          "city": "Pune",
          "country": "india",
          "pincode": "411039",
          "gender": "male",
          "languagesSpeak": null,
          "additionalInfo": null,
          "state": "MH"
        },
        "contactInfo": {
          "id": "5a2e4470e4b0e4fa266e0efd",
          "email": "Neet@gmail.com",
          "phone": "8055802119",
          "smsNotification": false,
          "countryCode": null,
          "country": null,
          "emlNt": false
        },
        "patientInfo": {
          "id": "5a2e4a36e4b0e4fa266e0f7b",
          "lifeStyle": {
            "id": "5a2e4a36e4b0e4fa266e0f79",
            "medication": "Test",
            "alcoholUse": "yes",
            "allergiesToMedication": "Testing",
            "alcoholDrinksPerWeek": "Do not Drink",
            "medicalCondition": "Cancer",
            "allergies": "Pollen",
            "vitaminSupplements": "Test",
            "smoke": "1",
            "contactlenses": "Soft"
          },
          "familyHistory": {
            "id": "5a2e4a36e4b0e4fa266e0f7a",
            "description": null,
            "diseaseRelation": [
              {
                "conditions": "Cataract",
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
        "timezone": null,
        "createdAt": "2017-12-11 12:40 AM PST",
        "forgotPasswordToken": null,
        "familyMembers": null,
        "parentUser": null,
        "parentUserRelation": "brother",
        "password": null,
        "rating": null,
        "preferredPharmacy": null,
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
        "doctorsOrg": null,
        "twilioAccessToken": null,
        "invited": false,
        "validated": true,
        "activated": true,
        "managedUser": true,
        "addedByCpm": false,
        "pilotDoc": false
      }
    ],
    "parentUser": null,
    "parentUserRelation": null,
    "password": null,
    "rating": null,
    "preferredPharmacy": [
      {
        "id": "5a2c2efee4b0e4fa266e01b4",
        "name": "Mediplus store",
        "address": "hinjewadi phase-1",
        "email": "niteshy2391@gmail.com",
        "city": "pune",
        "state": "Maharashtra",
        "country": null,
        "zipCode": "411007",
        "phoneNumber": "9423505079",
        "validated": false
      },
      {
        "id": "5a2e22fce4b0e4fa266e09ec",
        "name": "Mediplus store",
        "address": "hinjewadi phase-1",
        "email": null,
        "city": "pune",
        "state": "Maharashtra",
        "country": null,
        "zipCode": "411007",
        "phoneNumber": "9423505079",
        "validated": false
      }
    ],
    "kandyUserName": null,
    "kandyUserPassword": null,
    "kandyFullUserId": null,
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": null,
    "profileImagePath": "https://eyes.cooldoctors.io/PRDIMAGE/patient/5a2c0a69e4b0e4fa266e0180/ProfileImage/dashboard2.png",
    "isReferredDoctor": null,
    "randomtoken": "5Ys5Ad",
    "isEmailVerified": false,
    "doctorsGroups": null,
    "preferredDoctors": [],
    "isAcceptTC": false,
    "insurenceCards": [],
    "notificationSettings": {
      "id": "5a2c0a69e4b0e4fa266e017e",
      "addTestreport": true,
      "addTreatmentPlan": true,
      "sendReminderForEyeTest": true,
      "sendReminderForMedicine": true,
      "sentMessage": true
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
    "invited": false,
    "validated": true,
    "activated": true,
    "managedUser": false,
    "addedByCpm": false,
    "pilotDoc": false
  },
  "prescription": null,
  "questionaire": {
    "id": "5a2e646ae4b0e4fa266e1a82",
    "questions": [
      {
        "id": "5a2e646ae4b0e4fa266e1a7c",
        "question": "Snellen chart Right Eye vision test",
        "answerType": "String",
        "answer": "20/30",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5a2e646ae4b0e4fa266e1a7d",
        "question": "Snellen chart Left Eye vision test",
        "answerType": "String",
        "answer": "20/25",
        "param1": null,
        "param2": null,
        "param3": null
      }
    ],
    "symptoms": null,
    "frequency": null,
    "severity": null,
    "treatment": [
      {
        "id": "5a2e646ae4b0e4fa266e1a7e",
        "question": "Are you taking medications?",
        "answerType": "String",
        "answer": "",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5a2e646ae4b0e4fa266e1a7f",
        "question": "Are you taking Omega 3 supplements?",
        "answerType": "String",
        "answer": "",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5a2e646ae4b0e4fa266e1a80",
        "question": "Are you doing warm compresses?",
        "answerType": "String",
        "answer": "",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5a2e646ae4b0e4fa266e1a81",
        "question": "Are you using eye drops?",
        "answerType": "String",
        "answer": "",
        "param1": null,
        "param2": null,
        "param3": null
      }
    ],
    "appointment": null,
    "lasikQuestionnaire": null,
    "contactLenseQuestions": null
  },
  "report": null,
  "todos": null,
  "speciality": {
    "id": "55b7802be4b0b393bf91678e",
    "name": null,
    "questionnaire": null,
    "report": null
  },
  "createdAt": "2017-12-11 02:56 AM PST",
  "appointmentPrice": 0,
  "status": "draft",
  "waitId": 0,
  "currentLocationState": null,
  "isReferredDoctorAvailable": null,
  "diseaseImageFilePath": null,
  "contactlenseImageFilePath": null,
  "patientPreferredVisitLanguage": null,
  "symtons": "Dry Eye",
  "createdBy": "5a2c0a69e4b0e4fa266e0180",
  "paymentStatus": null,
  "visionTest": null,
  "videoVisitPath": null,
  "remark": null,
  "callReceivedStatus": false,
  "files": null,
  "needFollowUp": false,
  "pharmacy": [
    {
      "id": "5a2c2efee4b0e4fa266e01b4",
      "name": "Mediplus store",
      "address": "hinjewadi phase-1",
      "email": "niteshy2391@gmail.com",
      "city": "pune",
      "state": "Maharashtra",
      "country": null,
      "zipCode": "411007",
      "phoneNumber": "9423505079",
      "validated": false
    },
    {
      "id": "5a2e22fce4b0e4fa266e09ec",
      "name": "Mediplus store",
      "address": "hinjewadi phase-1",
      "email": null,
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
```

> Make sure to replace `X-Auth-Token` with your API key.

Save draft visit. User can edit this later and complete to make an appointment.

For saving appointment just pass “draft” in status parameter. 


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/doctor/createVisitWithAvailability
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
  | **Speciality** |   |
ID | ID of Speciality | String | Required
  | ** Questionnaire 
     array has  all questions and answers sendt in the visit to the doctor** |   |
ID | Questionnaire ID | Integer | Required
Questions | Questions | String | Required
ID | ID | Integer | Optional
Question2 | Questions | String | Optional
AnswerType | Answer Type | Boolean | Optional
Answer | answer (Y/N) | String | Optional
Appointment | Appointment | String | Optional
availabilityTimeSlot | Availability time should be pass as per doctor avaibility time. | String | Optional
status | Draft for saving appointment just pass”draft” | String | Required

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


## Reschedule upcoming visit

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X POST "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/reschedule/5a2e65fee4b0e4fa266e1bb5" -d '{"doctor":{"id":"56fb7614e4b0d3123cea4925"},"availabilityTimeSlot":{ "id" : "5a2e5bdce4b0e4fa266e167f"}}'

```

> The above command returns JSON structured like this:

```json
{
  "id": "5a2e65fee4b0e4fa266e1bb5",
  "startDate": "2017-12-17 12:20 PM UTC",
  "endDate": "2017-12-17 12:30 PM UTC",
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
          "degree": "    Bca",
          "university": "   un",
          "yearOfPasssing": "   88778"
        }
      ],
      "hospitalAttachedWithList": [
        {
          "id": "59e09cbce4b0a70b0de5b0c4",
          "name": "   ng tt",
          "city": "    Pune",
          "country": "   India"
        }
      ],
      "awardsReceivedList": [
        {
          "id": "59e09cbce4b0a70b0de5b0c5",
          "name": "q",
          "description": "    • • • • • • •  •  •  •  Description",
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
      "bio": "Dr. Moshe Mendelson is one of the prominent optometrists based in the silicon valley and has over 25 years of experience. He is Fellow of the International Academy of Orthokeratology and has treated thousands of patients in his career. Dr. Mendelson received his doctorate from the University of California, Berkeley and trained at Veterans Administration Hospital at Stanford Medical Center, Oak Knoll Naval Hospital, Pacific Presbyterian Medical Center. Formerly, he was Adjunct Professor for the New England College of Optometry and Salus University. He is a sought after speaker and travels around the world to speak at conferences and teaches optometry students from colleges around the country.\n\n\n\"I am passionate about using technological advances in telemedicine to be able to treat patients at a fraction of the cost. Telemedicine allows us to treat patients around the world who don't have easy access to good eye care\"",
      "profession": "Optometrist",
      "availabilityTimeZone": "America/Los_Angeles",
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
    "preferredPharmacy": null,
    "kandyUserName": null,
    "kandyUserPassword": null,
    "kandyFullUserId": null,
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": null,
    "profileImagePath": "https://dev.api.cooldoctors.io:8443/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsuper.png",
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
    "id": "5a2c0a69e4b0e4fa266e0180",
    "email": "patientuser@cooldoctors.io",
    "pharmacyName": null,
    "pharmacyAddress": null,
    "profileImageId": null,
    "profileImageName": null,
    "aboutMe": {
      "id": "5a2c0a69e4b0e4fa266e017d",
      "firstName": "Patient",
      "lastName": "Name",
      "birthDate": null,
      "address": "Kallam Anji Reddy Campus, Banjara Hills",
      "city": "Hyderabad",
      "country": "India",
      "pincode": "500034",
      "gender": "Female",
      "languagesSpeak": null,
      "additionalInfo": null,
      "state": "Telangana"
    },
    "contactInfo": {
      "id": "5a2c0a69e4b0e4fa266e017f",
      "email": "patientuser@cooldoctors.io",
      "phone": "8806900740",
      "smsNotification": false,
      "countryCode": null,
      "country": null,
      "emlNt": false
    },
    "patientInfo": {
      "id": "5a2e1e23e4b0e4fa266e0805",
      "lifeStyle": {
        "id": "5a2e1e23e4b0e4fa266e0803",
        "medication": "Test",
        "alcoholUse": "yes",
        "allergiesToMedication": "Testing",
        "alcoholDrinksPerWeek": "Do not Drink",
        "medicalCondition": "Cancer",
        "allergies": "Pollen",
        "vitaminSupplements": "Test",
        "smoke": "1",
        "contactlenses": "Soft"
      },
      "familyHistory": {
        "id": "5a2e1e23e4b0e4fa266e0804",
        "description": null,
        "diseaseRelation": [
          {
            "conditions": "Cataract",
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
    "createdAt": "2017-12-09 08:08 AM PST",
    "forgotPasswordToken": null,
    "familyMembers": [
      {
        "id": "5a2c1827e4b0e4fa266e018f",
        "email": "ESa6zdCf@eyecarelive.com",
        "pharmacyName": null,
        "pharmacyAddress": null,
        "profileImageId": "5a2c31a9e4b0e4fa266e01bf",
        "profileImageName": "0-cus-d1-b928632e6fef67a90ca8ecd0121882bb.jpg",
        "aboutMe": {
          "id": "5a2c1827e4b0e4fa266e018d",
          "firstName": "neet",
          "lastName": "yadav",
          "birthDate": null,
          "address": "Pune",
          "city": "Pune",
          "country": "india",
          "pincode": "411039",
          "gender": "male",
          "languagesSpeak": null,
          "additionalInfo": null,
          "state": "MH"
        },
        "contactInfo": {
          "id": "5a2c1827e4b0e4fa266e018e",
          "email": "Neet@gmail.com",
          "phone": "8055802119",
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
        "createdAt": "2017-12-09 09:06 AM PST",
        "forgotPasswordToken": null,
        "familyMembers": null,
        "parentUser": null,
        "parentUserRelation": "brother",
        "password": null,
        "rating": null,
        "preferredPharmacy": null,
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
        "doctorsOrg": null,
        "twilioAccessToken": null,
        "invited": false,
        "validated": true,
        "activated": true,
        "managedUser": true,
        "addedByCpm": false,
        "pilotDoc": false
      },
      {
        "id": "5a2e4470e4b0e4fa266e0efe",
        "email": "8BQH25JS@eyecarelive.com",
        "pharmacyName": null,
        "pharmacyAddress": null,
        "profileImageId": null,
        "profileImageName": null,
        "aboutMe": {
          "id": "5a2e4470e4b0e4fa266e0efc",
          "firstName": "neet",
          "lastName": "yadav",
          "birthDate": null,
          "address": "Pune",
          "city": "Pune",
          "country": "india",
          "pincode": "411039",
          "gender": "male",
          "languagesSpeak": null,
          "additionalInfo": null,
          "state": "MH"
        },
        "contactInfo": {
          "id": "5a2e4470e4b0e4fa266e0efd",
          "email": "Neet@gmail.com",
          "phone": "8055802119",
          "smsNotification": false,
          "countryCode": null,
          "country": null,
          "emlNt": false
        },
        "patientInfo": {
          "id": "5a2e4a36e4b0e4fa266e0f7b",
          "lifeStyle": {
            "id": "5a2e4a36e4b0e4fa266e0f79",
            "medication": "Test",
            "alcoholUse": "yes",
            "allergiesToMedication": "Testing",
            "alcoholDrinksPerWeek": "Do not Drink",
            "medicalCondition": "Cancer",
            "allergies": "Pollen",
            "vitaminSupplements": "Test",
            "smoke": "1",
            "contactlenses": "Soft"
          },
          "familyHistory": {
            "id": "5a2e4a36e4b0e4fa266e0f7a",
            "description": null,
            "diseaseRelation": [
              {
                "conditions": "Cataract",
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
        "timezone": null,
        "createdAt": "2017-12-11 12:40 AM PST",
        "forgotPasswordToken": null,
        "familyMembers": null,
        "parentUser": null,
        "parentUserRelation": "brother",
        "password": null,
        "rating": null,
        "preferredPharmacy": null,
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
        "doctorsOrg": null,
        "twilioAccessToken": null,
        "invited": false,
        "validated": true,
        "activated": true,
        "managedUser": true,
        "addedByCpm": false,
        "pilotDoc": false
      }
    ],
    "parentUser": null,
    "parentUserRelation": null,
    "password": null,
    "rating": null,
    "preferredPharmacy": [
      {
        "id": "5a2c2efee4b0e4fa266e01b4",
        "name": "Mediplus store",
        "address": "hinjewadi phase-1",
        "email": "niteshy2391@gmail.com",
        "city": "pune",
        "state": "Maharashtra",
        "country": null,
        "zipCode": "411007",
        "phoneNumber": "9423505079",
        "validated": false
      },
      {
        "id": "5a2e22fce4b0e4fa266e09ec",
        "name": "Mediplus store",
        "address": "hinjewadi phase-1",
        "email": null,
        "city": "pune",
        "state": "Maharashtra",
        "country": null,
        "zipCode": "411007",
        "phoneNumber": "9423505079",
        "validated": false
      }
    ],
    "kandyUserName": null,
    "kandyUserPassword": null,
    "kandyFullUserId": null,
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": null,
    "profileImagePath": "https://eyes.cooldoctors.io/PRDIMAGE/patient/5a2c0a69e4b0e4fa266e0180/ProfileImage/dashboard2.png",
    "isReferredDoctor": null,
    "randomtoken": "5Ys5Ad",
    "isEmailVerified": false,
    "doctorsGroups": null,
    "preferredDoctors": [],
    "isAcceptTC": false,
    "insurenceCards": [],
    "notificationSettings": {
      "id": "5a2c0a69e4b0e4fa266e017e",
      "addTestreport": true,
      "addTreatmentPlan": true,
      "sendReminderForEyeTest": true,
      "sendReminderForMedicine": true,
      "sentMessage": true
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
    "invited": false,
    "validated": true,
    "activated": true,
    "managedUser": false,
    "addedByCpm": false,
    "pilotDoc": false
  },
  "prescription": null,
  "questionaire": {
    "id": "5a2e65fee4b0e4fa266e1bb4",
    "questions": [
      {
        "id": "5a2e65fee4b0e4fa266e1bae",
        "question": "Snellen chart Right Eye vision test",
        "answerType": "String",
        "answer": "20/30",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5a2e65fee4b0e4fa266e1baf",
        "question": "Snellen chart Left Eye vision test",
        "answerType": "String",
        "answer": "20/25",
        "param1": null,
        "param2": null,
        "param3": null
      }
    ],
    "symptoms": null,
    "frequency": null,
    "severity": null,
    "treatment": [
      {
        "id": "5a2e65fee4b0e4fa266e1bb0",
        "question": "Are you taking medications?",
        "answerType": "String",
        "answer": "",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5a2e65fee4b0e4fa266e1bb1",
        "question": "Are you taking Omega 3 supplements?",
        "answerType": "String",
        "answer": "",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5a2e65fee4b0e4fa266e1bb2",
        "question": "Are you doing warm compresses?",
        "answerType": "String",
        "answer": "",
        "param1": null,
        "param2": null,
        "param3": null
      },
      {
        "id": "5a2e65fee4b0e4fa266e1bb3",
        "question": "Are you using eye drops?",
        "answerType": "String",
        "answer": "",
        "param1": null,
        "param2": null,
        "param3": null
      }
    ],
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
  "createdAt": "2017-12-11 03:03 AM PST",
  "appointmentPrice": 0,
  "status": "pending",
  "waitId": 0,
  "currentLocationState": null,
  "isReferredDoctorAvailable": null,
  "diseaseImageFilePath": null,
  "contactlenseImageFilePath": null,
  "patientPreferredVisitLanguage": null,
  "symtons": "Dry Eye",
  "createdBy": "5a2c0a69e4b0e4fa266e0180",
  "paymentStatus": null,
  "visionTest": null,
  "videoVisitPath": null,
  "remark": null,
  "callReceivedStatus": false,
  "files": null,
  "needFollowUp": false,
  "pharmacy": [
    {
      "id": "5a2c2efee4b0e4fa266e01b4",
      "name": "Mediplus store",
      "address": "hinjewadi phase-1",
      "email": "niteshy2391@gmail.com",
      "city": "pune",
      "state": "Maharashtra",
      "country": null,
      "zipCode": "411007",
      "phoneNumber": "9423505079",
      "validated": false
    },
    {
      "id": "5a2e22fce4b0e4fa266e09ec",
      "name": "Mediplus store",
      "address": "hinjewadi phase-1",
      "email": null,
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
  "availabilityTimeSlot": {
    "id": "5a2e5bdce4b0e4fa266e167f",
    "startTime": "12",
    "sTime": "2017-12-17 12:20 PM UTC",
    "eTime": "2017-12-17 12:30 PM UTC",
    "slotNumber": "2",
    "patient": null,
    "visitType": null,
    "appointmentId": "5a2e65fee4b0e4fa266e1bb5",
    "status": "enable",
    "booked": true
  },
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
```

> Make sure to replace `X-Auth-Token` with your API key.

Reschedule upcoming visit. Updates the date and time for the same visit type

Create appointment id need to pass with book slot.


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/reschedule/{AppointmentID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{Appointment ID} | For Reschedule appointment pass appointment ID | Integer | Required
doctor | Pass the selected or preferred doctor ID | String | Required
availabilityTimeSlot | Pass the new availability time slot as doctors availbility  | String | Required

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


## Get all visits

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/getPatientHistory/5a2c0a69e4b0e4fa266e0180"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "5a2c3534e4b0e4fa266e01cc",
    "startDate": "2017-12-09 11:10 AM PST",
    "endDate": "2017-12-09 11:25 AM PST",
    "doctor": {
      "id": "58e2268be4b0b3b8e551c825",
      "email": "doctor@cooldoctors.io",
      "pharmacyName": null,
      "pharmacyAddress": null,
      "profileImageId": null,
      "profileImageName": null,
      "aboutMe": {
        "id": "58e2268be4b0b3b8e551c823",
        "firstName": "Raj",
        "lastName": "R",
        "birthDate": "04/16/2017",
        "address": "1010 W Fremont Ave",
        "city": "Sunnyvale",
        "country": "USA",
        "pincode": "95014",
        "gender": " Male",
        "languagesSpeak": [
          "English",
          "",
          ""
        ],
        "additionalInfo": null,
        "state": "CA"
      },
      "contactInfo": {
        "id": "58e2268be4b0b3b8e551c824",
        "email": "doctor@cooldoctors.io",
        "phone": "408-836-0196",
        "smsNotification": true,
        "countryCode": null,
        "country": null,
        "emlNt": false
      },
      "patientInfo": null,
      "doctorInfo": {
        "id": "59816f67e4b0de21cd3e5b9b",
        "educationList": null,
        "hospitalAttachedWithList": null,
        "awardsReceivedList": null,
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
            "id": "5665a2cc9a87399fa0b9ba53",
            "state": "NY"
          }
        ],
        "registrationNumber": "23232",
        "whyCoolDoctors": null,
        "bio": "Test",
        "profession": "Optometrist",
        "availabilityTimeZone": "America/Los_Angeles",
        "npi": ""
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
      "createdAt": "2017-04-03 12:40 PM CEST",
      "forgotPasswordToken": "x6xf7d",
      "familyMembers": null,
      "parentUser": null,
      "parentUserRelation": null,
      "password": null,
      "rating": null,
      "preferredPharmacy": null,
      "kandyUserName": null,
      "kandyUserPassword": null,
      "kandyFullUserId": null,
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://dev.api.cooldoctors.io:8443/PRDIMAGE/doctor/58e2268be4b0b3b8e551c825/ProfileImage/Careers-after-MBA-for-doctor.jpg",
      "isReferredDoctor": null,
      "randomtoken": "Qrx9Fz",
      "isEmailVerified": false,
      "doctorsGroups": null,
      "preferredDoctors": [
        "56fb7614e4b0d3123cea4925"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58e24d29e4b03eb392b1d5b3",
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "patient": {
      "id": "5a2c0a69e4b0e4fa266e0180",
      "email": "patientuser@cooldoctors.io",
      "pharmacyName": null,
      "pharmacyAddress": null,
      "profileImageId": null,
      "profileImageName": null,
      "aboutMe": {
        "id": "5a2c0a69e4b0e4fa266e017d",
        "firstName": "Patient",
        "lastName": "Name",
        "birthDate": null,
        "address": "Kallam Anji Reddy Campus, Banjara Hills",
        "city": "Hyderabad",
        "country": "India",
        "pincode": "500034",
        "gender": "Female",
        "languagesSpeak": null,
        "additionalInfo": null,
        "state": "Telangana"
      },
      "contactInfo": {
        "id": "5a2c0a69e4b0e4fa266e017f",
        "email": "patientuser@cooldoctors.io",
        "phone": "8806900740",
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
      "timezone": {
        "id": "55f283b4e4b029528c27d0c5",
        "timezone": "Asia/Kolkata",
        "displayName": "India Standard Time"
      },
      "createdAt": "2017-12-09 08:08 AM PST",
      "forgotPasswordToken": null,
      "familyMembers": [
        {
          "id": "5a2c1827e4b0e4fa266e018f",
          "email": "ESa6zdCf@eyecarelive.com",
          "pharmacyName": null,
          "pharmacyAddress": null,
          "profileImageId": "5a2c31a9e4b0e4fa266e01bf",
          "profileImageName": "0-cus-d1-b928632e6fef67a90ca8ecd0121882bb.jpg",
          "aboutMe": {
            "id": "5a2c1827e4b0e4fa266e018d",
            "firstName": "neet",
            "lastName": "yadav",
            "birthDate": null,
            "address": "Pune",
            "city": "Pune",
            "country": "india",
            "pincode": "411039",
            "gender": "male",
            "languagesSpeak": null,
            "additionalInfo": null,
            "state": "MH"
          },
          "contactInfo": {
            "id": "5a2c1827e4b0e4fa266e018e",
            "email": "Neet@gmail.com",
            "phone": "8055802119",
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
          "createdAt": "2017-12-09 09:06 AM PST",
          "forgotPasswordToken": null,
          "familyMembers": null,
          "parentUser": null,
          "parentUserRelation": "brother",
          "password": null,
          "rating": null,
          "preferredPharmacy": null,
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
          "doctorsOrg": null,
          "twilioAccessToken": null,
          "invited": false,
          "validated": true,
          "activated": true,
          "managedUser": true,
          "addedByCpm": false,
          "pilotDoc": false
        }
      ],
      "parentUser": null,
      "parentUserRelation": null,
      "password": null,
      "rating": null,
      "preferredPharmacy": [
        {
          "id": "5a2c2efee4b0e4fa266e01b4",
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
      "kandyUserName": "bhrjnrp47t",
      "kandyUserPassword": "3ab1be12793b48",
      "kandyFullUserId": "bhrjnrp47t@cmobrtctest.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://eyes.cooldoctors.io/PRDIMAGE/patient/5a2c0a69e4b0e4fa266e0180/ProfileImage/dashboard2.png",
      "isReferredDoctor": null,
      "randomtoken": "5Ys5Ad",
      "isEmailVerified": false,
      "doctorsGroups": null,
      "preferredDoctors": [],
      "isAcceptTC": false,
      "insurenceCards": null,
      "notificationSettings": {
        "id": "5a2c0a69e4b0e4fa266e017e",
        "addTestreport": true,
        "addTreatmentPlan": true,
        "sendReminderForEyeTest": true,
        "sendReminderForMedicine": true,
        "sentMessage": true
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
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": false
    },
    "prescription": null,
    "questionaire": {
      "id": "5a2c3534e4b0e4fa266e01cb",
      "questions": [
        {
          "id": "5a2c3534e4b0e4fa266e01c9",
          "question": "I have red eye since last 10 days",
          "answerType": "String",
          "answer": "",
          "param1": null,
          "param2": null,
          "param3": null
        },
        {
          "id": "5a2c3534e4b0e4fa266e01ca",
          "question": "red eye",
          "answerType": "yes or no",
          "answer": "",
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
    "createdAt": "2017-12-09 11:10 AM PST",
    "appointmentPrice": 0,
    "status": "pending",
    "waitId": 0,
    "currentLocationState": "NY",
    "isReferredDoctorAvailable": null,
    "diseaseImageFilePath": null,
    "contactlenseImageFilePath": null,
    "patientPreferredVisitLanguage": null,
    "symtons": "red eye",
    "createdBy": "5a2c0a69e4b0e4fa266e0180",
    "paymentStatus": null,
    "visionTest": {
      "id": "563a0938e4b0d26ed7ce6237",
      "leftVisualAcuity": "20/50",
      "rightVisualAcuity": "20/70"
    },
    "videoVisitPath": null,
    "remark": null,
    "callReceivedStatus": false,
    "files": null,
    "needFollowUp": false,
    "pharmacy": [
      {
        "id": "5a2c2efee4b0e4fa266e01b4",
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
    "visitType": null,
    "visitPurpose": null,
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
    "paymentMode": null,
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

Get history of visits with full details of each visit. Includes visit type, questionnaire filled, images, video and any eye vision tests data available for each visit. The details also include treatment plan, prescriptions and medication reminders



### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/appointment/getPatientHistory/{PatientID}" 
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{PatientID} | Patient ID pass for appointment | String | Required

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
Role | Role | String


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Upload images for an appointment visit

```shell
curl -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:multipart/form-data" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/diseaseImagesNew" -X POST -F file=@/Users/cupertino/Downloads/2_user.png  -F side=left -F file=@/Users/cupertino/Downloads/2_user.png -F side=right
```

> The above command returns JSON structured like this:

```json
{
  "id": "5a2e6dfce4b0e4fa266e1e51",
  "disesFolderId": null,
  "fileName": [
    "1512992252224,https://s3.amazonaws.com/test-nakul/patient/5a2c0a69e4b0e4fa266e0180/DiseaseImage/1512992252224/2_user.png",
    "1512992252356,https://s3.amazonaws.com/test-nakul/patient/5a2c0a69e4b0e4fa266e0180/DiseaseImage/1512992252356/2_user.png"
  ],
  "side": [
    "left",
    "right"
  ],
  "status": null,
  "lense": null
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Upload photos and videos for an scheduled appointment

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/diseaseImagesNew 
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
-F file=@/FilePath | Pass the image path after @ | String | Required
Pass side=left/right | Image should have Left Or Right side | String | Required

### Response

Parameter | Description | Type
--------- | ----------- | ----
id | ID will be disease image unique ID | Integer
disesFolderId | Deprecated | String
fileName[] | FileName is array of the file with file ID and url | String
side[] | side array of the image sides | String
status | Deprecated | String
lense | Deprecated | String



`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Get images for an appointment visit


```shell
curl -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:multipart/form-data" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/diseaseImages/5a2e6dfce4b0e4fa266e1e51" -X GET
```

> The above command returns JSON structured like this:

```json
{
  "id": "5a2e6dfce4b0e4fa266e1e51",
  "disesFolderId": null,
  "fileName": [
    "1512992252224,https://s3.amazonaws.com/test-nakul/patient/5a2c0a69e4b0e4fa266e0180/DiseaseImage/1512992252224/2_user.png",
    "1512992252356,https://s3.amazonaws.com/test-nakul/patient/5a2c0a69e4b0e4fa266e0180/DiseaseImage/1512992252356/2_user.png"
  ],
  "side": [
    "left",
    "right"
  ],
  "status": null,
  "lense": null
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Get list of all images by appointment. 

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/diseaseImages/{diseaseImagesID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{diseaseImagesID} | Need to pass disease image ID | Integer | Required

### Response

Parameter | Description | Type
--------- | ----------- | ----
id | ID will be disease image unique ID | Integer
disesFolderId | Deprecated | String
fileName[] | FileName is array of the file with file ID and url | String
side[] | side array of the image sides | String
status | Deprecated | String
lense | Deprecated | String



`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## View Disease Images or download image use following API


```shell
curl -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:multipart/form-data" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/getDiseaseImage/1512899976338/5a2d0588e4b0e4fa266e028f" -X GET 

```

> The above command returns JSON structured like this:

```json
{
  "url": "https://d5qf5duw6o0fe.cloudfront.net/patient/5a2c0a69e4b0e4fa266e0180/DiseaseImage/1512899976338/2_user.png?Expires=1512902784&Signature=fCnGu8DMs-p2T0HhwkDFo-dAGiZxJ~njgAhUTD90ynyP-Gz~Bs-sC6aVaSriAEYC1D~MvIxIXfp8CJVPlAWXa83ey5~6v-bCAnpaYw9mctcw0UUOjAz2gANm9FgdIvxVwzCTbNkwCRGDMNvqCuMGUJdLkxIvk00A12hoLddpnMrknLW2PLc0asHqjMay2SEL~CbkQQStDRKXOEpXjWk4eRwxo~jlvq4XAjCUToLv9gs0SaiteLqPkWrPAp~0MEJGTA5Xm72jJJgWU8XVgt8iH0~mA5TlBJcDvhPlmZmPe7~mFShWpDRBxZ6uBw~5Mlhf4U8BRDqZoaYg39g-xzSYEA__&Key-Pair-Id=APKAJKM62WTRWOS5N27Q"
}
```

> Make sure to replace `X-Auth-Token` with your API key.

View Disease Images or download image use following API

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/diseaseImages/{diseaseImagesID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{diseaseImagesID} | Need to pass disease image ID | Integer | Required

### Response

Parameter | Description | Type
--------- | ----------- | ----
id | ID will be disease image unique ID | Integer
disesFolderId | Deprecated | String
fileName[] | FileName is array of the file with file ID and url | String
side[] | side array of the image sides | String
status | Deprecated | String
lense | Deprecated | String



`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

