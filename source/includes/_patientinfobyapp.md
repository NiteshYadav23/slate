

# Patient Info By Appoointment

## Get All Eye photos of Patients 

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/getAllDiseaseImageOfPatient/5742c31ae4b0e03acf77f054"

```

> The above command returns JSON structured like this:

```json
{
  "symtons": "Contact lens",
  "status": null,
  "createdAt": "2017-06-15 11:35 PM PDT",
  "questionaire": null,
  "todos": null,
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
  "diseaseImageFilePath": {
    "id": "59437c0fe4b0103debeb425e",
    "disesFolderId": null,
    "fileName": [
      "1497594895250,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/DiseaseImage/1497594895250/img_436873LeftEye.jpg",
      "1497594895421,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/DiseaseImage/1497594895421/img_357798dRightEye.jpg",
      "1497594895555,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/DiseaseImage/1497594895555/img_843141leftEyeVodio.mp4",
      "1497594895740,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/DiseaseImage/1497594895740/img_567287rightEyeVodio.mp4"
    ],
    "side": [
      "left",
      "right  ",
      "left Video",
      "right_video"
    ],
    "status": null,
    "lense": null
  },
  "contactlenseImageFilePath": {
    "id": "59437be3e4b0103debeb4252",
    "disesFolderId": null,
    "fileName": [
      "1497594850308,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/DiseaseImage/1497594850308/img_707420LeftEye.jpg",
      "1497594850632,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/DiseaseImage/1497594850632/img_365123dRightEye.jpg",
      "1497594850956,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/DiseaseImage/1497594850956/img_278519leftEyeVodio.mp4",
      "1497594851131,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/DiseaseImage/1497594851131/img_617769rightEyeVodio.mp4"
    ],
    "side": [
      "left",
      "right  ",
      "left Video",
      "right_video"
    ],
    "status": null,
    "lense": "lense  ,lense  ,lense  ,lense  "
  },
  "solutionBottleImage": null,
  "remark": null,
  "doctorInfo": null,
  "patientInfo": null,
  "patientAboutMe": null,
  "doctorProfileImage": null,
  "appointmentId": null,
  "needFollowUp": false,
  "doctorId": null,
  "files": null,
  "medicinePrescriptions": null
}
```


### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/getAllDiseaseImageOfPatient/{PatientID}
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{PatientID} | Pass Patient ID for get all disease images | String | Required


### Response

Parameter | Description | Type 
--------- | ----------- | ----
symtons | Symptoms name for appointment | String
status | Status of appointment Pending, Completed or canceled. | String
createdAt | Created timestamp for appointment | String
questionaire[{}] | This will return the questionnaires for the apponitment | String
aboutMe[{}] | Doctor’s details | String
diseaseImageFilePath[{}] | It will return the array with file ID and other details | String
side[{}] | Side of images | String
solutionBottleImage[{}] | Deprecated | String
doctorInfo[{}] | Doctor info details | String
specialities[{}] | Specialities details need to be fixed always | String
licencedState[{}] | Doctor’s licenced states | String
registrationNumber | Registartion number of doctor | String
whyCoolDoctors | Why eyecarelive - details.  | String
bio | Bio details need to be added by doctor  | String
profession | Add progfession | String
availabilityTimeZone | Doctor’s Availability time zone  | String
npi | Doctor’s NPI | String
patientInfo | Patient info Deprecated | String
patientAboutMe | Deprecated | String
doctorProfileImage | Deprecated | String
appointmentId | Deprecated | String
needFollowUp | Deprecated | String
 | **Other All parameters are Deprecated, Pleas igonre.** | 


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>


## Get First Ten Patient History

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/firstTenPatientHistory/5742c31ae4b0e03acf77f054"


```

> The above command returns JSON structured like this:

```json
{
  "symtons": "Distorted vision",
  "status": "pending",
  "createdAt": "2017-12-18 04:35 AM PST",
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
  "todos": null,
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
  "diseaseImageFilePath": null,
  "contactlenseImageFilePath": null,
  "solutionBottleImage": null,
  "remark": null,
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
  "patientInfo": null,
  "patientAboutMe": null,
  "doctorProfileImage": null,
  "appointmentId": null,
  "needFollowUp": false,
  "doctorId": null,
  "files": null,
  "medicinePrescriptions": null
}
```
In this Api, doctor will get all the patients information about appointment as Added Treatment Plan, Diagnosis & Assesment data is coming if doctor updated.

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/firstTenPatientHistory/{PatientID}
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{PatientID} | User’s email address | String | Required


### Response

Parameter | Description | Type 
--------- | ----------- | ----
symtons | Symptoms name for appointment | String
status | Status of appointment Pending, Completed or canceled. | String
createdAt | Created timestamp for appointment | String
questionaire[{}] | This will return the questionnaires for the apponitment | String
aboutMe[{}] | Doctor’s details | String
diseaseImageFilePath[{}] | It will return the array with file ID and other details | String
side[{}] | Side of images | String
solutionBottleImage[{}] | Deprecated | String
doctorInfo[{}] | Doctor info details | String
specialities[{}] | Specialities details need to be fixed always | String
licencedState[{}] | Doctor’s licenced states | String
registrationNumber | Registartion number of doctor | String
whyCoolDoctors | Why eyecarelive - details.  | String
bio | Bio details need to be added by doctor  | String
profession | Add progfession | String
availabilityTimeZone | Doctor’s Availability time zone  | String
npi | Doctor’s NPI | String
patientInfo | Patient info Deprecated | String
patientAboutMe | Deprecated | String
doctorProfileImage | Deprecated | String
appointmentId | Deprecated | String
needFollowUp | Deprecated | String
 | **Other All parameters are Deprecated, Pleas igonre.** | 


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Get Next Ten Patient History

```shell
DoctorOnDemand/api/doctor/appointment/nextTenPatientHistory/{PatientID}/{NumberOfPage}
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/nextTenPatientHistory/5742c31ae4b0e03acf77f054/1"

```

> The above command returns JSON structured like this:

```json
{
  "symtons": "Distorted vision",
  "status": "pending",
  "createdAt": "2017-12-18 04:35 AM PST",
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
  "todos": null,
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
  "diseaseImageFilePath": null,
  "contactlenseImageFilePath": null,
  "solutionBottleImage": null,
  "remark": null,
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
  "patientInfo": null,
  "patientAboutMe": null,
  "doctorProfileImage": null,
  "appointmentId": null,
  "needFollowUp": false,
  "doctorId": null,
  "files": null,
  "medicinePrescriptions": null
}
```
In this API need to pass the number of pages to load more appointments.

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/nextTenPatientHistory/{PatientID}/{NumberOfPage}
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{PatientID} | Need to pass patientID | String | Required
{NumberOfPage} | Need to pass number of page to be loaded next | String | Required


### Response

Parameter | Description | Type 
--------- | ----------- | ----
symtons | Symptoms name for appointment | String
status | Status of appointment Pending, Completed or canceled. | String
createdAt | Created timestamp for appointment | String
questionaire[{}] | This will return the questionnaires for the apponitment | String
aboutMe[{}] | Doctor’s details | String
diseaseImageFilePath[{}] | It will return the array with file ID and other details | String
side[{}] | Side of images | String
solutionBottleImage[{}] | Deprecated | String
doctorInfo[{}] | Doctor info details | String
specialities[{}] | Specialities details need to be fixed always | String
licencedState[{}] | Doctor’s licenced states | String
registrationNumber | Registartion number of doctor | String
whyCoolDoctors | Why eyecarelive - details.  | String
bio | Bio details need to be added by doctor  | String
profession | Add progfession | String
availabilityTimeZone | Doctor’s Availability time zone  | String
npi | Doctor’s NPI | String
patientInfo | Patient info Deprecated | String
patientAboutMe | Deprecated | String
doctorProfileImage | Deprecated | String
appointmentId | Deprecated | String
needFollowUp | Deprecated | String
 | **Other All parameters are Deprecated, Pleas igonre.** | 


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>


