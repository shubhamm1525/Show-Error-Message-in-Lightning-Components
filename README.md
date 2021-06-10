# Show-Error-Message-in-Lightning-Components

While working with Lightning Component , we have to do error handling and display the error message to end user using toast message.
But the returned error message can be of DML or Custom Validation.When the error message is displayed it contains Information which might not be important to end user.

Hence we have to Spli the error message string and display appropriate error.

Exmample : 

<b>Error message: Upsert failed. First exception on row 0 with id a0g6w000000SI08AAG; first error: FIELD_CUSTOM_VALIDATION_EXCEPTION, You are allowed to select only one Accounting Product ( Smart Accounting, Smart Accounting: Corporate, Classic Vista, Global Vista, Vista 5, PDEP ) per each individual Production Company: Primary Prod Co Product: [] </b>

This line is not important for end user <b>"Error message: Upsert failed. First exception on row 0 with id a0g6w000000SI08AAG; first error: FIELD_CUSTOM_VALIDATION_EXCEPTION,</b>". So we can remove that part of the error message using the Javascript substring method to remove the unwanted text.

Link for JS Substring method documentation : (https://www.w3schools.com/jsref/jsref_substring.asp)

<b>Error Before :</b>

"Error message: Upsert failed. First exception on row 0 with id a0g6w000000SI08AAG; first error: FIELD_CUSTOM_VALIDATION_EXCEPTION, You are allowed to select only one Accounting Product ( Smart Accounting, Smart Accounting: Corporate, Classic Vista, Global Vista, Vista 5, PDEP ) per each individual Production Company: Primary Prod Co Product: [] "

<b>Error After :</b>
 
"You are allowed to select only one Accounting Product ( Smart Accounting, Smart Accounting: Corporate, Classic Vista, Global Vista, Vista 5, PDEP ) per each individual Production Company: Primary Prod Co Product: [] "
  
  
Note :  This method will not be sutaible for all the scenarios.

