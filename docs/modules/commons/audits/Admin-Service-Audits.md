The admin portal provides various services for MOSIP administrators such as Login, Account management, Resource Management, Master data management and Packet status check based on RID.

# Packet Status Service
The packet status service allows us to view the status of a packet by giving the RID of the packet. The packet status will contain all the stages the packet has passed through along with the last stage the packet is in. In case the packet has not been processed or is marked for Re-Send/Re-Register, the admin will be able to view specific comments indicating the reason for that particular status.

## User Events
The following events are triggered as part of User Event Type in Packet Status Service module of Admin Services

### Failure response for User Event Type

Event ID | Event Type | Event Name | Description | Reference ID Type
-------- | ---------- | ---------- | ----------- | -----------------
ADM-PKT_405 | User | Authorization request | This event specifies that the specified user name is not authorized | No ID 
ADM-PKT-406 | User | Check RID validation | This event specifies that the specified registration ID is invalid | No ID 
ADM-PKT-407 | User | Check whether center exists or not | This event specifies that the center id extracted from registration id does not exist | No ID 
ADM-PKT-408 | User | Check whether RID exists or not | This event specifies that the registration ID is missing in the input | No ID 

## System Events
The following events are triggered as part of System Event Type in Packet Status Service module of Admin Services

**Request Info for System Event Type**

Event ID | Event Type | Event Name | Description | Reference ID Type
-------- | ---------- | ---------- | ----------- | -----------------
ADM-PKT_102 | System | Request for packet status update API | This event calls the API to update the packet status for RID | RID
ADM-PKT-103 | System | Check authorization RID with zone | This event triggers the authorization of registration ID with the zone | RID
ADM-PKT-104 | System | Request to get packet status | This event calls the API to get the packet status for Registration ID | RID
ADM-PKT-105 | System | Request to get packet status | This event specifies that the packet with registration id has reached Packet Receiver	| RID
ADM-PKT-106 | System | Request to get packet status | This event specifies that the packet with registration id is uploaded to the landing zone | RID
ADM-PKT-107 | System | Request to get packet status | This event specifies that the packet with registration id is uploaded to the Packet Store | RID
ADM-PKT-108 | System | Request to get packet status | This event specifies that the PDF for registration id is added to queue for printing | RID
ADM-PKT-109 | System | Request to get packet status	| This event specifies that the printing and post completed for the registration ID | RID

**Success response for System Event Type**

Event ID | Event Type | Event Name | Description | Reference ID Type
-------- | ---------- | ---------- | ----------- | -----------------
ADM-PKT-200 | System | Request for packet status update API | This event describes that the API call to packet status update for RID is successful | RID
ADM-PKT-201 | System | Check authorization RID with zone | This event specifies that the authorization of Registration ID with the zone is successful | RID

**Failure response for System Event Type**

Event ID | Event Type | Event Name | Description | Reference ID Type
-------- | ---------- | ---------- | ----------- | -----------------
ADM-PKT-404 | System | Check authorization RID with zone | This event specifies that the authorization of registration ID with the zone is failed | RID
ADM-PKT-410 | System | Check authentication | This event specifies that the authentication failed for auth manager | No ID
ADM-PKT-405 | System | Check access | This event specifies that the access is denied from auth manager | No ID
ADM-PKT-401 | System | Check authentication | This event specifies that the user tried to operate on a protected resource without providing the proper authorization | No ID
ADM-PKT-403 | System | Check authentication | This event specifies that the user does not have the necessary permissions for the resource | No ID
ADM-PKT-405 | System | Authorization request | This event specifies that the User <user_name> is not authorized | No ID
ADM-PKT-406 | System | Check RID validation | This event specifies that the Registration ID is invalid | No ID
ADM-PKT-407 | System | Check whether centre exists or not | This event specifies that the centre id extracted from registration ID does not exist | No ID
ADM-PKT-408 | System | Check RID exists | This event specifies that the Registration id is missing in the input | No ID
ADM-PKT-409 | System | Request to get packet status | This event specifies that the System error has occurred while fetching packet status for registration id RID | RID
ADM-PKT-402 | System | Request to get packet response API | This event specifies that the JSON parse exception occurred while parsing packet response | No ID

