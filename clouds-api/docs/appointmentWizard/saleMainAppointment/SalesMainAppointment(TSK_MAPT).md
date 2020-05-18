# ** Sales Main Appointment (TSK_MAPT) **

## ** Introduction **

Appointment wizard is used for booking appointment for services from service provider organization or
distributor organization and this section contain all the API and Document detail for installer side (service provider ).

List of Api used for this subKeyType (** TSK_MAPT ** ).

- Assign Appointment Api
- Reject Appointment Api
- Complete Appointment Api

---

## ** Assign Appointment Request on APT_CLZ_COM **

This API used when user assign a appointment to user who has right to handle
appointment request at services provider org.

* `BeanId`       - UPDATE#SRV#TSK#TSK_MAPT#ASSIGN_APPOINTMENT
* `Service Name` - APT_CLZ_COM
* `actionArray`  - ** ASSIGN_APPOINTMENT **
* `Flow Diagram` - [link](https://app.diagrams.net/#G10zTC0x5hrtfKyqs-Tgi6dUSEb6_FJ_w0)

### ** Parameters **

Parameter name                | Data Type       | Description
------------                  | -------------   |---------------------
CML_ACCEPTED                  | Integer         | active status of appointment(1 means appointment has bean accepted)
SRV_DETAILS                   | JsonArray       | contain details of services like its CML_SERIAL_ID , slot details , services name
CML_ASSIGNED_TO               | String          | assign userId

### ** Assign Appointment Request on APT_CLZ_COM ** :-

```yaml
{
  "userId": "a.srv@ssserviceprovider.clouzer.com",
  "action": "UPDATE",
  "dataArray": [
    {
      "actionArray": [
        "ASSIGN_APPOINTMENT"
      ],
      "calmailUpdate": {
        "LAST_MODIFIED_BY": "a.srv@ssserviceprovider.clouzer.com",
        "LAST_MODIFIED_ON": "2020-03-26T11:47:10.978Z",
        "CML_ACCEPTED": 1,
        "CML_ASSIGNED_TO": "ASSIGNED",
        "SRV_DETAILS": [
         {
          "CML_TITLE": "automation",
          "CML_SERIAL_ID": "SS -SRV-157320214349699",
          "FROM_TO_TIME": [
            {
              "CML_FROM_DATETIME": "2020-03-26T08:00:00.757Z",
              "CML_TO_DATETIME": "2020-03-26T09:00:00.757Z",
              "CML_ASSIGNED_TO": "a.srv@ssserviceprovider.clouzer.com"
            },
            {
              "CML_FROM_DATETIME": "2020-03-26T09:00:00.757Z",
              "CML_TO_DATETIME": "2020-03-26T10:00:00.757Z",
              "CML_ASSIGNED_TO": "a.srv@ssserviceprovider.clouzer.com"
            }
          ],
          "CML_COST": 1234,
          "KEY_VAL": "ssserviceprovider.clouzer.com#PRJ_ORG_WKS_1573201799432_4255#SEC_WIZ_SRV_0015#TSK_SRV_LST_1573202143566_8156",
          "CML_DISCOUNT": 2,
          "CML_DISCOUNT_TYPE": "%",
          "CML_ESTIMATED_TIME": 0.25,
          "CML_SERVICE_PROVIDERS": [
            "ssserviceprovider.clouzer.com#PRJ_DEPT_ORG_1231231231231_1234#SEC_WIZ_ROLE_0001#TSK_ROL_LST_0002"
          ],
          "CML_COUNT": 2,
          "SUB_KEY_TYPE": "TSK_PSRV",
          "CML_CURRENCY_TYPE": "$"
        }],
        "SYNC_PENDING_STATUS": 0
      },
      "essentialList": [
        {
          "a.srv@ssserviceprovider.clouzer.com": "a.srv@ssserviceprovider.clouzer.com#PRJ_URM_0002"
        }
      ],
      "keyType": "TSK",
      "keyVal": "ssserviceprovider.clouzer.com#PRJ_AGN_123456_5#SEC_AGN_123456_5#TSK_MAPT_1585221051879_1071",
      "subKeyType": "TSK_MAPT"
    }
  ],
  "moduleName": "SRV",
  "requestId": "/sync#/sync#wLQYciVfuC0HscNkAAAAa.srv@ssserviceprovider.clouzer.com#1585223230978r194r29",
  "socketId": "/sync#wLQYciVfuC0HscNkAAAA",
  "topic": "CCR_CLZ_COM"
}

```

### ** Assign Appointment Action Impact **

!!! note
    1)Same services man Can be assign to different slot.

    2) After assigning appointment to service man , appointment get replicated to assign user urm.

    3) Property Replicated at installer side

    4) Appointment get updated in installer and builder org also.


### ** Assign Appointment Response on BROADCAST ** :

