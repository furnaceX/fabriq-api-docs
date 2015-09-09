# Errors

FABRIQ uses standard HTTP response codes to indicate the status of an API request. In general, codes in the 2xx range indicate success, codes in the 4xx range indicate an error that resulted from the provided information (e.g. a required parameter was missing), and codes in the 5xx range indicate an internal
system or server error.

Error Codes ||
---------------- | -----------  
200<br>*OK*	| Everything worked as expected
400<br>*Bad Request*	| Request received with a missing or invalid parameter
401<br>*Unauthorized*	| An access_token or client_id was invalid or not provided
402<br>*Request Failed*	| Parameters were valid but request failed
404<br>*Not Found*	| The requested item doesn't exist
429<br>*Too Many Requests*	| Too many requests hit the API too quickly
500<br>*Server Error*| FABRIQ server error
