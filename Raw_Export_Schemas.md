#  Schemas

All tables are updated daily, adding the results from the previous day. The date and timestamp of the events are present in all tables:

## Acquisition File

This file contains all acquisition events. These events are the only ones that come from the acquisition callback, not from our SDK, this is why they don’t contain our common variables.

```
{
    "arrival_ts": long (nullable = true),
    "data": {
        "attribution_partner": string (nullable = true),
        "google_aid": string (nullable = true),
        "install_campaign": string (nullable = true),
        "install_publisher": string (nullable = true),
        "install_site": string (nullable = true),
        "ios_idfa": string (nullable = true),
        "ios_idfv": string (nullable = true)
    },
    "game_id": long (nullable = true),
    "multi_message": boolean (nullable = true),
    "public_key": string (nullable = true)
}
```


## Ads Table

This table contains all ads events.

```
{
  "arrival_ts": long (nullable = true),
  "country_code": string (nullable = true),
  "data": {
    "ab_id": string (nullable = true),
    "ab_variant_id": string (nullable = true),
    "ad_action": string (nullable = true),
    "ad_placement": string (nullable = true),
    "ad_sdk_name": string (nullable = true),
    "ad_type": string (nullable = true),
    "android_app_build": string (nullable = true),
    "android_app_signature": string (nullable = true),
    "android_app_version": string (nullable = true),
    "android_bundle_id": string (nullable = true),
    "android_channel_id": string (nullable = true),
    "android_id": string (nullable = true),
    "android_mac_md5": string (nullable = true),
    "android_mac_sha1": string (nullable = true),
    "build": string (nullable = true),
    "category": string (nullable = true),
    "client_ts": long (nullable = true),
    "configuration_keys": array (nullable = true),
    "element": string (containsNull = true),
    "configurations": array (nullable = true),
    "connection_type": string (nullable = true),
    "device": string (nullable = true),
    "engine_version": string (nullable = true),
    "google_aid": string (nullable = true),
    "google_aid_src": string (nullable = true),
    "ios_app_build": string (nullable = true),
    "ios_app_version": string (nullable = true),
    "ios_att": string (nullable = true),
    "ios_bundle_id": string (nullable = true),
    "ios_idfa": string (nullable = true),
    "ios_idfv": string (nullable = true),
    "ios_testflight": boolean (nullable = true),
    "jailbroken": boolean (nullable = true),
    "limited_ad_tracking": boolean (nullable = true),
    "manufacturer": string (nullable = true),
    "os_version": string (nullable = true),
    "platform": string (nullable = true),
    "sdk_version": string (nullable = true),
    "session_id": string (nullable = true),
    "session_num": long (nullable = true),
    "user_id": string (nullable = true),
    "v": long (nullable = true)
  },
  "first_in_batch": boolean (nullable = true),
  "game_id": long (nullable = true),
  "ip": string (nullable = true),
  "user_meta": {
    "attribution_partner": string (nullable = true),
    "cohort_month": long (nullable = true),
    "cohort_week": long (nullable = true),
    "first_build": string (nullable = true),
    "install_campaign": string (nullable = true),
    "install_hour": long (nullable = true),
    "install_publisher": string (nullable = true),
    "install_site": string (nullable = true),
    "install_ts": long (nullable = true),
    "is_converting": string (nullable = true),
    "is_paying": string (nullable = true),
    "origin": string (nullable = true),
    "pay_ft": long (nullable = true),
    "revenue": Currency type, depending on the currency, e.g. "EUR"
  }
}
```


##  Business File

This file contains all business events.