```yaml

{
  "userId": "kara.james@faservices.clouzer.com",
  "extraParam": {
    "moduleName": "SRV",
    "hitServerFlag": "1"
  },
  "action": "UPDATE",
  "moduleName": "SRV",
  "requestId": "/sync#/sync#WP3Pp2pWu2oXQwOeAAUgkara.james@faservices.clouzer.com#1587709472500r11r226",
  "FROM": "senddatatoserver",
  "socketId": "/sync#WP3Pp2pWu2oXQwOeAAUg",
  "dataArray": [
    {
      "ACTIVE_STATUS": 1,
      "CML_ACCEPTED": 1,
      "CML_CITY": "San Francisco County",
      "CML_COMPLETION_PERCENTAGE": 0,
      "CML_CONTINENT": "North America",
      "CML_COUNTRY": "United States",
      "CML_COUNTRY_CODE": "US",
      "CML_CURRENCY_TYPE": "$",
      "CML_DESCRIPTION": "",
      "CML_LATITUDE": 37.7749295,
      "CML_LOCATION": "San Francisco, CA, USA",
      "CML_LONGITUDE": -122.4194155,
      "CML_ORG_LOGO": [
        "/hdfs/genis.cooper@clouzer.com/Cloud Vault/Media/Upload/2020/Apr/1587702464114_1537_mirvacclzbuilder.png"
      ],
      "CML_ORG_PHONE": 0,
      "CML_ORG_REF_LOGO": [
        "/hdfs/jenny.brown@clouzer.com/Cloud Vault/Media/Upload/2020/Apr/1587702522219_2427_cloudsclzlogoclzorangeclzbgclzclz4clz.png"
      ],
      "CML_ORG_REF_PHONE": 0,
      "CML_ORG_REF_TITLE": "Clouds Distributor",
      "CML_ORG_TITLE": "Mirvac",
      "CML_ORG_WEB_SITE": "mirvac.clouzer.com",
      "CML_ORIGINAL_SERVICE_ID": [
        "faservices.clouzer.com#PRJ_ORG_WKS_1587702874044_4647#SEC_WIZ_SRV_0015#TSK_SRV_LST_1587702917632_33"
      ],
      "CML_PROPERTY_ID": "willough.mirvac.clouzer.com#PRJ_ORG_WKS_1587709191269_3592",
      "CML_PROPERTY_NAME": "Willough",
      "CML_PROP_SERIAL_ID": "MIR-PRP-158770919126890",
      "CML_REF_ID": "faservices.clouzer.com#PRJ_AGN_123456_5#SEC_AGN_123456_5",
      "CML_REQUEST_COMMENT": "Mirvac wants to book and appointment MIR-APT-15877094204220 for Home Automation Installation service for Clouds Distributor org at San Francisco, CA, USA.",
      "CML_SERIAL_ID": "MIR-APT-15877094204220",
      "CML_SERVICE_PROVIDERS": true,
      "CML_STATE": "California",
      "CML_SUB_CATEGORY": "faservices.clouzer.com#PRJ_ORG_WKS_1587702874044_4647",
      "CML_TIMEZONE": 25200000,
      "CML_TITLE": "Appointment for Willough from Mirvac",
      "CML_ZIPCODE": 94103,
      "CONTACT_DETAILS": {},
      "CREATED_BY": "genis.cooper@mirvac.clouzer.com",
      "CREATED_ON": "2020-04-24T06:23:24.622Z",
      "CREATED_USER": "mirvac.clouzer.com#PRJ_ORG_WKS_1587702504656_5708",
      "CREATE_IP": "",
      "DEPT_PROJECT_ID": "faservices.clouzer.com#PRJ_ORG_WKS_1587702874044_4647",
      "IS_USER_REGISTER": true,
      "KEY_TYPE": "TSK",
      "KEY_VAL": "faservices.clouzer.com#PRJ_AGN_123456_5#SEC_AGN_123456_5#TSK_MAPT_1587709420678_5944",
      "LAST_MODIFIED_BY": "genis.cooper@mirvac.clouzer.com",
      "LAST_MODIFIED_ON": "2020-04-24T06:23:24.622Z",
      "ORG_PROJECT_ID": "faservices.clouzer.com#PRJ_ORG_WKS_1587702874044_4647",
      "PARENT_WIZARD_ID": "mirvac.clouzer.com#PRJ_AGN_123456_5#SEC_AGN_123456_5",
      "SRV_FA -SRV-158770291770692": {
        "CML_TITLE": "Home Automation Installation",
        "CML_SERIAL_ID": "FA -SRV-158770291770692",
        "FROM_TO_TIME": [
          {
            "CML_FROM_DATETIME": "2020-04-24T07:30:00.484Z",
            "CML_TO_DATETIME": "2020-04-24T08:30:00.484Z"
          }
        ],
        "CML_COST": 50,
        "CML_ESTIMATED_TIME": 1,
        "CML_DISCOUNT": 0,
        "CML_CURRENCY_TYPE": "$",
        "CML_DISCOUNT_TYPE": "%",
        "KEY_VAL": "faservices.clouzer.com#PRJ_ORG_WKS_1587702874044_4647#SEC_WIZ_SRV_0015#TSK_SRV_LST_1587702917632_33",
        "SUB_KEY_TYPE": "TSK_PSRV",
        "CML_COUNT": 2,
        "CML_SERVICE_PROVIDERS": [
          "faservices.clouzer.com#PRJ_DEPT_ORG_1231231231231_1234#SEC_WIZ_ROLE_0001#TSK_ROL_LST_0002"
        ]
      },
      "SUB_KEY_TYPE": "TSK_MAPT",
      "SYNC_PENDING_STATUS": 1,
      "UPDATE_IP": "",
      "USER_LAST_MODIFIED_ON": "2020-04-24T06:23:24.622Z",
      "isPackageAppointment": true
    }
  ]
}
```
