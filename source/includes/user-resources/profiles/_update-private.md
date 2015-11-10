## Update private profile

> **Definition**

```text
PUT https://api.fabriq.io/profiles/private
```

> **Sample Request**

```shell
curl -X PUT 'https://api.fabriq.io/profiles/private'        \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -H 'Content-Type: application/json'         \
  -d '{                                        
        "driver_license": "NY I1234562"
      }'
```

> **Sample Response**

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
    "emergency_contacts": null,
    "next_of_kin": null,
    "personal_identifiers": "birth mark right calf",
    "medical_conditions": null,
    "allergies": "gluten, penicillin",
    "medications": null,
    "emergency_instructions": null,
    "media": null
}
```

To update the user's `email` or `mobile_number` update the [User](#the-user-object) object directly.

<br>

ARGUMENTS ||
---------:        | -----------
twitter_url <br>*optional*, *string*  | Link to user's twitter account
facebook_url <br>*optional*, *string*  | Link to user's facebook account
linkedin_url <br>*optional*, *string*  | Link to user's linkedin account
instagram_url <br>*optional*, *string*  | Link to user's instagram account
driver_license <br>*optional*, *string*  | Driver's license number (should include country/state)
license_plate <br>*optional*, *string*  | License plate number (should include country/state)
employer_name <br>*optional*, *string*  | Name of user's school or employer
employer_address <br>*optional*, *string*  | Address of user' school or employer
employer_phone_number <br>*optional*, *string*  | Phone number of user's school or employer
residence1_address <br>*optional*, *string*  | User's primary address
residence2_address <br>*optional*, *string*  | User's second address
residence3_address <br>*optional*, *string*  | User's third address
residence4_address <br>*optional*, *string*  | User's fourth address
doctor_name <br>*optional*, *string*  | Primary physician's name
doctor_address <br>*optional*, *string*  | Primary physician's address
doctor_phone_number <br>*optional*, *string*  | Primary physician's phone number
dentist_name <br>*optional*, *string*  | Dentist's name
dentist_address <br>*optional*, *string*  | Dentist's address
dentist_phone_number <br>*optional*, *string*  | Dentist's phone number
emergency_contacts <br>*optional*, *string*  | Additional emergency contacts
personal_identifiers <br>*optional*, *string*  | Any identifying marks such as scars, tatoos, etc.
medical_conditions <br>*optional*, *string*  | List of all known medical conditions
allergies <br>*optional*, *string*  | List of all known allergies
medications <br>*optional*, *string*  | List of medications user is currently taking
emergency_instructions <br>*optional*, *string*  | Instructions for specific emergencies


### Returns
Return the updated private profile object.