```
{
  "arrival_ts": long (nullable = true),
  "country_code": string (nullable = true),
  "data": {
    "ab_id": string (nullable = true),
    "ab_variant_id": string (nullable = true),
    "amount": long (nullable = true),
    "amount_usd": double (nullable = true),
    "android_app_build": string (nullable = true),
    "android_app_signature": string (nullable = true),
    "android_app_version": string (nullable = true),
    "android_bundle_id": string (nullable = true),
    "android_channel_id": string (nullable = true),
    "android_id": string (nullable = true),
    "android_mac_md5": string (nullable = true),
    "android_mac_sha1": string (nullable = true),
    "build": string (nullable = true),
    "cart_type": string (nullable = true),
    "category": string (nullable = true),
    "client_ts": long (nullable = true),
    "configuration_keys": array (nullable = true),
    "element": string (containsNull = true),
    "configurations": array (nullable = true),
    "connection_type": string (nullable = true),
    "country_code": string (nullable = true),
    "currency": string (nullable = true),
    "device": string (nullable = true),
    "engine_version": string (nullable = true),
    "event_id": string (nullable = true),
    "google_aid": string (nullable = true),
    "google_aid_src": string (nullable = true),
    "ios_app_build": string (nullable = true),
    "ios_app_version": string (nullable = true),
    "ios_att": string (nullable = true),
    "ios_bundle_id": string (nullable = true),
    "ios_idfa": string (nullable = true),
    "ios_idfv": string (nullable = true),
    "jailbroken": boolean (nullable = true),
    "limited_ad_tracking": boolean (nullable = true),
    "manufacturer": string (nullable = true),
    "oaid": string (nullable = true),
    "os_version": string (nullable = true),
    "platform": string (nullable = true),
    "receipt_info": {
      "receipt": string (nullable = true),
      "receipt_id": string (nullable = true),
      "signature": string (nullable = true),
      "store": string (nullable = true)
    },
    "sdk_version": string (nullable = true),
    "session_id": string (nullable = true),
    "session_num": long (nullable = true),
    "transaction_num": long (nullable = true),
    "user_id": string (nullable = true),
    "v": long (nullable = true)
  },
  "first_in_batch": boolean (nullable = true),
  "game_id": long (nullable = true),
  "ip": string (nullable = true),
  "user_meta": {
    "attribution_partner": string (nullable = true),
    "cohort_month": long (nullable = true),
    "cohort_week": long (nullable = true),
    "first_build": string (nullable = true),
    "install_campaign": string (nullable = true),
    "install_hour": long (nullable = true),
    "install_publisher": string (nullable = true),
    "install_site": string (nullable = true),
    "install_ts": long (nullable = true),
    "is_converting": string (nullable = true),
    "is_paying": string (nullable = true),
    "origin": string (nullable = true),
    "pay_ft": long (nullable = true),
    "receipt_status": string (nullable = true),
    "revenue": Currency type, depending on the currency, e.g. "EUR"
  }
}
```


## Design File

This file contains all design events.

```
{
  "arrival_ts": long (nullable = true),
  "country_code": string (nullable = true),
  "data": {
    "ab_id": string (nullable = true),
    "ab_variant_id": string (nullable = true),
    "android_app_build": string (nullable = true),
    "android_app_signature": string (nullable = true),
    "android_app_version": string (nullable = true),
    "android_bundle_id": string (nullable = true),
    "android_channel_id": string (nullable = true),
    "android_id": string (nullable = true),
    "android_mac_md5": string (nullable = true),
    "android_mac_sha1": string (nullable = true),
    "build": string (nullable = true),
    "category": string (nullable = true),
    "client_ts": long (nullable = true),
    "configuration_keys": array (nullable = true),
    "element": string (containsNull = true),
    "configurations": array (nullable = true),
    "connection_type": string (nullable = true),
    "device": string (nullable = true),
    "engine_version": string (nullable = true),
    "event_id": string (nullable = true),
    "google_aid": string (nullable = true),
    "google_aid_src": string (nullable = true),
    "ios_app_build": string (nullable = true),
    "ios_app_version": string (nullable = true),
    "ios_att": string (nullable = true),
    "ios_bundle_id": string (nullable = true),
    "ios_idfa": string (nullable = true),
    "ios_idfv": string (nullable = true),
    "ios_testflight": boolean (nullable = true),
    "jailbroken": boolean (nullable = true),
    "limited_ad_tracking": boolean (nullable = true),
    "manufacturer": string (nullable = true),
    "oaid": string (nullable = true),
    "os_version": string (nullable = true),
    "platform": string (nullable = true),
    "sdk_version": string (nullable = true),
    "session_id": string (nullable = true),
    "session_num": long (nullable = true),
    "user_id": string (nullable = true),
    "v": long (nullable = true),
    "value": string (nullable = true)
  },
  "first_in_batch": boolean (nullable = true),
  "game_id": long (nullable = true),
  "ip": string (nullable = true),
  "user_meta": {
    "attribution_partner": string (nullable = true),
    "cohort_month": long (nullable = true),
    "cohort_week": long (nullable = true),
    "first_build": string (nullable = true),
    "install_campaign": string (nullable = true),
    "install_hour": long (nullable = true),
    "install_keyword": string (nullable = true),
    "install_publisher": string (nullable = true),
    "install_site": string (nullable = true),
    "install_ts": long (nullable = true),
    "is_converting": string (nullable = true),
    "is_paying": string (nullable = true),
    "origin": string (nullable = true),
    "pay_ft": long (nullable = true),
    "revenue": Currency type, depending on the currency, e.g. "EUR",
    "site_id": string (nullable = true)
  }
}
```


