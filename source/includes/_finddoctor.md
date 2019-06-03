

# Find Doctor/Clinic

## Find Doctor/Clinic by state, by location & All.

Verify if the patient is an existing registered user and has credentials. 


```shell
 curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/eclClinic/getAllDoctorsAndEclClinics/v3"
```
> The above command returns JSON structured like this:

```json
{
  "doctors": [
    {
      "id": "56fb7614e4b0d3123cea4925",
      "email": "nitesh.yadav@cupertinosoft.com",
      "firstName": "Dr. John",
      "lastName": "Gelles",
      "profession": "Ophthalmologist",
      "profileImagePath": "https://s3.amazonaws.com/deveclprofimg/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/imgDefault.png",
      "city": "8L10iLEjsRBVkFaI1gu4bw==",
      "state": "tdK26+Dp5ks9TH9wFlmgDA==",
      "preffered": true
    },
    {
      "id": "56fbd63de4b0777c5a04f540",
      "email": "nitesh.yadav@cooldoctors.io",
      "firstName": "Dr. Moshe",
      "lastName": "Mendelson",
      "profession": "Ophthalmologist",
      "profileImagePath": null,
      "city": "RJwLsmnPATnBjHJjPehhYA==",
      "state": "7RsRnv7ZO9LVoxfOUEx9UlvX6tam9de+xDWdwh5k/Z8=",
      "preffered": true
    },
    {
      "id": "",
      "email": "lindsaydurtschi@gmail.com",
      "firstName": "Lindsay",
      "lastName": "Durtschi",
      "profession": null,
      "profileImagePath": null,
      "city": "hBJrCsmIi0nalDhxWS+2Ug==",
      "state": "0eqLltqu1Q+JKDnw55Iylg==",
      "preffered": false
    },
    {
      "id": "58e2268be4b0b3b8e551c825",
      "email": "doctor@cooldoctors.io",
      "firstName": "Raj",
      "lastName": "R",
      "profession": "Optometrist",
      "profileImagePath": null,
      "city": "sFWmH4McpWLm+NqMragYQg==",
      "state": "KQJdYdlXExqOB/F8AA5D4g==",
      "preffered": false
    }
  ],
  "eclClinics": [
    {
      "id": "5c2c9110f893f4108a3df9d6",
      "name": "Nitesh Hights",
      "description": "This dream",
      "logo": " ",
      "clinicLogo": " ",
      "city": "Pune",
      "state": "MH",
      "preffered": false
    },
    {
      "id": "5c3452c5f893f4108aa24407",
      "name": "Cupertino Clinic",
      "description": "This dream",
      "logo": " ",
      "clinicLogo": " ",
      "city": "Pune",
      "state": "MH",
      "preffered": false
    },
    {
      "id": "5c3452eff893f4108aa2441e",
      "name": "Eyecare Clinic",
      "description": "This dream",
      "logo": " ",
      "clinicLogo": " ",
      "city": "Pune",
      "state": "MH",
      "preffered": false
    }
  ]
}
```

### HTTP Request

`GET http://localhost:8080/DoctorOnDemand/api/patient/eclClinic/getAllDoctorsAndEclClinics/v3
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL for | This is for getting all the doctors and clinic  | String | Required

### Response

Parameter |  Description | Type 
--------- | ------------ | ---- 
doctors:[{}] | This will be an array of all the doctor list. | String
id | Unique ID of the database | String
email | The email address of the doctor | String
firstName | Doctor First Name | String
lastName | Doctor Last Name | String
profession | This will return the profession of doctor | String
profileImagePath | This will have the profile link | String
city | City name of the doctor | String
state | State name of doctor | String
preferred | A preferred doctor or not | boolean
eclClinics:[{}] | This will be an array of all the clinic list. | String
id | Unique ID of the database | String
name | Name of the clinic | String'
description | Description of the Clinic | String
logo | | .jpg, etc
clinicLogo | Clinic Logo | .jpg,etc
city | City of the Clinic | String
state | State of the clinic | String
preferred | A preferred clinic or not | boolean


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>


## Find a Doctor/Clinic by Zip code.


```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/eclClinic/searchDoctorAndEclClinicByZip/v3/411045"


