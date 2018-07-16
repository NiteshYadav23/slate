

# Availability


## Create availability

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cooldoctors.io:doctor:1515823387217:5beaa02207a3e861e35283011b0dc12a" "http://api.endpoint.eyecarelive/DoctorOnDemand/api/doctor/availability" -X POST -d '{"startDate":"2015-06-15 09:44 PM IDT","endDate":"2015-10-15 09:44 PM IDT"}'
 
```
> The above command returns JSON structured like this:

```json
{
  "id": "55dea28ae4b0c34612e032fd",
  "startDate": "2015-06-15 09:44 PM IDT",
  "endDate": "2015-10-15 09:44 PM IDT",
  "doctor": {
    "id": "55de9c50e4b0c34612e032ee",
    "email": "niteshy2391@gmail.com",
    "pharmacyName": null,
    "pharmacyAddress": null,
    "profileImageId": null,
    "profileImageName": null,
    "aboutMe": {
      "id": "55de9c50e4b0c34612e032ec",
      "firstName": "Nitesh",
      "lastName": "Yadav",
      "birthDate": null,
      "address": "Pune",
      "city": "Pune",
      "country": "india",
      "pincode": "411045",
      "gender": "female",
      "languagesSpeak": null,
      "additionalInfo": null,
      "state": "Maharashtra"
    },
    "contactInfo": {
      "id": "55de9c50e4b0c34612e032ed",
      "email": "niteshy2391@gmail.com",
      "phone": "1111111111"
    },
    "patientInfo": null,
    "doctorInfo": {
      "id": "55de9ff0e4b0c34612e032fc",
      "educationList": [
        {
          "id": "55de9ff0e4b0c34612e032f7",
          "degree": "BDS",
          "university": "Pune",
          "yearOfPasssing": "2013"
        }
      ],
      "hospitalAttachedWithList": [
        {
          "id": "55de9ff0e4b0c34612e032f8",
          "name": "Pune Sasun hospital",
          "city": "Pune",
          "country": "India"
        }
      ],
      "awardsReceivedList": [
        {
          "id": "55de9ff0e4b0c34612e032f9",
          "name": "Best Doctor",
          "description": "Eye Care",
          "date": "2015-08-27 08:19 AM IDT"
        }
      ],
      "specialities": [
        {
          "id": "55b7802be4b0b393bf91678e",
          "name": "eye care",
          "questionnaire": null,
          "report": null
        }
      ],
      "licencedState": [
        {
          "id": "55de9ff0e4b0c34612e032fa",
          "state": "NY"
        },
        {
          "id": "55de9ff0e4b0c34612e032fb",
          "state": "CA"
        }
      ],
      "registrationNumber": "22222"
    },
    "role": {
      "id": "551ad2ffe4b0b59ff0cceccb",
      "name": "doctor"
    },
    "timezone": null,
    "createdAt": "2015-08-27 08:12 AM IDT",
    "forgotPasswordToken": null,
    "familyMembers": null,
    "parentUser": null,
    "parentUserRelation": null,
    "password": "neethip666",
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
    "randomtoken": "ZnwMJq",
    "isEmailVerified": false,
    "invited": false,
    "validated": true,
    "activated": true,
    "managedUser": false
  }
}
```

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/availability
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
StartDate | Start date for create availability | String | Required
EndDate | End date for Availability | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID |ID of Doctor | Integer
Email ID | Doctor's Email ID | String
Pharmacy Name | Pharmacy name | String
pharmacy Address | pharmacy Address | String
profile Image Id | Profile image ID | Integer
profile Image Name | Profile image Name | .jpg,etc
About Me :[{}] | About me info for the Doctor | String
Contact Info:[{}] | Contact person Info | String
Patient Info :[{}] | Patient info | String
Hospital Attached With List :[{}] | Hospital Attached with list | String
Awards Received List | Awards Received List | String
Specialities | Specialities Details | String
Report | Report | String
Role | Role | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>