## Error File

This file contains all error events.
```
{
    "arrival_ts": long (nullable = true),
    "country_code": string (nullable = true),
    "data": {
        "ab_id": string (nullable = true),
        "ab_variant_id": string (nullable = true),
        "android_app_build": string (nullable = true),
        "android_app_signature": string (nullable = true),
        "android_app_version": string (nullable = true),
        "android_bundle_id": string (nullable = true),
        "android_channel_id": string (nullable = true),
        "android_id": string (nullable = true),
        "android_mac_md5": string (nullable = true),
        "android_mac_sha1": string (nullable = true),
        "build": string (nullable = true),
        "category": string (nullable = true),
        "client_ts": long (nullable = true),
        "configuration_keys": array (nullable = true),
        "element": string (containsNull = true),
        "configurations": array (nullable = true),
        "connection_type": string (nullable = true),
        "country_code": string (nullable = true),
        "device": string (nullable = true),
        "engine_version": string (nullable = true),
        "google_aid": string (nullable = true),
        "google_aid_src": string (nullable = true),
        "ios_app_build": string (nullable = true),
        "ios_app_version": string (nullable = true),
        "ios_att": string (nullable = true),
        "ios_bundle_id": string (nullable = true),
        "ios_idfa": string (nullable = true),
        "ios_idfv": string (nullable = true),
        "ios_testflight": boolean (nullable = true),
        "jailbroken": boolean (nullable = true),
        "limited_ad_tracking": boolean (nullable = true),
        "manufacturer": string (nullable = true),
        "message": string (nullable = true),
        "oaid": string (nullable = true),
        "os_version": string (nullable = true),
        "platform": string (nullable = true),
        "sdk_version": string (nullable = true),
        "session_id": string (nullable = true),
        "session_num": long (nullable = true),
        "severity": string (nullable = true),
        "user_id": string (nullable = true),
        "v": long (nullable = true)
    },
    "first_in_batch": boolean (nullable = true),
    "game_id": long (nullable = true),
    "ip": string (nullable = true),
    "user_meta": {
        "attribution_partner": string (nullable = true),
        "cohort_month": long (nullable = true),
        "cohort_week": long (nullable = true),
        "first_build": string (nullable = true),
        "install_campaign": string (nullable = true),
        "install_hour": long (nullable = true),
        "install_publisher": string (nullable = true),
        "install_site": string (nullable = true),
        "install_ts": long (nullable = true),
        "is_converting": string (nullable = true),
        "is_paying": string (nullable = true),
        "origin": string (nullable = true),
        "pay_ft": long (nullable = true),
        "revenue": Currency type, depending on the currency, e.g. "EUR"
    }
}
```


## Impression File

This file contains all impression events.

