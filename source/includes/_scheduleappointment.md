

# Schedule Appointment

## Get-Date for Availability

Verify if the patient is an existing registered user and has credentials. 


```shell
curl -i -H "Content-Type:application/json" -H "x-auth-token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/getDates/v3" -X POST -d '{"timezone":"Asia/Kolkata"}'


```
> The above command returns JSON structured like this:

```json
[
  "2019-05-26",
  "2019-05-27",
  "2019-05-28",
  "2019-05-29",
  "2019-05-30",
  "2019-05-31",
  "2019-06-01",
  "2019-06-02",
  "2019-06-03",
  "2019-06-04",
  "2019-06-05",
  "2019-06-06",
  "2019-06-07",
  "2019-06-08"
]
```

### HTTP Request

`POST http://localhost:8080/DoctorOnDemand/api/patient/appointment/getDates/v3
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL  | Use this URL for API  | String | Required
timezone | Need to pass the timezone | String | Required

### Response

Parameter |  Description | Type 
--------- | ------------ | ---- 
Dates | This will returns all the dates for current and next week | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>


## Get Current week availability of Doctor


```shell
curl -i -H "Content-Type:application/json" -H "x-auth-token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/getAvailabilityOfCurrentWeek/56fb7614e4b0d3123cea4925" -X POST -d '{"timezone":"Asia/Kolkata"}'

```
> The above command returns JSON structured like this:

```json
[
  {
    "id": "5cf20ac8f893f42ebcd34a45",
    "startTime": "08",
    "sTime": "2019-06-01 02:00 PM IST",
    "eTime": "2019-06-01 08:40 AM UTC",
    "slotNumber": "0",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5cf20ac8f893f42ebcd34a46",
    "startTime": "08",
    "sTime": "2019-06-01 02:10 PM IST",
    "eTime": "2019-06-01 08:50 AM UTC",
    "slotNumber": "1",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5cf20ac8f893f42ebcd34a47",
    "startTime": "08",
    "sTime": "2019-06-01 02:20 PM IST",
    "eTime": "2019-06-01 09:00 AM UTC",
    "slotNumber": "2",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5cf20ac8f893f42ebcd34a48",
    "startTime": "09",
    "sTime": "2019-06-01 02:30 PM IST",
    "eTime": "2019-06-01 09:10 AM UTC",
    "slotNumber": "3",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5cf20ac8f893f42ebcd34a49",
    "startTime": "09",
    "sTime": "2019-06-01 02:40 PM IST",
    "eTime": "2019-06-01 09:20 AM UTC",
    "slotNumber": "4",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5cf20ac8f893f42ebcd34a4a",
    "startTime": "09",
    "sTime": "2019-06-01 02:50 PM IST",
    "eTime": "2019-06-01 09:30 AM UTC",
    "slotNumber": "5",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  }
]
```

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/getAvailabilityOfCurrentWeek/{DoctorID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL  | Use this URL for API  | String | Required
timezone | Need to pass the timezone | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID |Database Unique ID | String
startTime | Start time shows the slot   | String
sTime | This is the converted time as per doctors availability | String
eTime | This is the end time of the appointment. | String
slotNumber | This is slot number for internal backend use | String
patient | Deprecated | String
visitType | Deprecated | String
appointmentId | Deprecated | String
status | Enable and disable for backend use. | String
booked | This will indicate the slot already booked or available for the patient. | Boolean
Array:[{}] |  Same above array it will return for the same. | String

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>


## Get Next week availability of Doctor

```shell
curl -i -H "Content-Type:application/json" -H "x-auth-token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/getAvailabilityOfNextWeek/56fb7614e4b0d3123cea4925" -X POST -d '{"timezone":"Asia/Kolkata"}'

```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "5cf20afcf893f42ebcd34a87",
    "startTime": "10",
    "sTime": "2019-06-04 04:00 PM IST",
    "eTime": "2019-06-04 10:40 AM UTC",
    "slotNumber": "0",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5cf20afcf893f42ebcd34a88",
    "startTime": "10",
    "sTime": "2019-06-04 04:10 PM IST",
    "eTime": "2019-06-04 10:50 AM UTC",
    "slotNumber": "1",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5cf20afcf893f42ebcd34a89",
    "startTime": "10",
    "sTime": "2019-06-04 04:20 PM IST",
    "eTime": "2019-06-04 11:00 AM UTC",
    "slotNumber": "2",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5cf20afcf893f42ebcd34a8a",
    "startTime": "11",
    "sTime": "2019-06-04 04:30 PM IST",
    "eTime": "2019-06-04 11:10 AM UTC",
    "slotNumber": "3",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5cf20afcf893f42ebcd34a8b",
    "startTime": "11",
    "sTime": "2019-06-04 04:40 PM IST",
    "eTime": "2019-06-04 11:20 AM UTC",
    "slotNumber": "4",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5cf20afcf893f42ebcd34a8c",
    "startTime": "11",
    "sTime": "2019-06-04 04:50 PM IST",
    "eTime": "2019-06-04 11:30 AM UTC",
    "slotNumber": "5",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  }
]
```


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/getAvailabilityOfNextWeek/{DoctorID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL  | Use this URL for API  | String | Required
timezone | Need to pass the timezone | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID |Database Unique ID | String
startTime | Start time shows the slot   | String
sTime | This is the converted time as per doctors availability | String
eTime | This is the end time of the appointment. | String
slotNumber | This is slot number for internal backend use | String
patient | Deprecated | String
visitType | Deprecated | String
appointmentId | Deprecated | String
status | Enable and disable for backend use. | String
booked | This will indicate the slot already booked or available for the patient. | Boolean
Array:[{}] |  Same above array it will return for the same. | String

<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

