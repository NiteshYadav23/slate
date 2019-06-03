
# Treatment Plan
## Get Treatment Plan for a given user or patient

```shell

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/getPatientHistory/5a2c0a69e4b0e4fa266e0180"

```
> The above command returns JSON structured like this:

```json
[{
	"symtons": "Dry Eye",
	"status": "pending",
	"createdAt": "2017-12-10 07:13 AM PST",
	"questionaire": {
		"id": "5a2d4f01e4b0e4fa266e05ec",
		"questions": [{
			"id": "5a2d4f01e4b0e4fa266e05d1",
			"question": "Snellen chart Right Eye vision test",
			"answerType": "String",
			"answer": "20/30",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05d2",
			"question": "Snellen chart Left Eye vision test",
			"answerType": "String",
			"answer": "20/25",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05d3",
			"question": "Speed Test Score",
			"answerType": "String",
			"answer": "0",
			"param1": null,
			"param2": null,
			"param3": null
		}],
		"symptoms": [{
			"id": "5a2d4f01e4b0e4fa266e05d4",
			"question": "Dryness, Grittiness or Scratchiness: At this Visit",
			"answerType": "String",
			"answer": "Yes",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05d5",
			"question": "Dryness, Grittiness or Scratchiness: Within past 72 hours",
			"answerType": "String",
			"answer": "Yes",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05d6",
			"question": "Dryness, Grittiness or Scratchiness: Within past 3 mos",
			"answerType": "String",
			"answer": "Yes",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05d7",
			"question": "Soreness or Irritation: At this Visit",
			"answerType": "String",
			"answer": "Yes",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05d8",
			"question": "Soreness or Irritation: Within past 72 hours",
			"answerType": "String",
			"answer": "Yes",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05d9",
			"question": "Soreness or Irritation: Within past 3 months",
			"answerType": "String",
			"answer": "Yes",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05da",
			"question": "Burning or Watering: At this Visit",
			"answerType": "String",
			"answer": "Yes",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05db",
			"question": "Burning or Watering: Within past 72 hours",
			"answerType": "String",
			"answer": "Yes",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05dc",
			"question": "Burning or Watering: Within past 3 mos months",
			"answerType": "String",
			"answer": "Yes",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05dd",
			"question": "Eye Fatigue: At The Visit",
			"answerType": "String",
			"answer": "Yes",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05de",
			"question": "Eye Fatigue: Within past 72 hours",
			"answerType": "String",
			"answer": "Yes",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05df",
			"question": "Eye Fatigue: Within past 3 months",
			"answerType": "String",
			"answer": "Yes",
			"param1": null,
			"param2": null,
			"param3": null
		}],
		"frequency": [{
			"id": "5a2d4f01e4b0e4fa266e05e0",
			"question": "Dryness, Grittiness or Scratchiness",
			"answerType": "String",
			"answer": "0",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05e1",
			"question": "Soreness or Irritation",
			"answerType": "String",
			"answer": "0",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05e2",
			"question": "Burning or Watering",
			"answerType": "String",
			"answer": "0",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05e3",
			"question": "Eye Fatigue",
			"answerType": "String",
			"answer": "0",
			"param1": null,
			"param2": null,
			"param3": null
		}],
		"severity": [{
			"id": "5a2d4f01e4b0e4fa266e05e4",
			"question": "Dryness, Grittiness or Scratchiness",
			"answerType": "String",
			"answer": "0",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05e5",
			"question": "Soreness or Irritation",
			"answerType": "String",
			"answer": "0",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05e6",
			"question": "Burning or Watering",
			"answerType": "String",
			"answer": "0",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05e7",
			"question": "Eye Fatigue",
			"answerType": "String",
			"answer": "0",
			"param1": null,
			"param2": null,
			"param3": null
		}],
		"treatment": [{
			"id": "5a2d4f01e4b0e4fa266e05e8",
			"question": "Are you taking medications?",
			"answerType": "String",
			"answer": "",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05e9",
			"question": "Are you taking Omega 3 supplements?",
			"answerType": "String",
			"answer": "",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05ea",
			"question": "Are you doing warm compresses?",
			"answerType": "String",
			"answer": "",
			"param1": null,
			"param2": null,
			"param3": null
		}, {
			"id": "5a2d4f01e4b0e4fa266e05eb",
			"question": "Are you using eye drops?",
			"answerType": "String",
			"answer": "",
			"param1": null,
			"param2": null,
			"param3": null
		}],
		"appointment": null,
		"lasikQuestionnaire": null,
		"contactLenseQuestions": null
	},
	####"todos": [{
		"id": "5a2e761de4b0e4fa266e1fce",
		"patient": "5a2c0a69e4b0e4fa266e0180",
		"status": 0,
		"appointment": "5a2d4f01e4b0e4fa266e05ed",
		"assessment": "sdfsfsfs",
		"diagnosis": "sfs",
		"treatmentPlan": "sdfsfs",
		"updatedAt": "2017-12-11 04:12 AM PST"
	}],
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
		"languagesSpeak": ["English", "", ""],
		"additionalInfo": null,
		"state": "ca"
	},
	"diseaseImageFilePath": null,
	"contactlenseImageFilePath": null,
	"solutionBottleImage": null,
	"remark": null,
	"doctorInfo": {
		"id": "5823018fe4b0242bf4219c2d",
		"educationList": [{
			"id": "59e09cbce4b0a70b0de5b0c3",
			"degree": "    Bca",
			"university": "   un",
			"yearOfPasssing": "   88778"
		}],
		"hospitalAttachedWithList": [{
			"id": "59e09cbce4b0a70b0de5b0c4",
			"name": "   ng tt",
			"city": "    Pune",
			"country": "   India"
		}],
		"awardsReceivedList": [{
			"id": "59e09cbce4b0a70b0de5b0c5",
			"name": "q",
			"description": "   Description",
			"date": "11/11/1991"
		}],
		"specialities": [{
			"id": "55b78065e4b0b393bf91678f",
			"name": "general physician",
			"questionnaire": null,
			"report": null
		}],
		"licencedState": [{
			"id": "5665a2cb9a87399fa0b9ba33",
			"state": "AL"
		}, {
			"id": "5665a2cb9a87399fa0b9ba34",
			"state": "AK"
		}, {
			"id": "5665a2cb9a87399fa0b9ba35",
			"state": "AZ"
		}, {
			"id": "5665a2cb9a87399fa0b9ba40",
			"state": "IL"
		}, {
			"id": "5665a2cb9a87399fa0b9ba41",
			"state": "IN"
		}, {
			"id": "5665a2cb9a87399fa0b9ba42",
			"state": "IA"
		}],
		"registrationNumber": "22222",
		"whyCoolDoctors": null,
		"profession": "Optometrist",
		"availabilityTimeZone": "America/Los_Angeles",
		"npi": "0123456789778"
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
			"diseaseRelation": [{
				"conditions": "Cataract",
				"relationship": "Aunt"
			}]
		}
	},
	"patientAboutMe": {
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
	"doctorProfileImage": "https://dev.api.cooldoctors.io:8443/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsuper.png",
	"appointmentId": "5a2d4f01e4b0e4fa266e05ed",
	"needFollowUp": false,
	"doctorId": "56fb7614e4b0d3123cea4925",
	"files": null,
	####"medicinePrescriptions": [{
		"id": "5a2e78cee4b0e4fa266e2002",
		"patientId": null,
		"appointmentId": "5a2d4f01e4b0e4fa266e05ed",
		"medicineName": "Eye Drop",
		"dosage": "2",
		"frequencyHourPerDay": "4",
		"totalDays": "6",
		"createdAt": "2017-12-11 04:23 AM PST",
		"calculatedNoToSend": "6",
		"sendCount": null,
		"status": "enable",
		"type": "Drops",
		"firstReminderSend": false
	}]
}]

```