```
{
    "arrival_ts": long (nullable = true),
    "country_code": string (nullable = true),
    "data": {
        "ab_id": string (nullable = true),
        "ab_variant_id": string (nullable = true),
        "ad_network_name": string (nullable = true),
        "ad_network_version": string (nullable = true),
        "android_app_build": string (nullable = true),
        "android_app_signature": string (nullable = true),
        "android_app_version": string (nullable = true),
        "android_bundle_id": string (nullable = true),
        "android_channel_id": string (nullable = true),
        "android_id": string (nullable = true),
        "android_mac_md5": string (nullable = true),
        "android_mac_sha1": string (nullable = true),
        "build": string (nullable = true),
        "category": string (nullable = true),
        "client_ts": long (nullable = true),
        "configuration_keys": array (nullable = true),
        "element": string (containsNull = true),
        "configurations": array (nullable = true),
        "connection_type": string (nullable = true),
        "device": string (nullable = true),
        "engine_version": string (nullable = true),
        "google_aid": string (nullable = true),
        "google_aid_src": string (nullable = true),
        "impression_data": {
            "adgroup_id": string (nullable = true),
            "adgroup_name": string (nullable = true),
            "adgroup_priority": long (nullable = true),
            "adgroup_type": string (nullable = true),
            "adunit_format": string (nullable = true),
            "adunit_id": string (nullable = true),
            "adunit_name": string (nullable = true),
            "app_version": string (nullable = true),
            "country": string (nullable = true),
            "creative_id": string (nullable = true),
            "currency": string (nullable = true),
            "demand_partner_data": {
                "encrypted_cpm": string (nullable = true)
            },
            "id": string (nullable = true),
            "network_name": string (nullable = true),
            "network_placement_id": string (nullable = true),
            "placement": string (nullable = true),
            "precision": string (nullable = true),
            "publisher_revenue": double (nullable = true),
            "publisher_revenue_usd_cents": double (nullable = true),
            "revenue": double (nullable = true)
        },
        "ios_app_build": string (nullable = true),
        "ios_app_version": string (nullable = true),
        "ios_att": string (nullable = true),
        "ios_bundle_id": string (nullable = true),
        "ios_idfa": string (nullable = true),
        "ios_idfv": string (nullable = true),
        "jailbroken": boolean (nullable = true),
        "limited_ad_tracking": boolean (nullable = true),
        "manufacturer": string (nullable = true),
        "oaid": string (nullable = true),
        "os_version": string (nullable = true),
        "platform": string (nullable = true),
        "sdk_version": string (nullable = true),
        "session_id": string (nullable = true),
        "session_num": long (nullable = true),
        "user_id": string (nullable = true),
        "v": long (nullable = true)
    },
    "first_in_batch": boolean (nullable = true),
    "game_id": long (nullable = true),
    "ip": string (nullable = true),
    "user_meta": {
        "attribution_partner": string (nullable = true),
        "cohort_month": long (nullable = true),
        "cohort_week": long (nullable = true),
        "first_build": string (nullable = true),
        "install_campaign": string (nullable = true),
        "install_hour": long (nullable = true),
        "install_publisher": string (nullable = true),
        "install_site": string (nullable = true),
        "install_ts": long (nullable = true),
        "is_converting": string (nullable = true),
        "is_paying": string (nullable = true),
        "origin": string (nullable = true),
        "pay_ft": long (nullable = true),
        "revenue": Currency type, depending on the currency, e.g. "EUR"
    }
}
```


## Progression File

This file contains all progression events.
```
{
    "arrival_ts": long (nullable = true),
    "country_code": string (nullable = true),
    "data": {
        "ab_id": string (nullable = true),
        "ab_variant_id": string (nullable = true),
        "android_app_build": string (nullable = true),
        "android_app_signature": string (nullable = true),
        "android_app_version": string (nullable = true),
        "android_bundle_id": string (nullable = true),
        "android_channel_id": string (nullable = true),
        "android_id": string (nullable = true),
        "android_mac_md5": string (nullable = true),
        "android_mac_sha1": string (nullable = true),
        "attempt_num": long (nullable = true),
        "build": string (nullable = true),
        "category": string (nullable = true),
        "client_ts": long (nullable = true),
        "configuration_keys": array (nullable = true),
        "element": string (containsNull = true),
        "configurations": array (nullable = true),
        "connection_type": string (nullable = true),
        "device": string (nullable = true),
        "engine_version": string (nullable = true),
        "event_id": string (nullable = true),
        "google_aid": string (nullable = true),
        "google_aid_src": string (nullable = true),
        "ios_app_build": string (nullable = true),
        "ios_app_version": string (nullable = true),
        "ios_att": string (nullable = true),
        "ios_bundle_id": string (nullable = true),
        "ios_idfa": string (nullable = true),
        "ios_idfv": string (nullable = true),
        "ios_testflight": boolean (nullable = true),
        "jailbroken": boolean (nullable = true),
        "limited_ad_tracking": boolean (nullable = true),
        "manufacturer": string (nullable = true),
        "oaid": string (nullable = true),
        "os_version": string (nullable = true),
        "platform": string (nullable = true),
        "score": long (nullable = true),
        "sdk_version": string (nullable = true),
        "session_id": string (nullable = true),
        "session_num": long (nullable = true),
        "user_id": string (nullable = true),
        "v": long (nullable = true)
    },
    "first_in_batch": boolean (nullable = true),
    "game_id": long (nullable = true),
    "ip": string (nullable = true),
    "user_meta": {
        "attribution_partner": string (nullable = true),
        "cohort_month": long (nullable = true),
        "cohort_week": long (nullable = true),
        "first_build": string (nullable = true),
        "install_campaign": string (nullable = true),
        "install_hour": long (nullable = true),
        "install_keyword": string (nullable = true),
        "install_publisher": string (nullable = true),
        "install_site": string (nullable = true),
        "install_ts": long (nullable = true),
        "is_converting": string (nullable = true),
        "is_paying": string (nullable = true),
        "origin": string (nullable = true),
        "pay_ft": long (nullable = true),
        "revenue": Currency type, depending on the currency, e.g. "EUR",
        "site_id": string (nullable = true)
    }
}
```


