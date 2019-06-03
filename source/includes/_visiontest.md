

# Vision Test 

## Vision Test Scan QR Code 


```shell
 curl -k -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X POST "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/vision/validateQrCode/DOD1559552104201"
```
> The above command returns JSON structured like this:

```json
{
  "success": "5cf4d960f893f4029e17a2f1"
}

```

### HTTP Request

`POST http://localhost:8080//DoctorOnDemand/api/patient/vision/validateQrCode/{GET-ID-FromQR}/
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL | This based on URL  | String | Required

### Response

Parameter |  Description | Type 
--------- | ------------ | ---- 
success | This will return the unique ID | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>


## Use this to start the Vision Test


```shell
curl -k -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/vision/updateTestNew" -X POST -d '{"id":"5cf4d960f893f4029e17a2f1","distChecked": "1"}
```
> The above command returns JSON structured like this:

```json
{
  "id": "5cf4d960f893f4029e17a2f1",
  "otp": null,
  "patientId": "5ceed13cf893f45b5812b8e1",
  "leftOne": null,
  "leftTwo": null,
  "leftThree": null,
  "leftFour": null,
  "leftFive": null,
  "leftSix": null,
  "leftSeven": null,
  "leftEight": null,
  "leftNine": null,
  "rightOne": null,
  "rightTwo": null,
  "rightThree": null,
  "rightFour": null,
  "rightFive": null,
  "rightSix": null,
  "rightSeven": null,
  "rightEight": null,
  "rightNine": null,
  "qrCode": "DOD1559552104201",
  "qrImage": "iVBORw0KGgoAAAANSUhEUgAAAMgAAADIAQAAAACFI5MzAAAA1klEQVR42u2XQQ7DIAwEzYln8NMWfsozOGVrG4jUNjmzkbCiCDI5IC+7JIK7kk022eQZpIlWaPJuKdswMREbFlQlZU55SJZUWr90+YzkiGAlEsBIXG2MOxfpLrGmXvtnIRlVw13uLCS6atuDyU38rfZ6klzhquH3ilXfYiKudreI5x8R8dmhG9Bbm4WJ9DwGsj7+7fVq0mukcvr3z0pyqg1b8hGpyEzlbmVwETvNUNW+AZTEA0aPixw5iTU1gIvAY8+lrmRkfgWY4Bf+WUn2/9wmmzyUfAAOicWwjrNOsgAAAABJRU5ErkJggg==",
  "codeScanned": "1",
  "distChecked": "1",
  "reset": null,
  "cancel": null,
  "end": null,
  "fieldParam": null,
  "alexa": false,
  "resultRightEye": null,
  "resultLeftEye": null,
  "attemptLeftOne": null,
  "attemptLeftTwo": null,
  "attemptLeftThree": null,
  "attemptLeftFour": null,
  "attemptLeftFive": null,
  "attemptLeftSix": null,
  "attemptLeftSeven": null,
  "attemptLeftEight": null,
  "attemptLeftNine": null,
  "attemptRightOne": [
    {
      "id": "5cf4e916f893f4029e17a6f6",
      "count": "1",
      "position": "RIGHT",
      "answer": null,
      "result": null
    }
  ],
  "attemptRightTwo": null,
  "attemptRightThree": null,
  "attemptRightFour": null,
  "attemptRightFive": null,
  "attemptRightSix": null,
  "attemptRightSeven": null,
  "attemptRightEight": null,
  "attemptRightNine": null
}
```

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/vision/updateTestNew/
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
ID  | This ID is unique | Integer | Required
distChecked | That should be number | String | Required


### Response

Parameter | Description | Type 
--------- | ----------- | ----
id | This will return Unique ID | String
otp | Deprecated | String 
patientId | Patient Unique ID | String
leftOne | This will return the dynamic c position | String
leftTwo | This will return the dynamic c position | String
leftThree | This will return the dynamic c position | String
leftFour | This will return the dynamic c position | String
leftFive | This will return the dynamic c position | String
leftSix | This will return the dynamic c position | String
leftSeven | This will return the dynamic c position | String
leftEight | This will return the dynamic c position | String
leftNine | This will return the dynamic c position | String
rightOne | This will return the dynamic c position | String
rightTwo | This will return the dynamic c position | String
rightThree | This will return the dynamic c position | String
rightFour | This will return the dynamic c position | String
rightFive | This will return the dynamic c position | String
rightSix| This will return the dynamic c position | String
rightSeven | This will return the dynamic c position | String
rightEight | This will return the dynamic c position | String
rightNine | This will return the dynamic c position | String
qrCode | QR scan for the Code | String
qrImage | QR Image generate | .jpg,etc
codeScanned | Code scanned or not | String
distChecked | Scan and test start or not | String 
reset | Reset test or not | String
cancel | Deprecated | String 
end | Deprecated | String
fieldParam | Deprecated | String
alexa | Alexa true or false | Boolean
resultRightEye | This will be result to compare the answer | String
resultLeftEye | This will be result to compare the answer | String
attemptLeftOne | This will be result to compare the answer | String
attemptLeftTwo | This will be result to compare the answer | String
attemptLeftThree | This will be result to compare the answer | String
attemptLeftFour | This will be result to compare the answer | String
attemptLeftFive | This will be result to compare the answer | String
attemptLeftSix | This will be result to compare the answer | String
attemptLeftSeven | This will be result to compare the answer | String
attemptLeftEight | This will be result to compare the answer | String
attemptLeftNine:[{}] | This will be result to compare the answer | String
attemptRightOne:[{}] | This will be result to compare the answer | String
id | ID as per the unique created dynamically | String
count | Count for test | String
position | Position of the eye test |  String
answer | Will return as answer | String
result |  | String
attemptRightTwo | Attempt of user for the result. | String
attemptRightThree | Attempt of user for the result. | String
attemptRightFour | Attempt of user for the result. | String
attemptRightFive | Attempt of user for the result. | String
attemptRightSix | Attempt of user for the result. | String
attemptRightSeven | Attempt of user for the result. | String
attemptRightEight | Attempt of user for the result. | String
attemptRightNine | Attempt of user for the result. | String

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>



