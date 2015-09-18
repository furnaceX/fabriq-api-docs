## Error Codes


Error Codes ||
---------------- | -----------  
200<br>*OK*	| Everything worked as expected
400<br>*Bad Request*	| Request received with a missing or invalid parameter
401<br>*Unauthorized*	| An access_token or client_id was invalid or not provided
403<br>*Not Allowed*	| The request was valid but user not allowed to access the item
404<br>*Not Found*	| The requested item doesn't exist
412<br>*Validation Error*	| The request was valid but could not be completed because a condition was not met. For example, specifying to alert a circle that does not have any verified contacts would result in this error
429<br>*Too Many Requests*	| Too many requests hit the API too quickly
500<br>*Server Error* | Internal FABRIQ server error
