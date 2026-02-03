## Overview
This QA project tests, the API provided by the website Restful-Booker (https://restful-booker.herokuapp.com/). The project can be imported and ran in Postman or through command line using Newman. Currently runs 4 tests using the data stored in bookingData.csv file located Postman Collections folder.

## Created With
| Name | Version |
| --- | --- |
| [Postman](https://www.postman.com/) | 11.83.0 |
| [Node.js](https://nodejs.org/en) | 24.11.1 |
| [Newman](https://learning.postman.com/docs/collections/using-newman-cli/installing-running-newman) | 6.2.1 |
## Running with Newman
> [!Note]
> All commands are ran within the `postman_restful-booker` folder/directory.

To run api tests using the testing data provided in bookingData.csv file. By default, the test will run for each row of data that exist:
```
newman run Restful-Booker.json -d bookingData.csv
```
To run api tests for x rows of test data (in this example, 2 rows) from the provided bookingData.csv file. If the number of requested runs exceeds the number of rows in the test data file, the last row will be reused for the additional test runs:
```
newman run Restful-Booker.json -d bookingData.csv -n 2
```