# Bulk Data Service
The bulk data service provides a feature for the mosip administrator to bulk insert, upload or delete - master data using csv’s. The bulk data upload operation can be performed based on various parameters.

## System Events
The following events are triggered as part of System Event Type in Bulk Data Service module of Admin Services

### Request Info for System Event Type

Event ID | Event Type | Event Name | Description | Reference ID Type
----------|------------|------------|-------------|------------------
ADM-BLK-101 | System | Request for bulk data upload API | This event calls the API to bulk upload data | No ID
ADM-BLK-102 | System | Request for bulk data upload operation | This event requests the bulk data upload based on category name | No ID
ADM-BLK-103 | System | Request for bulk data upload operation | This event requests bulk data upload based on operation and file_name | No ID
ADM-BLK-104 | System | Request for bulk data upload operation | This event requests the bulk data upload based on category category_name | No ID
ADM-BLK-105 | System | Request for bulk data upload operation | This event specifies that the bulk data upload job started with job id - job Id  | No ID
ADM-BLK-106 | System | Request for bulk data insert operation based on category | This event returns the status of bulk data insert operation file_name,operation,jobId and message | No ID
ADM-BLK-107 | System | Request for bulk data upload transaction | This event specifies the inserting of data into transaction table based on (operation,category,entity_name) | No ID
ADM-BLK-108 | System | Request for bulk data upload transaction | This event specifies that the data is successfully inserted into transaction table with transaction id | Transaction id
ADM-BLK-109 | System | Request for bulk data insert operation based on category | This event returns the status of the uploading packet packetId,message | No ID
ADM-BLK-110 | System | Request to get transaction details based on transaction id | This event fetches the transaction details for transaction id | Transaction Id
ADM-BLK-111 | System | Request to get all the transaction details | This event fetches the transaction details for all the transactions | No ID
ADM-BLK-112 | System | Request for bulk data upload operation | This event requests for bulk data packet upload of file_name file | No ID

### Success response for System Event Type

Event ID | Event Type | Event Name | Description | Reference ID Type
-------- | ---------- | ---------- | ----------- | -----------------
ADM-BLK-200 | System | Request for bulk data upload API | This event specifies that the bulk data upload is successful | No ID
ADM-BLK-201 | System | Request to get transaction details based on transaction id | This event specifies that the request to fetch the transaction details for transaction id is successful | No ID
ADM-BLK-202 | System | Request to get all the transaction details | This event specifies that the request to fetch the transaction details for all the transactions is successful | No ID

### Failure response for System Event Type

Event ID | Event Type | Event Name | Description | Reference ID Type
-------- | ---------- | ---------- | ----------- | -----------------
ADM-BLK-401 | System | Request for bulk data upload operation | This event specifies that the bulk data upload failed – and returns file_name,operation,jobId and errormessage | No ID
ADM-BLK-402 | System | Request for bulk data operation | This event specifies that an error occurred while operating bulk data for file_name,operation and error message | No ID
ADM-BLK-403 | System | Validating CSV file request | This event specifies that the file name is not a CSV file  | No ID
ADM-BLK-404 | System | Validating CSV file request | This event returns a validation message stating that it’s a invalid CSV file  | No ID
ADM-BLK-405 | System | Validating CSV file request | This event specifies that all the rows have same number of element in CSV file | No ID
ADM-BLK-406 | System | Request for bulk data insert operation based on category | This event returns a validation message stating that it’s a 
invalid category  | No ID
ADM-BLK-407 | System | Request for bulk data upload packets | This event specifies that the upload of packets failed for (packetId, message) | No ID
ADM-BLK-408 | System | Request to get transaction details based on transaction id | This event specifies that it was unable to retrieve transaction details for transaction id | No ID
ADM-BLK-409 | System | Request to get all the transaction details | This event specifies that it was unable to retrieve transaction details for all transactions | No ID
ADM-BLK-410 | System | Request for bulk data insert operation | This event returns a validation message stating that it’s a invalid argument | No ID
