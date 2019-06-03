

# Calling Notification 


## Add Device Token

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X POST "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/auth/addDeviceToken" -d '{"deviceToken":"88771f3bc9d31b4711f3a4859e76d60aecd44d1b28b0e56dc6387854036f8bf2","platform":"VOIP"}'

 
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
      "addedByCpm": false,
      "activated": true,
      "invited": false,
      "validated": true,
      "pilotDoc": false,
      "managedUser": true
    }
  ],
  "parentUser": null,
  "parentUserRelation": null,
  "password": null,
  "rating": null,
  "preferredPharmacies": null,
  "oldPassword": null,
  "loginStatus": "Online",
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
    "sendReminderForMedicine": true,
    "sentMessage": true,
    "addTreatmentPlan": true,
    "sendReminderForEyeTest": true,
    "addTestreport": true,
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
}```

Add Device token for patient to receive a call.


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/auth/addDeviceToken/
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
deviceToken | Device ID | String | Required
platform | Notification Platform | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID |ID of User | Integer
Email ID | User's Email ID | String
Pharmacy Name | Pharmacy name | String
pharmacy Address | pharmacy Address | String
profile Image Id | Profile image ID | Integer
profile Image Name | Profile image Name | .jpg,etc
About Me :[{}] | About me for User detail | String
Contact Info:[{}] | Contact person Info | String
Patient Info :[{}] | Patient info | String
Doctor Info :[{}] | Doctor info | String
Hospital Attached With List :[{}] | Hospital Attached with List Details | String
Awards Received List :[{}] | Awards received list | String
Specialties:[{}] | Specialiities Detail deprecated | String
Report:[{}] | Report deprecated |  String
Role :[{}] | "role":{"id":"551ad2ffe4b0b59ff0cceccb","name":"doctor"} | String
Price:[{}] | Price info | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Activate Doctor

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patilnak88@gmail.com:admin:1515516167302:73eee16ab9e185d0fbfb21f0fba9ad25" -X POST "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/admin/user/activate/5a2d64f4e4b02c0a7433f43f"

 
```
> The above command returns JSON structured like this:

```json
{
  "success": true
}
```
> Make sure to replace `X-Auth-Token` with your API key.

When patient logged In or Signed Up then it should add the device token to get a notification for messages and calls.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/pharmacy/api/admin/user/activate/user'sID
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
/DoctorOnDemand/api/admin/user/activate/ID | Valid ID for Activate Doctor | Integer | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
{“success”:”True”} | {“success”:”True”} it Means successful Response | String


<aside class="info">
Remember - The Doctor account is created only when Admin activates Doctor !!
</aside>



