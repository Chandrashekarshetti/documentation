# Data sync

# Registration Client Services

## Retrieve a list of PRIDs for a given date range

Upon receiving the registration center id, date range (start date, end date) for the List of pre-registrations, user id (registration officer/supervisor) from the registration client, the pre-registration system processes the information.
* The system then fetches all the pre-registrations within the date range (start date, end date) and for the registration center id received, and calculates the count of the pre-registration ids being sent
* The system sends the list of pre-registration ids along with a count of pre-registrations

## Retrieve application data by PRID

Upon receiving the list of pre-registrations from the registration client, the pre-registration system processes the information.
* The system receives the pre-registration id/ids for which pre-registration data has to be sent
* The system retrieves the demographic and the documents from the database and object-store respectively
* The system creates an encrypted zip file per pre-registration id consisting of demo data, documents, and appointment time
* The system then sends this encrypted zip file to the requesting registration client

## To Do

## API Details
 * [API Documentation](https://nayakrounak.gitbook.io/mosip-docs/v/1.2.0/modules/registration/pre-registration/Pre-Reg-API-Documentation.md)

* Configuration Parameters
    * List of parameters and how they alter the behaviour of the API

## Links to related content
* Link to design documentation,
* Links to How To articles

