# Migrations API
Migrations API allows end-users to setup a migration of a database from Daylite Self-Serve to Daylite Cloud. This API will ensure that it is currently possible to perform a migration (there are a limited number of slots available at any given time), validate the table properties of the database being migrated to ensure that they are within the limits being accepted by Cloud, and confirm that the primary user's email address isn't in use. If successful, an upload URL will be generated where the backup can be uploaded to. If the uploaded size matches the expected size from the source computer, the migration will then be passed onto a migration worker machine to complete the transition to Cloud.

#Endpoints
---
POST /migrations
