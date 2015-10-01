## Retrieve private profile

> **Definition**

```text
GET https://api.fabriq.io/profiles/private
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/profiles/private'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
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
    "personal_identifiers": "birth mark right calf",
    "medical_conditions": null,
    "allergies": "gluten, penicillin",
    "medications": null,
    "emergency_instructions": null
}
```

### Returns
The user's private profile object.