```
> The above command returns JSON structured like this:

```json
{
  "doctors": [
    {
      "id": "56fb7614e4b0d3123cea4925",
      "email": "nitesh.yadav@cupertinosoft.com",
      "firstName": "Dr. John",
      "lastName": "Gelles",
      "profession": "Ophthalmologist",
      "profileImagePath": "https://s3.amazonaws.com/deveclprofimg/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/imgDefault.png",
      "city": "8L10iLEjsRBVkFaI1gu4bw==",
      "state": "tdK26+Dp5ks9TH9wFlmgDA==",
      "preffered": true
    },
    {
      "id": "56fbd63de4b0777c5a04f540",
      "email": "nitesh.yadav@cooldoctors.io",
      "firstName": "Dr. Moshe",
      "lastName": "Mendelson",
      "profession": "Ophthalmologist",
      "profileImagePath": null,
      "city": "RJwLsmnPATnBjHJjPehhYA==",
      "state": "7RsRnv7ZO9LVoxfOUEx9UlvX6tam9de+xDWdwh5k/Z8=",
      "preffered": true
    },
    {
      "id": "",
      "email": "lindsaydurtschi@gmail.com",
      "firstName": "Lindsay",
      "lastName": "Durtschi",
      "profession": null,
      "profileImagePath": null,
      "city": "hBJrCsmIi0nalDhxWS+2Ug==",
      "state": "0eqLltqu1Q+JKDnw55Iylg==",
      "preffered": false
    },
    {
      "id": "58e2268be4b0b3b8e551c825",
      "email": "doctor@cooldoctors.io",
      "firstName": "Raj",
      "lastName": "R",
      "profession": "Optometrist",
      "profileImagePath": null,
      "city": "sFWmH4McpWLm+NqMragYQg==",
      "state": "KQJdYdlXExqOB/F8AA5D4g==",
      "preffered": false
    }
  ],
  "eclClinics": [
    {
      "id": "5c2c9110f893f4108a3df9d6",
      "name": "Nitesh Hights",
      "description": "This dream",
      "logo": " ",
      "clinicLogo": " ",
      "city": "Pune",
      "state": "MH",
      "preffered": false
    },
    {
      "id": "5c3452c5f893f4108aa24407",
      "name": "Cupertino Clinic",
      "description": "This dream",
      "logo": " ",
      "clinicLogo": " ",
      "city": "Pune",
      "state": "MH",
      "preffered": false
    },
    {
      "id": "5c3452eff893f4108aa2441e",
      "name": "Eyecare Clinic",
      "description": "This dream",
      "logo": " ",
      "clinicLogo": " ",
      "city": "Pune",
      "state": "MH",
      "preffered": false
    }
  ]
}
```

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/eclClinic/searchDoctorAndEclClinicByZip/v3/{Zipcode}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL for  | This is for getting all the doctors and clinic  | String | Required


### Response

Parameter | Description | Type 
--------- | ----------- | ----
doctors:[{}] | This will be an array of all the doctor list. | String
id | Unique ID of the database | String
email | The email address of the doctor | String
firstName | Doctor First Name | String
lastName | Doctor Last Name | String
profession | This will return the profession of doctor | String
profileImagePath | This will have the profile link | String
city | City name of the doctor | String
state | State name of doctor | String
preferred | A preferred doctor or not | boolean
eclClinics:[{}] | This will be an array of all the clinic list. | String
id | Unique ID of the database | String
name | Name of the clinic | String'
description | Description of the Clinic | String
logo | | .jpg, etc
clinicLogo | Clinic Logo | .jpg,etc
city | City of the Clinic | String
state | State of the clinic | String
preferred | A preferred clinic or not | boolean


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>


## Find a Doctor/Clinic by name.

```shell
curl -i -H "Content-Type:application/json" -H "x-auth-token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/eclClinic/searchDoctorAndEclClinicByName/v3" -X POST -d '{"name": "Nitesh"}'

```

> The above command returns JSON structured like this:

```json
{
  "doctors": [
    {
      "id": "5b167f9fe4b092d44572680c",
      "email": "mit@cupertinosoft.com",
      "firstName": "Nitesh",
      "lastName": "Yadav",
      "profession": "Optometrist",
      "profileImagePath": null,
      "city": "nA/XB0rC8UvKhkMzMDAtmg==",
      "state": "",
      "preffered": false
    },
    {
      "id": "5b1687b0e4b092d445726936",
      "email": "mit23@cupertinosoft.com",
      "firstName": "Nitesh",
      "lastName": "Yadav",
      "profession": null,
      "profileImagePath": null,
      "city": "PUl6wQwczVk+SuNM98o/Og==",
      "state": "",
      "preffered": false
    }
  ],
  "eclClinics": [
    {
      "id": "5c2c9110f893f4108a3df9d6",
      "name": "Nitesh Hights",
      "description": "This dream",
      "logo": " ",
      "clinicLogo": " ",
      "city": "Pune",
      "state": "MH",
      "preffered": false
    }
  ]
}
```

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/eclClinic/searchDoctorAndEclClinicByName/v3/

`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL for  | This is for getting all the doctors and clinic   | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
doctors:[{}] | This will be an array of all the doctor list. | String
id | Unique ID of the database | String
email | The email address of the doctor | String
firstName | Doctor First Name | String
lastName | Doctor Last Name | String
profession | This will return the profession of doctor | String
profileImagePath | This will have the profile link | String
city | City name of the doctor | String
state | State name of doctor | String
preferred | A preferred doctor or not | boolean
eclClinics:[{}] | This will be an array of all the clinic list. | String
id | Unique ID of the database | String
name | Name of the clinic | String'
description | Description of the Clinic | String
logo | | .jpg, etc
clinicLogo | Clinic Logo | .jpg,etc
city | City of the Clinic | String
state | State of the clinic | String
preferred | A preferred clinic or not | boolean

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

