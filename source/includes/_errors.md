# Errors

<aside class="notice">This is the error section .</aside>

The Contact API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is not found 
404 | Not Found -- The specified contact/id could not be found
405 | Method Not Allowed -- You tried to access a contact with an invalid method
406 | Not Acceptable -- You requested a command that is not accetable ( invalid data type)
410 | Gone -- The contact requested has been removed from our database
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarially offline for maintanance. Please try again later.