## Add Treatment Plan, Assessment, Diagnosis

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X POST "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/todo/5a37b5f6e4b00ad7ad9bf261" -d '{"patient":"5742c31ae4b0e03acf77f054","status":"0","appointment":"5a37b5f6e4b00ad7ad9bf261","assessment":"Testing","diagnosis":"Testing","treatmentPlan":"Testing"}'


```

> The above command returns JSON structured like this:

```json
{
  "id": "5a38052fe4b00ad7ad9bf5c2",
  "patient": "5742c31ae4b0e03acf77f054",
  "status": 0,
  "appointment": "5a37b5f6e4b00ad7ad9bf261",
  "assessment": "Testing",
  "diagnosis": "Testing",
  "treatmentPlan": "Testing",
  "updatedAt": "2017-12-18 10:13 AM PST"
}
```
In this API need to pass the number of pages to load more appointments.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/todo/{AppointmentID}
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{AppointmentID} | Appointment ID need to pass in URL | String | Required
patient | Need to pass the pateint ID | String | Required
status | Deprecreated | String | Optional
appointment | Appointment ID | String | Required
assessment | Write assessment for patient | String | Required
diagnosis | Write Diagnosis for patient | String | Required
treatmentPlan | Write Treatment Plan | String | Required


### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID | ID create from database | String
patient | User ID  | String
status | Token for accessing purpose  | String
appointment | Appointment ID  | String
assessment | Updated Assessment will return  | String
diagnosis | Updated Diagnosis will return | String
treatmentPlan | Updated Treatment Plan will return | String
updatedAt | Updated time  | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>


## Add Medicine Prescription

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X POST "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/addMedicinePrescription/5a37b5f6e4b00ad7ad9bf261" -d '[{"medicineName":"Eye drop","dosage":"3","frequencyHourPerDay":"4","totalDays":"6","type":"Drops"}]'

```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "5a380680e4b00ad7ad9bf5e3",
    "patientId": null,
    "appointmentId": "5a37b5f6e4b00ad7ad9bf261",
    "medicineName": "Eye drop",
    "dosage": "3",
    "frequencyHourPerDay": "4",
    "totalDays": "6",
    "createdAt": "2017-12-18 10:18 AM PST",
    "calculatedNoToSend": "6",
    "sendCount": null,
    "status": "enable",
    "type": "Drops",
    "firstReminderSend": false
  },
  {
    "id": "5a380765e4b00ad7ad9bf5f7",
    "patientId": null,
    "appointmentId": "5a37b5f6e4b00ad7ad9bf261",
    "medicineName": "Eye drop",
    "dosage": "3",
    "frequencyHourPerDay": "4",
    "totalDays": "6",
    "createdAt": "2017-12-18 10:22 AM PST",
    "calculatedNoToSend": "6",
    "sendCount": null,
    "status": "enable",
    "type": "Drops",
    "firstReminderSend": false
  }
]
```

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/getMedicinePrescription/{AppointmentID}
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{AppointmentID} | Appointment ID need to pass in URL | String | Required
medicineName | Medicine Name | String | Required
dosage | Dose | String | Required
frequencyHourPerDay | Frequency hour per day | String | Required
assessment | Write assessment for patient | String | Required
totalDays | TotalDays | String | Required
createdAt | Created At time stamp | String | Required


### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID | ID create from database | String
patientId | User ID or family member ID | String
appointmentId | Token for accessing purpose   | String
medicineName | Medicine Name | String
dosage | Dose   | String
frequencyHourPerDay | Frequency hour per day | String
totalDays | Total Days | String
createdAt | Created At time stamp | String
calculatedNoToSend | Deprecreated | String
sendCount | Deprecreated | String
status | Deprecreated | String
type | Drops or etc | String
firstReminderSend | False or True | String

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Get Medicine Prescription 

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/getMedicinePrescription/5a37b5f6e4b00ad7ad9bf261"

```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "5a380680e4b00ad7ad9bf5e3",
    "patientId": null,
    "appointmentId": "5a37b5f6e4b00ad7ad9bf261",
    "medicineName": "Eye drop",
    "dosage": "3",
    "frequencyHourPerDay": "4",
    "totalDays": "6",
    "createdAt": "2017-12-18 10:18 AM PST",
    "calculatedNoToSend": "6",
    "sendCount": null,
    "status": "enable",
    "type": "Drops",
    "firstReminderSend": false
  }
]
```

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/getMedicinePrescription/{AppointmentID}
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{AppointmentID} | Appointment ID need to pass in URL | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID | ID create from database | String
patientId | User ID or family member ID | String
appointmentId | Token for accessing purpose   | String
medicineName | Medicine Name | String
dosage | Dose   | String
frequencyHourPerDay | Frequency hour per day | String
totalDays | Total Days | String
createdAt | Created At time stamp | String
calculatedNoToSend | Deprecreated | String
sendCount | Deprecreated | String
status | Deprecreated | String
type | Drops or etc | String
firstReminderSend | False or True | String

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Add Test Report

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/getMedicinePrescription/5a37b5f6e4b00ad7ad9bf261"

```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "5a380680e4b00ad7ad9bf5e3",
    "patientId": null,
    "appointmentId": "5a37b5f6e4b00ad7ad9bf261",
    "medicineName": "Eye drop",
    "dosage": "3",
    "frequencyHourPerDay": "4",
    "totalDays": "6",
    "createdAt": "2017-12-18 10:18 AM PST",
    "calculatedNoToSend": "6",
    "sendCount": null,
    "status": "enable",
    "type": "Drops",
    "firstReminderSend": false
  }
]
```
This API use for add the test report information then as per this API gives success then need to upload report file for that we have second API please check below.


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/patientReportInfo/{AppointmentID}
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{AppointmentID} | Appointment ID need to pass in URL | String | Required
testName | Test name of the report file | String | Required
reportDate | Report date | String | Required
description | Write a content of description for the report | String | Required
tags | Need to pass “eyes” | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID | Created Database ID | String
fileId[] | This will return the number of ID for test reports.  | String
fileName[] | Filename of the test reported files.  | String
filePath | This will return the file path | String
testName | Test name of the report file   | String
remarks | Deprecreated  | String
description | Write a content of description for the report | String
tags | Need to pass “eyes” | String
uploadDate | Upload date  | String
reportDate | Report date  | String
contentTypes[] | ["image/jpeg","application/octet-stream"] | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Add Test Report File

```shell
curl -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -H "Content-Type:multipart/form-data" "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/patientReport/5a37b5f6e4b00ad7ad9bf261/5a3808c3e4b00ad7ad9bf615" -X POST -F file=@/Users/cupertino/Desktop/FlashquoteWhite.png

