# Purchase Main Appointment (TSK_OAPT)

## ** Introduction **

Appointment wizard is used for booking appointment for a service from services provider organization or
distributor organization and this section contain all the API and Document detail for builder side org
, where client take action on appointment or book appointment for any services provider org.

List of API used for  subKeyType (**TSK_MAPT**).

- Book Appointment API
- Cancel Appointment API

---

## ** Book Appointment **

This API used when user book  appointment for any services through distributor
or services provider organization.

* `BeanId`       - INSERT#SRV#TSK#TSK_MAPT#BOOK_APT_BUD
* `actionArray`  - ** BOOK_APT_BUD **
* `Service Name` - APT_CLZ_COM
* `Flow Diagram` - [link](https://app.diagrams.net/#G10zTC0x5hrtfKyqs-Tgi6dUSEb6_FJ_w0)

### ** Parameters **

Parameter name                | Data Type           | Description
------------                  | -------------   |---------------------
CML_ORIGINAL_SERVICE_ID       | JsonArray       | contain KEY_VAL of services for which appointment is book
SRV_DETAILS                   | JsonArray       | contain details of services like its CML_SERIAL_ID , slot details , services name 
isPackageAppointment          | boolean         | true = appointment book for product serives package and false = only for services
CML_PROPERTY_ID               | String          | property keyVal
CML_PROPERTY_NAME             | String          | property name for under which appointment is book
CML_PROP_SERIAL_ID            | String          | property serialId (unique Id generate for each property)


### ** Book Appointment Request on APT_CLZ_COM ** :-

```yaml
{
  "userIdas": "scm.cli@builderorgc.clouzer.com",
  "action": "INSERT",
  "dataArray": [
    {
      "actionArray": [
        "BOOK_APPOINTMENT"
      ],
      "calmailObject": {
        "ACTIVE_STATUS": 1,
        "CML_TITLE": "Appointment for Messi from BuilderOrgC",
        "CML_REF_ID": "scm.cli@builderorgc.clouzer.com#PRJ_AGN_123_2#SEC_AGN_0002_0017",
        "KEY_TYPE": "TSK",
        "CML_SUB_CATEGORY": "builderorgc.clouzer.com#PRJ_ORG_WKS_1586953186624_3762",
        "SUB_KEY_TYPE": "TSK_OAPT",
        "SYNC_PENDING_STATUS": 0,
        "CML_TEMP_KEY_VAL": "undefined#TSK_OAPT#scm.cli@builderorgc.clouzer.com:1587023237130_18822755418_10980",
        "DEPT_PROJECT_ID": "builderorgc.clouzer.com#PRJ_ORG_WKS_1586953186624_3762",
        "ORG_PROJECT_ID": "builderorgc.clouzer.com#PRJ_ORG_WKS_1586953186624_3762",
        "CREATE_IP": "192.168.1.5",
        "UPDATE_IP": "192.168.1.5",
        "USER_LAST_MODIFIED_ON": "2020-04-16T07:46:59.516Z",
        "CML_DESCRIPTION": "",
        "CML_ORG_WEB_SITE": "builderorgc.clouzer.com",
        "PARENT_WIZARD_ID": "builderorgc.clouzer.com#PRJ_AGN_123456_5#SEC_AGN_123456_5",
        "CREATED_ON": "2020-04-16T07:46:59.516Z",
        "CML_LOCATION": "\"EEPSIT\" Balwantpuram, S. No. 110/1/A, Off Paud Road, Kothrud, Shivtirthanagar, Matoba Nagar, Kothrud, Pune, Maharashtra 411038, India",
        "CML_COUNTRY": "India",
        "CML_STATE": "Maharashtra",
        "CML_CITY": "Pune",
        "CML_ZIPCODE": "411038",
        "CML_COUNTRY_CODE": "IN",
        "CML_LONGITUDE": 73.80668109999999,
        "CML_LATITUDE": 18.5138812,
        "CML_CONTINENT": "Asia",
        "CML_TIMEZONE": -19800000,
        "CML_ORG_REF_TITLE": "DIstributorOrgC",
        "CML_ORG_REF_LOGO": [],
        "CML_PROP_SERIAL_ID": "BUI-PRP-158702310478263",
        "CML_PROPERTY_ID": "messi.builderorgc.clouzer.com#PRJ_ORG_WKS_1587023104749_9518",
        "CML_PROPERTY_NAME": "Messi",
        "CML_ORG_TITLE": "BuilderOrgC",
        "CML_ORG_LOGO": [],
        "CREATED_USER": "builderorgc.clouzer.com#PRJ_ORG_WKS_1586953186624_3762",
        "CONTACT_DETAILS": {},
        "CML_ORG_PHONE": 1234567890,
        "CML_ORG_REF_PHONE": 0,
        "IS_USER_REGISTER": true,
        "CML_ORIGINAL_SERVICE_ID": [
          "servicesorgc.clouzer.com#PRJ_ORG_WKS_1586953118819_2873#SEC_WIZ_SRV_0015#TSK_SRV_LST_1586953364340_68"
        ],
        "SRV_DETAILS": [
        {
          "CML_TITLE": "ISP Installation",
          "CML_SERIAL_ID": "SER-SRV-158695336445283",
          "FROM_TO_TIME": [
            {
              "CML_FROM_DATETIME": "2020-04-16T05:00:00.052Z",
              "CML_TO_DATETIME": "2020-04-16T06:00:00.052Z"
            }
          ],
          "CML_COST": 50,
          "CML_ESTIMATED_TIME": 1,
          "CML_DISCOUNT": 0,
          "CML_CURRENCY_TYPE": "$",
          "CML_DISCOUNT_TYPE": "%",
          "KEY_VAL": "messi.builderorgc.clouzer.com#PRJ_ORG_WKS_1587023104749_9518#SEC_PRP_PKG_001#TSK_PRPS_PKG_1587023169430_45#TSK_SRV_SUM_1587023169438_71",
          "SUB_KEY_TYPE": "TSK_PSRV",
          "CML_COUNT": 1,
          "CML_SERVICE_PROVIDERS": [
            "servicesorgc.clouzer.com#PRJ_DEPT_ORG_1231231231231_1234#SEC_WIZ_ROLE_0001#TSK_ROL_LST_0002"
          ]
        }
        ],
        "isPackageAppointment": true
      },
      "inviteeList": [
        {
          "IDE_ATTENDEES_EMAIL": "distributororgc.clouzer.com#PRJ_ORG_WKS_1586953163209_1134",
          "IDE_TYPE": "FROM",
          "KEY_TYPE": "IDE",
          "SUB_KEY_TYPE": "TSK_AEVT"
        },
        {
          "IDE_ATTENDEES_EMAIL": "builderorgc.clouzer.com#PRJ_ORG_WKS_1586953186624_3762",
          "IDE_TYPE": "TO",
          "KEY_TYPE": "IDE",
          "SUB_KEY_TYPE": "TSK_AEVT"
        }
      ],
      "essentialList": [
        {
          "CML_PRJ_REF_ID": "distributororgc.clouzer.com#PRJ_ORG_WKS_1586953163209_1134",
          "IS_BTOB_FLOW": true
        }
      ]
    }
  ],
  "moduleName": "SRV",
  "requestId": "/sync#/sync#MG52YDWv9qfA4xcyAAAdscm.cli@builderorgc.clouzer.com#1587023237131r133r292",
  "FROM": "senddatatoserver",
  "socketId": "/sync#O3i55c3rnaD_9zI3AAAZ",
  "topic": "CCR_CLZ_COM"
}
```

###  **  Book Appointment Response on BROADCAST ** :-

```yaml
{
  "userId": "genis.cooper@mirvac.clouzer.com",
  "action": "INSERT",
  "moduleName": "SRV",
  "requestId": "/sync#/sync#nvoZGqXc2cGVncWfAAuKgenis.cooper@mirvac.clouzer.com#1587726025649r196r233",
  "FROM": "senddatatoserver",
  "socketId": "/sync#XCEDmfndPuKo1MDMAAtm",
  "topic": "CCR_CLZ_COM",
  "dataArray": [
    {
      "actionArray": [
        "BOOK_APT_BUD"
      ],
      "calmailObject": {
        "ACTIVE_STATUS": 1,
        "CML_TITLE": "Appointment for Aeres from Mirvac",
        "CML_REF_ID": "mirvac.clouzer.com#PRJ_AGN_123456_5#SEC_AGN_123456_5",
        "KEY_TYPE": "TSK",
        "CML_SUB_CATEGORY": "mirvac.clouzer.com#PRJ_ORG_WKS_1587702504656_5708",
        "SUB_KEY_TYPE": "TSK_OAPT",
        "SYNC_PENDING_STATUS": 1,
        "CML_TEMP_KEY_VAL": "undefined#TSK_OAPT#genis.cooper@mirvac.clouzer.com:1587726025649_19767377292_18263",
        "DEPT_PROJECT_ID": "mirvac.clouzer.com#PRJ_ORG_WKS_1587702504656_5708",
        "ORG_PROJECT_ID": "mirvac.clouzer.com#PRJ_ORG_WKS_1587702504656_5708",
        "CREATE_IP": "",
        "UPDATE_IP": "",
        "USER_LAST_MODIFIED_ON": "2020-04-24T11:00:18.307Z",
        "CML_DESCRIPTION": "",
        "CML_ORG_WEB_SITE": "mirvac.clouzer.com",
        "PARENT_WIZARD_ID": "mirvac.clouzer.com#PRJ_AGN_123456_5#SEC_AGN_123456_5",
        "CREATED_ON": "2020-04-24T11:00:18.307Z",
        "CML_LOCATION": "San Francisco, CA, USA",
        "CML_COUNTRY": "United States",
        "CML_STATE": "California",
        "CML_CITY": "San Francisco County",
        "CML_ZIPCODE": 94103,
        "CML_COUNTRY_CODE": "US",
        "CML_LONGITUDE": -122.4194155,
        "CML_LATITUDE": 37.7749295,
        "CML_CONTINENT": "North America",
        "CML_TIMEZONE": 25200000,
        "CML_ORG_REF_TITLE": "Clouds Distributor",
        "CML_ORG_REF_LOGO": [
          "/hdfs/jenny.brown@clouzer.com/Cloud Vault/Media/Upload/2020/Apr/1587702522219_2427_cloudsclzlogoclzorangeclzbgclzclz4clz.png"
        ],
        "CML_PROP_SERIAL_ID": "MIR-PRP-158772558806284",
        "CML_PROPERTY_ID": "aeres.mirvac.clouzer.com#PRJ_ORG_WKS_1587725588063_2455",
        "CML_PROPERTY_NAME": "Aeres",
        "CML_ORG_TITLE": "Mirvac",
        "CML_ORG_LOGO": [
          "/hdfs/genis.cooper@clouzer.com/Cloud Vault/Media/Upload/2020/Apr/1587702464114_1537_mirvacclzbuilder.png"
        ],
        "CREATED_USER": "mirvac.clouzer.com#PRJ_ORG_WKS_1587702504656_5708",
        "CONTACT_DETAILS": {},
        "CML_ORG_PHONE": 0,
        "CML_ORG_REF_PHONE": 0,
        "IS_USER_REGISTER": true,
        "CML_ORIGINAL_SERVICE_ID": [
          "faservices.clouzer.com#PRJ_ORG_WKS_1587702874044_4647#SEC_WIZ_SRV_0015#TSK_SRV_LST_1587702917632_33"
        ],
        "SRV_FA -SRV-158770291770692": {
          "CML_TITLE": "Home Automation Installation",
          "CML_SERIAL_ID": "FA -SRV-158770291770692",
          "FROM_TO_TIME": [
            {
              "CML_FROM_DATETIME": "2020-04-24T08:30:00.623Z",
              "CML_TO_DATETIME": "2020-04-24T09:30:00.623Z"
            }
          ],
          "CML_COST": 50,
          "CML_ESTIMATED_TIME": 1,
          "CML_DISCOUNT": 0,
          "CML_CURRENCY_TYPE": "$",
          "CML_DISCOUNT_TYPE": "%",
          "KEY_VAL": "aeres.mirvac.clouzer.com#PRJ_ORG_WKS_1587725588063_2455#SEC_PRP_PKG_001#TSK_PRPS_PKG_1587725693567_57#TSK_SRV_SUM_1587725693657_61",
          "SUB_KEY_TYPE": "TSK_PSRV",
          "CML_COUNT": 2,
          "CML_SERVICE_PROVIDERS": [
            "faservices.clouzer.com#PRJ_DEPT_ORG_1231231231231_1234#SEC_WIZ_ROLE_0001#TSK_ROL_LST_0002"
          ]
        },
        "isPackageAppointment": true,
        "KEY_VAL": "mirvac.clouzer.com#PRJ_AGN_123456_5#SEC_AGN_123456_5#TSK_OAPT_1587726028918_4865",
        "CML_SERIAL_ID": "MIR-APT-158772602891145",
        "CREATED_BY": "genis.cooper@mirvac.clouzer.com",
        "LAST_MODIFIED_BY": "genis.cooper@mirvac.clouzer.com",
        "LAST_MODIFIED_ON": "2020-04-24T11:00:18.307Z",
        "LISTING_IDS": {
          "genis.cooper@mirvac.clouzer.com#PRJ_AGN_123_2#SEC_AGN_0002_0017": "genis.cooper@mirvac.clouzer.com#PRJ_AGN_123_2#SEC_AGN_0002_0017#TSK_OAPT_1587726028902_5575"
        },
        "LISTING_ID": "mirvac.clouzer.com#PRJ_AGN_123456_5#SEC_AGN_123456_5#TSK_OAPT_1587726028918_4865"
      }
    }
  ]
}
```
