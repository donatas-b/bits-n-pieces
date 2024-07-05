GET - retrieve something
DELETE - delete something
POST - Save this
PUT - I made a change, save that again

An API is essentially a contract between the client and the server or between two applications:
 - endpoints are correctly named
 - resources and their types correctly reflect the object model
 - there is no missing or duplicate functionality
 - relationships between resources are reflected in the API  correctly. 

## API test actions 

For each API request, the test would need to take the following actions: 

1. Verify correct HTTP status code.
2. Verify response payload.
3. Verify response headers.
4. Verify correct application state.
5. Verify basic performance sanity.

## Test scenario categories

1. Basic positive tests (happy paths) - execute API call with valid required parameters
2. Extended positive testing with optional parameters - execute API call with valid required parameters AND valid optional parameters
3. Negative testing with valid input - execute API calls with valid input that attempts illegal operations (e.g. not existing resource)
4. Negative testing with invalid input - execute API calls with invalid input (missing required parameters, invalid values)
5. Destructive testing - intentionally attempt to fail the API to check its robustness (Malformed content in request, Wrong content-type in payload)
6. Security, authorization, and permission tests

## Test flows
1. Testing requests in isolation – Executing a single API request and checking the response accordingly.
2. Multi-step workflow with several requests – Testing a series of requests which are common user actions, since some requests can rely on other ones.
3. Combined API and web UI tests – This is mostly relevant to manual testing, where we want to ensure data integrity and consistency between the UI and API.