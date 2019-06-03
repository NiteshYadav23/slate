

# Doctor Profile


## Get doctor info

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:niteshy2391@gmail.com:doctor:1443244746137:490c0398fcb578b08be9b7c065c9aad0" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/doctorinfo/55de9ff0e4b0c34612e032fc"
 
```
> The above command returns JSON structured like this:

```json
{
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
}
```

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/doctorinfo/{doctorInfoId}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
ID | Doctor's ID | Integer | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
200 Ok |It means successfully | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Update Doctor info

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/doctorinfo" -X POST -d '{"id":"5823018fe4b0242bf4219c2d","educationList" [{"id":"59e09cbce4b0a70b0de5b0c3","degree":"Bca","university":"un","yearOfPasssing":"88778"}],"hospitalAttachedWithList":[{"id":"59e09cbce4b0a70b0de5b0c4","name":"tt","city":"Pune","country":"India"}],"awardsReceivedList":[{"id":"59e09cbce4b0a70b0de5b0c5","name":"q","description":"Description","date":"11/11/1991"}],"specialities":[{"id":"55b78065e4b0b393bf91678f","name":"general physician","questionnaire":null,"report":null}],"licencedState":[{"id":"5665a2cb9a87399fa0b9ba33","state":"AL"},{"id":"5665a2cb9a87399fa0b9ba34","state":"AK"},{"id":"5665a2cb9a87399fa0b9ba35","state":"AZ"},{"id":"5665a2cb9a87399fa0b9ba37","state":"CA"},{"id":"5665a2cb9a87399fa0b9ba40","state":"IL"},{"id":"5665a2cb9a87399fa0b9ba41","state":"IN"},{"id":"5665a2cb9a87399fa0b9ba42","state":"IA"}],"registrationNumber":"22222","whyCoolDoctors":null,"bio":"","profession":"Optometrist","availabilityTimeZone":"Asia/Kolkata","npi":"0123456789778"}' 
```
> The above command returns JSON structured like this:

```json
{
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
}
```

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/doctorinfo
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
ID | Doctor's ID | Integer | Optional
educationList | List of Education | String | Optional
hospitalAttachedWithList | List of Hospitals | String | Optional
awardsReceivedList | List of Awards | String | Optional
specialities | Doctor specialities | String | Optional
licencedState | Licenced State | String | Optional
registrationNumber | Registration Number | Optional
whyCoolDoctors | Why you choosed cool | Optional
bio | desciption of bio | Optional
profession | profession | Optional
availabilityTimeZone | The time zone selected | Optional
npi |  | Optional


### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID | Doctor's ID | Integer | Optional
educationList | List of Education | String | Optional
hospitalAttachedWithList | List of Hospitals | String | Optional
awardsReceivedList | List of Awards | String | Optional
specialities | Doctor specialities | String | Optional
licencedState | Licenced State | String | Optional
registrationNumber | Registration Number | Optional
whyCoolDoctors | Why you choosed cool | Optional
bio | desciption of bio | Optional
profession | profession | Optional
availabilityTimeZone | The time zone selected | Optional
npi |  | Optional

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Get doctor Profile

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516208048648:27ecd079dffdd0f3d0535865008fba0f" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/user/profile"
```
> The above command returns JSON structured like this:

```json
{
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
}
```

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/user/profile
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
/DoctorOnDemand/api/doctor/user/profile | Get the all Doctor’s Profile | String | Required

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
Doctor Info :[{}] | Doctor info | String
Hospital Attached With List :[{}] | Hospital Attached with list | String
Awards Received List :[{}] | Awards received list | String
Specialities :[{}] | Specialities Details | String
Report:[{}] | Report | String
Role :[{}] | Role | String
Price:[{}] | Price info | String

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Update Doctor Profile

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nakulypatil@gmail.com:doctor:1440749653573:8dadcd8f0d86c3abf40b4f98ef8d5f69" "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/user/profile" -X PUT -d '{"id": "55a3b77ce4b003f998707a5c","email": "nakulypatil@gmail.com","pharmacyName": null,"pharmacyAddress": null,"aboutMe": {"id": "55a3b77ce4b003f998707a5a","firstName": "Nitesh","lastName": "yadav","birthDate": "1990-02-23 12:41 PM IST","address": "Pune","city": "Pune","country": "india","pincode": "411045","gender": "male","languagesSpeak": null,"additionalInfo": "Hi I plays cricket"},"contactInfo": {"id": "55a3b77ce4b003f998707a5b","email": "nakulypatil@gmail.com","phone": "3333333333"},"doctorInfo": {"registrationNumber": "44444444"},"role": {"id": "551ad2ffe4b0b59ff0cceccb","name": "doctor"},"timezone": {"id": "551ad2ffe4b0b59ff0cceccb","timezone": "Asia/Kolkata","displayName": null}}'

```
> The above command returns JSON structured like this:

```json
{
  "id": "55a3b77ce4b003f998707a5c",
  "email": "nakulypatil@gmail.com",
  "pharmacyName": null,
  "pharmacyAddress": null,
  "profileImageId": null,
  "profileImageName": null,
  "aboutMe": {
    "id": "55a3b77ce4b003f998707a5a",
    "firstName": "Nitesh",
    "lastName": "yadav",
    "birthDate": "1990-02-23 12:41 PM IST",
    "address": "Pune",
    "city": "Pune",
    "country": "india",
    "pincode": "411045",
    "gender": "male",
    "languagesSpeak": null,
    "additionalInfo": "Hi I plays cricket",
    "state": "NY"
  },
  "contactInfo": {
    "id": "55a3b77ce4b003f998707a5b",
    "email": "nakulypatil@gmail.com",
    "phone": "3333333333"
  },
  "patientInfo": null,
  "doctorInfo": {
    "id": "55c9ff64e4b0664156913e86",
    "educationList": [
      {
        "id": "55c9ff64e4b0664156913e81",
        "degree": "MD",
        "university": "Pune",
        "yearOfPasssing": "2014"
      }
    ],
    "hospitalAttachedWithList": [
      {
        "id": "55c9ff64e4b0664156913e82",
        "name": "Pune Sasun hospital",
        "city": "Pune",
        "country": "India"
      }
    ],
    "awardsReceivedList": [
      {
        "id": "55c9ff64e4b0664156913e83",
        "name": "Best Doctor",
        "description": "Eye Care",
        "date": "2015-07-02 12:41 PM IST"
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
        "id": "55c9ff64e4b0664156913e84",
        "state": "NY"
      },
      {
        "id": "55c9ff64e4b0664156913e85",
        "state": "CA"
      }
    ],
    "registrationNumber": "44444444"
  },
  "role": {
    "id": "551ad2ffe4b0b59ff0cceccb",
    "name": "doctor"
  },
  "timezone": null,
  "createdAt": "2015-07-13 01:05 PM UTC",
  "forgotPasswordToken": null,
  "familyMembers": null,
  "parentUser": null,
  "parentUserRelation": null,
  "password": null,
  "rating": null,
  "preferredPharmacies": null,
  "kandyUserName": "55a3b77ce4b003f998707a5c",
  "kandyUserPassword": "f7016bcd403f43",
  "kandyFullUserId": "55a3b77ce4b003f998707a5c@cmobrtctest.com",
  "oldPassword": null,
  "loginStatus": "Online",
  "stripeCustId": null,
  "invited": false,
  "validated": true,
  "activated": true,
  "managedUser": false
}
```

### HTTP Request

`PUT
http://localhost:8080/DoctorOnDemand/api/doctor/user/profile
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
ID | ID of update doctors profile | Integer | Required
Email | Doctors profile Email ID  | String | Required
Pharmacy Name | Pharmacy Name | String | Optional
Pharmacy Address | Pharmacy Address | String | Optional
 | **About Me** |  |
ID |ID of creator | Integer | Required
First Name | First Name | String | Required
Last Name | Last Name | String | Required
BirthDate | Date of Birth (MM/DD/YYYY) | String | Optional
Address | Doctor’s Address | String | Optional
City | City | String | Optional
Country | Country | String | Optional
Pincode | Pincode of Doctor's Area |Integer | Optional
Gender | Gender (M,F) | String | Required
Languages Speak | Languages | String | Optional
Additional Info | Additional Info | String | Optional
 | **Contact Info** |  |
ID | Contact ID | Integer | Required
Email | Contact Email ID  | String | Required
Phone | Contact Number | Integer | Optional
Role(ID,NAME) | Role (ID and Name) | String | Required
ContactInfo[{}] | ContactInfo Details | String | Optional
 | **Doctor Info** |  |
educationList | Doctor's Education details | String | Optional
hospitalAttachedWithList | List of Hospitals teid up with Doctors | String | Optional
awardsReceivedList | Awards Received by the Doctor | String | Optional
availabilityTimeZone | Time zone opted by Doctor | String | Optional
specialities[{}] | Specialities of Doctor | String | Optional
registrationNumber | Registration Number of Doctor| String | Optional
licencedState | Licensed State of Doctor | String | Required

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
Doctor Info :[{}] | Doctor info | String
Hospital Attached With List :[{}] | Hospital Attached with list | String
Awards Received List :[{}] | Awards received list | String
Specialities :[{}] | Specialities Details | String
Report:[{}] | Report | String
Role :[{}] | Role | String
Price:[{}] | Price info | String

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Add Doctor profile photo

```shell
curl -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516255939831:feb45f5ddb978fa7a171dea4310b9844" -H "Content-Type:multipart/form-data" "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/user/profileImageFromFile" -X POST -F file=@/Users/cupertino/Downloads/paulsupe232.png


```
> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/user/profileImageFromFile
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
file=@/FILE_PATH | Give the doctor's profile pic path | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
success |True & False | String

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>


## Get Doctor profile image

```shell
curl -i -H "Content-Type: application/image" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516255575772:70c944473b1cedcb218c871ee7f7d175" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/user/profileImageFromFile"

```
> The above command returns JSON structured like this:

```json
{
  "imagepath": "https://api.endpoint.eyecarelive/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsupe232.png"
}
```

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/user/profileImageFromFile
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Use URL for Get profile | This get API url will return the link for doctor’s photos | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
imagepath |This will return the image path URL | String

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>