## Resource File

This file contains all ressource events.
```
{
  "arrival_ts": long (nullable = true),
  "country_code": string (nullable = true),
  "data": {
      "amount": long (nullable = true),
      "build": string (nullable = true),
      "category": string (nullable = true),
      "client_ts": long (nullable = true),
      "configuration_keys": array (nullable = true),
      "element": string (containsNull = true),
      "configurations": array (nullable = true),
      "connection_type": string (nullable = true),
      "device": string (nullable = true),
      "engine_version": string (nullable = true),
      "event_id": string (nullable = true),
      "ios_app_build": string (nullable = true),
      "ios_app_version": string (nullable = true),
      "ios_att": string (nullable = true),
      "ios_bundle_id": string (nullable = true),
      "ios_idfa": string (nullable = true),
      "ios_idfv": string (nullable = true),
      "jailbroken": boolean (nullable = true),
      "limited_ad_tracking": boolean (nullable = true),
      "manufacturer": string (nullable = true),
      "os_version": string (nullable = true),
      "platform": string (nullable = true),
      "sdk_version": string (nullable = true),
      "session_id": string (nullable = true),
      "session_num": long (nullable = true),
      "user_id": string (nullable = true),
      "v": long (nullable = true)
  },
  "first_in_batch": boolean (nullable = true),
  "game_id": long (nullable = true),
  "ip": string (nullable = true),
  "user_meta": {
      "cohort_month": long (nullable = true),
      "cohort_week": long (nullable = true),
      "first_build": string (nullable = true),
      "install_hour": long (nullable = true),
      "install_ts": long (nullable = true),
      "is_converting": string (nullable = true),
      "is_paying": string (nullable = true),
      "origin": string (nullable = true),
      "pay_ft": long (nullable = true),
      "revenue": Currency type, depending on the currency, e.g. "EUR"
  }
}
```


## Sdkerror File

This file contains all sdkerror events.
```
{
    "arrival_ts": "long (nullable = true)",
    "country_code": "string (nullable = true)",
    "data": {
        "category": "string (nullable = true)",
        "device": "string (nullable = true)",
        "engine_version": "string (nullable = true)",
        "error_action": "string (nullable = true)",
        "error_area": "string (nullable = true)",
        "error_category": "string (nullable = true)",
        "error_parameter": "string (nullable = true)",
        "jailbroken": "boolean (nullable = true)",
        "manufacturer": "string (nullable = true)",
        "os_version": "string (nullable = true)",
        "platform": "string (nullable = true)",
        "reason": "string (nullable = true)",
        "sdk_version": "string (nullable = true)",
        "type": "string (nullable = true)",
        "v": "long (nullable = true)"
    },
    "first_in_batch": "boolean (nullable = true)",
    "game_id": "long (nullable = true)",
    "ip": "string (nullable = true)"
}
```


## Sessionend File 

