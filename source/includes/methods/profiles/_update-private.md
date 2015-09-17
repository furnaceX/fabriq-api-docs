## Update private profile

> Definition

```text
PUT https://api.fabriq.io/profiles/private
```

> Sample Request

```shell
curl -X PUT 'https://api.fabriq.io/profiles/private'        \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -H 'Content-Type: application/json'         \
  -d '{                                        
        "driver_license": "NY I1234562"
      }'
```

> Sample Response

```json
{
    "email": "jane@example.com",
    "mobile_number": "+12125551212",
    "twitter_url": "https://twitter.com/janedoe",
    "facebook_url": "https://facebook.com/janedoe",
    "linkedin_url": null,
    "instagram_url": null,
    "driver_license": "NY I1234562",
    "license_plate": "NY 5NQE861",
    "employer_name": "City University",
    "employer_address": "100 Campus St., New York, NY 12345",
    "employer_phone_number": "+12125551212",
    "residence1_address": "123 Main St., New York, NY 12345",
    "residence2_address": "456 Any St., San Francisco, CA 54321",
    "residence3_address": null,
    "residence4_address": null,
    "doctor_name": "Dr. Jane Smith",
    "doctor_address": "123 Main St., New York, NY 12345",
    "doctor_phone_number": "+12125551212",
    "dentist_name": "Dr. John Doe",
    "dentist_address": "123 Main St., New York, NY 12345",
    "dentist_phone_number": "+12125551212",
    "personal_identifiers": "birth mark right calf",
    "medical_conditions": null,
    "allergies": "gluten, penicillin",
    "medications": null,
    "emergency_instructions": null
}
```


ARGUMENTS ||
---------:        | -----------
first_name <br>*optional*  |  -
last_name <br>*optional*  |  -
display_name <br>*optional*  |  -
birth_date <br>*optional*  |  -
gender <br>*optional*  |  -
height <br>*optional*  |  -
weight <br>*optional*  |  -
race <br>*optional*  |  -
eye_color <br>*optional*  |  -
hair_color <br>*optional*  |  -
photo_data <br>*optional*  |  -
photo_content_type <br>*optional*  |  -
photo_size <br>*optional*  |  -


### Returns
Return the updated profile object.