> Make sure to replace `X-Auth-Token` with your API key.

Get Treatment Plan for a given user or patient
Get list of treatment plans for a patient
Get a list of all prescriptions written by the doctor
In this API for all appointments list, Will return the patient appointment data with Treatment plan, Medical Prescriptions etc. 

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/appointment/getPatientHistory/{PatientID}"
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
getPreferredDoctor | URL will give all doctors| String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | ID of created by database | String 
Start date | Start date of created | String 
End Date | End date of created | String 
Doctor | doctor name info | String 
 Patient| Patient name Info | String 
ID| user id# | String 
Email | User’s Email Address| String 
profile Image Id| Profile photo ID . Deprecated  | String 
profile Image Name| Profile photo Name Depreciated | String 
About Me :[{}]| about me for User’s details  | String 
Contact Info:[{}] | Contact person Info| String 
Patient Info :[{}] | Patient info  | String 
Doctor Info :[{}]| Doctor info  | String 
Hospital Attached With List :[{}]| Hospital Attached with list  | String 
Family History:[{}]| Array of the family history | String 
Awards Received List | Awards received list| String 
medicinePrescriptions[{}] | It will give the prescriptions details by appointment | String 
Questionnaire[{}] | Questionnaire details  | String 
TODO[{}]| Treatment plan details by appointments | String 
Specialities| Specialities Details| String 
Appointment| Appointment details| String 
Report | Report| String 
Created At :[{}]| Array of the created at  | String 



`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>



