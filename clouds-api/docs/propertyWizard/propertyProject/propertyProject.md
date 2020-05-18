# Appointment Wizard API

Guide to all API of Appointment Wizard.

---

## Introduction

Appointment wizard is used for booking services for services provider organization or
distributor organization.

## **ASSIGN_APPOINTMENT**

This API used when user assign a appointment to user who has right to handle
appointment request at services provider org.

### Assign Appointment Impact

!!! note

    1) Same services man Can be assign to different slot.

    2) After assigning appointment to service man , appointment get replicated to assign user urm.

    3) Property Replicated at installer side 

    4) Appointment get updated in installer and builder org also.


#### Assign Appointment Request:-

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
        "SRV_SS -SRV-157320214349699": {
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
        },
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