This file contains all Sessionend events.
```
{
  "arrival_ts": long (nullable = true),
  "country_code": string (nullable = true),
  "data": {
    "ab_id": string (nullable = true),
    "ab_variant_id": string (nullable = true),
    "android_app_build": string (nullable = true),
    "android_app_signature": string (nullable = true),
    "android_app_version": string (nullable = true),
    "android_bundle_id": string (nullable = true),
    "android_channel_id": string (nullable = true),
    "android_id": string (nullable = true),
    "android_mac_md5": string (nullable = true),
    "android_mac_sha1": string (nullable = true),
    "build": string (nullable = true),
    "category": string (nullable = true),
    "client_ts": long (nullable = true),
    "configuration_keys": array (nullable = true),
    "element": string (containsNull = true),
    "configurations": array (nullable = true),
    "connection_type": string (nullable = true),
    "country_code": string (nullable = true),
    "device": string (nullable = true),
    "engine_version": string (nullable = true),
    "google_aid": string (nullable = true),
    "google_aid_src": string (nullable = true),
    "ios_app_build": string (nullable = true),
    "ios_app_version": string (nullable = true),
    "ios_att": string (nullable = true),
    "ios_bundle_id": string (nullable = true),
    "ios_idfa": string (nullable = true),
    "ios_idfv": string (nullable = true),
    "ios_testflight": boolean (nullable = true),
    "jailbroken": boolean (nullable = true),
    "length": long (nullable = true),
    "limited_ad_tracking": boolean (nullable = true),
    "manufacturer": string (nullable = true),
    "oaid": string (nullable = true),
    "os_version": string (nullable = true),
    "platform": string (nullable = true),
    "sdk_version": string (nullable = true),
    "session_id": string (nullable = true),
    "session_num": long (nullable = true),
    "user_id": string (nullable = true),
    "v": long (nullable = true)
  },
  "first_in_batch": boolean (nullable = true),
  "game_id": long (nullable = true),
  "ip": string (nullable = true),
  "user_meta": {
    "attribution_partner": string (nullable = true),
    "cohort_month": long (nullable = true),
    "cohort_week": long (nullable = true),
    "first_build": string (nullable = true),
    "install_campaign": string (nullable = true),
    "install_hour": long (nullable = true),
    "install_keyword": string (nullable = true),
    "install_publisher": string (nullable = true),
    "install_site": string (nullable = true),
    "install_ts": long (nullable = true),
    "is_converting": string (nullable = true),
    "is_paying": string (nullable = true),
    "origin": string (nullable = true),
    "pay_ft": long (nullable = true),
    "revenue": Currency type, depending on the currency, e.g. "EUR",
    "site_id": string (nullable = true)
  }
}
```


## User File

This file contains all user events.

```
{
  "arrival_ts": long (nullable = true),
  "country_code": string (nullable = true),
  "data": {
      "ab_id": string (nullable = true),
      "ab_variant_id": string (nullable = true),
      "android_app_build": string (nullable = true),
      "android_app_signature": string (nullable = true),
      "android_app_version": string (nullable = true),
      "android_bundle_id": string (nullable = true),
      "android_channel_id": string (nullable = true),
      "android_id": string (nullable = true),
      "android_mac_md5": string (nullable = true),
      "android_mac_sha1": string (nullable = true),
      "build": string (nullable = true),
      "category": string (nullable = true),
      "client_ts": long (nullable = true),
      "configuration_keys": array (nullable = true),
      "element": string (containsNull = true),
      "configurations": array (nullable = true),
      "connection_type": string (nullable = true),
      "country_code": string (nullable = true),
      "device": string (nullable = true),
      "engine_version": string (nullable = true),
      "google_aid": string (nullable = true),
      "google_aid_src": string (nullable = true),
      "install": boolean (nullable = true),
      "ios_app_build": string (nullable = true),
      "ios_app_version": string (nullable = true),
      "ios_att": string (nullable = true),
      "ios_bundle_id": string (nullable = true),
      "ios_idfa": string (nullable = true),
      "ios_idfv": string (nullable = true),
      "ios_testflight": boolean (nullable = true),
      "jailbroken": boolean (nullable = true),
      "limited_ad_tracking": boolean (nullable = true),
      "manufacturer": string (nullable = true),
      "oaid": string (nullable = true),
      "os_version": string (nullable = true),
      "platform": string (nullable = true),
      "sdk_version": string (nullable = true),
      "session_id": string (nullable = true),
      "session_num": long (nullable = true),
      "user_id": string (nullable = true),
      "v": long (nullable = true)
  },
  "first_in_batch": boolean (nullable = true),
  "game_id": long (nullable = true),
  "ip": string (nullable = true),
  "user_meta": {
      "attribution_partner": string (nullable = true),
      "cohort_month": long (nullable = true),
      "cohort_week": long (nullable = true),
      "first_build": string (nullable = true),
      "install_campaign": string (nullable = true),
      "install_hour": long (nullable = true),
      "install_keyword": string (nullable = true),
      "install_publisher": string (nullable = true),
      "install_site": string (nullable = true),
      "install_ts": long (nullable = true),
      "is_converting": string (nullable = true),
      "is_paying": string (nullable = true),
      "origin": string (nullable = true),
      "pay_ft": long (nullable = true),
      "revenue": Currency type, depending on the currency, e.g. "EUR",
      "site_id": string (nullable = true)
  }
}
```