```

> The above command returns JSON structured like this:

```json
{
  "id": "5a3808c3e4b00ad7ad9bf615",
  "fileId": [
    "1513621700401",
    "1513622298684"
  ],
  "fileName": [
    "1513148262759.JPEG",
    "FlashquoteWhite.png"
  ],
  "filePath": [
    "https://s3.amazonaws.com/test-nakul/doctor/56fb7614e4b0d3123cea4925/testResult/1513621700123/1513148262759.JPEG",
    "https://s3.amazonaws.com/test-nakul/doctor/56fb7614e4b0d3123cea4925/testResult/1513622298597/FlashquoteWhite.png"
  ],
  "testName": "Testing",
  "remarks": null,
  "description": "test",
  "tags": "eyes",
  "uploadDate": "2017-12-18 10:28 AM PST",
  "reportDate": "12/18/2017",
  "contentTypes": [
    "image/jpeg",
    "application/octet-stream"
  ]
}
```
This API use for add the test report information then as per this API gives success then need to upload report file for that we have second API please check below.


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/patientReportInfo/{AppointmentID}/{TestReportAdded_ID}
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{AppointmentID} | Appointment ID need to pass in URL | String | Required
{TestReportAdded_ID} | Test Report ID need to pass | String | Required
 -F file=@/FilePath | Need to pass the file path | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID | Created Database ID | String
fileId[] | This will return the number of ID for test reports.  | String
fileName[] | Filename of the test reported files.  | String
filePath | This will return the file path | String
testName | Test name of the report file   | String
remarks | Deprecreated  | String
description | Write a content of description for the report | String
tags | Need to pass “eyes” | String
uploadDate | Upload date  | String
reportDate | Report date  | String
contentTypes[] | ["image/jpeg","application/octet-stream"] | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Show All Amsler Test

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/getEyeTestByPatientAndTestName/amsler/5742c31ae4b0e03acf77f054"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "580dedbee4b01aaee5501717",
    "testName": "amsler",
    "createdDate": "2016-10-24 01:17 PM CEST",
    "user": "5742c31ae4b0e03acf77f054",
    "createdBy": "5742c31ae4b0e03acf77f054",
    "eyeSides": [
      {
        "eyeSide": "left",
        "eyeImages": "1477307848382,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/eyetests/1477307848382/img_159238front.jpg",
        "amsler_blue": "0",
        "amsler_green": "0",
        "amsler_black": "0",
        "amsler_orange": "0",
        "leftVisualAcuity": null,
        "rightVisualAcuity": null
      },
      {
        "eyeSide": "right",
        "eyeImages": "1477307848622,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/eyetests/1477307848622/img_143517dback.jpg",
        "amsler_blue": "0",
        "amsler_green": "0",
        "amsler_black": "0",
        "amsler_orange": "0",
        "leftVisualAcuity": null,
        "rightVisualAcuity": null
      }
    ],
    "firstReminderSend": true,
    "secondReminderSend": true,
    "thirdReminderSend": true,
    "fourthReminderSend": true
  },
  {
    "id": "580dd895e4b01aaee54ff373",
    "testName": "amsler",
    "createdDate": "2016-10-24 11:47 AM CEST",
    "user": "5742c31ae4b0e03acf77f054",
    "createdBy": "5742c31ae4b0e03acf77f054",
    "eyeSides": [
      {
        "eyeSide": "left",
        "eyeImages": "1477302512715,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/eyetests/1477302512715/img_945860front.jpg",
        "amsler_blue": "0",
        "amsler_green": "0",
        "amsler_black": "0",
        "amsler_orange": "0",
        "leftVisualAcuity": null,
        "rightVisualAcuity": null
      },
      {
        "eyeSide": "right",
        "eyeImages": "1477302512806,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/eyetests/1477302512806/img_658846dback.jpg",
        "amsler_blue": "0",
        "amsler_green": "0",
        "amsler_black": "0",
        "amsler_orange": "0",
        "leftVisualAcuity": null,
        "rightVisualAcuity": null
      }
    ],
    "firstReminderSend": false,
    "secondReminderSend": false,
    "thirdReminderSend": false,
    "fourthReminderSend": false
  }
]
```
This API use for add the test report information then as per this API gives success then need to upload report file for that we have second API please check below.


### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/getEyeTestByPatientAndTestName/amsler/{PatientUserID}
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{PatientID} | Need to pass the patient id in get URL | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID | Database ID | String
testName | Test name like Halo, Amsler    | String
createdDate | Created Date and time  | String
user | User's ID  | String
createdBy | Created by means if main user ID | String
eyeSides[{}] | Eye sides have file ID and details of halo test | String
firstReminderSend | This the the reminder for user to know 3 months completed for eye test | String
secondReminderSend | This the the reminder for user to know 3 months completed for eye test | String
thirdReminderSend | This the the reminder for user to know 3 months completed for eye test | String
fourthReminderSend | This the the reminder for user to know 3 months completed for eye test  | String
reportDate | Report date  | String
contentTypes[] | ["image/jpeg","application/octet-stream"] | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Show All Halo Test

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/getEyeTestByPatientAndTestName/halo/5742c31ae4b0e03acf77f054"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "5931126ce4b0e21c5150d6b8",
    "testName": "halo",
    "createdDate": "2017-06-02 12:23 AM PDT",
    "user": "5742c31ae4b0e03acf77f054",
    "createdBy": "5742c31ae4b0e03acf77f054",
    "eyeSides": [
      {
        "eyeSide": "left",
        "eyeImages": "1496388205560,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/eyetests/1496388205560/img_451784front.jpg",
        "amsler_blue": "0",
        "amsler_green": "0",
        "amsler_black": "0",
        "amsler_orange": "0",
        "leftVisualAcuity": null,
        "rightVisualAcuity": null
      },
      {
        "eyeSide": "right",
        "eyeImages": "1496388205959,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/eyetests/1496388205959/img_804734dback.jpg",
        "amsler_blue": "0",
        "amsler_green": "0",
        "amsler_black": "0",
        "amsler_orange": "0",
        "leftVisualAcuity": null,
        "rightVisualAcuity": null
      }
    ],
    "firstReminderSend": true,
    "secondReminderSend": true,
    "thirdReminderSend": true,
    "fourthReminderSend": true
  },
  {
    "id": "59259f7ce4b0d1269ffee7af",
    "testName": "halo",
    "createdDate": "2017-05-24 07:58 AM PDT",
    "user": "5742c31ae4b0e03acf77f054",
    "createdBy": "5742c31ae4b0e03acf77f054",
    "eyeSides": [
      {
        "eyeSide": "left",
        "eyeImages": "1495637887431,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/eyetests/1495637887431/img_797961front.jpg",
        "amsler_blue": "0",
        "amsler_green": "0",
        "amsler_black": "0",
        "amsler_orange": "0",
        "leftVisualAcuity": null,
        "rightVisualAcuity": null
      },
      {
        "eyeSide": "right",
        "eyeImages": "1495637887680,https://s3.amazonaws.com/test-nakul/doctor/5742c31ae4b0e03acf77f054/eyetests/1495637887680/img_433075dback.jpg",
        "amsler_blue": "0",
        "amsler_green": "0",
        "amsler_black": "0",
        "amsler_orange": "0",
        "leftVisualAcuity": null,
        "rightVisualAcuity": null
      }
    ],
    "firstReminderSend": true,
    "secondReminderSend": true,
    "thirdReminderSend": false,
    "fourthReminderSend": false
  }
]
```


### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/getEyeTestByPatientAndTestName/halo/{PatientUserID}
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{PatientID} | Patient ID for get HALO test | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID | Database ID | String
testName | Test name like Halo, Amsler    | String
createdDate | Created Date and time  | String
user | User's ID  | String
createdBy | Created by means if main user ID | String
eyeSides[{}] | Eye sides have file ID and details of halo test | String
firstReminderSend | This the the reminder for user to know 3 months completed for eye test | String
secondReminderSend | This the the reminder for user to know 3 months completed for eye test | String
thirdReminderSend | This the the reminder for user to know 3 months completed for eye test | String
fourthReminderSend | This the the reminder for user to know 3 months completed for eye test  | String

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>


## Download Patient PDF

```shell
 curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/appointment/getPdffile/5a37b5f6e4b00ad7ad9bf261"


```

> The above command returns this:

```json
It will download the PDF.

```


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/appointment/getPdffile/{AppointmentID}
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Appointment ID | Pass appointment ID in this api url | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
PDF |User will get the PDF | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Get Insurance details of patient

```shell
 curl -i -H "Content-Type: application/image" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516255575772:70c944473b1cedcb218c871ee7f7d175" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/user/getInsurenceCard/585a25f2e4b077dac66f2334"
```

> The above command returns this:

```json
[
  {
    "name": "J. F. Molloy and Associates Inc.",
    "files": [
      "1509948381910,https://s3.amazonaws.com/test-nakul/doctor/585a25f2e4b077dac66f2334/insurencecard/1509948381910/img_415072front.jpg",
      "1509948382040,https://s3.amazonaws.com/test-nakul/doctor/585a25f2e4b077dac66f2334/insurencecard/1509948382040/img_306406dback.jpg"
    ],
    "memberId": "ooopp",
    "payerId": "00143"
  }
]

```


### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/user/getInsurenceCard/{PatientID}
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{PatientID} | Pass patient ID in url for get the insurance details | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
name | Name of the insurance company detials | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

