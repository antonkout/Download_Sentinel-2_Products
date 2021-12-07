# Download-Sentinel-2
This jupyter notebook is for downloading Sentinel-2 imagery from the Google's Cloud Storage interpreting BigQuerry Service. This script need a google cloud service key, which is generated following the instructions below. 

### Required Python Libraries
------------------------------------------------

```
google-cloud-bigquery == 2.31.0
google-auth == 2.3.3
pandas == 1.3.4
```
### Creating a service account at Cloud Storage
#### Step 1.1: Define the service account details
1. Navigate to the IAM Service Accounts page in the GCP console.
2. Select the project you want to use by using the project dropdown menu, located near the top left corner of the page.
3. Click <b>+ Create Service Account</b>. 
4. On the Service account details page, fill in the field as follows:
    - <b>Service account name</b>: `Enter a name for the service account.` 
    - <b>Service account description</b>: `Enter a description for the service account.`
5. Click <b>Create</b>.

#### Step 1.2: Assign BigQuery Admin permissions
Next, you’ll assign the BigQuery Admin role to the service account. This is required to successfully load data into Google BigQuery.
1. On the Service account permissions page, click the <b>Role</b> field.
2. In the window that displays, type `bigquery` into the filter/search field.
3. Select <b>BigQuery Admin</b>.
4. Click <b>Continue</b>.

#### Step 1.3: Create a JSON project key
The last step is to create and download a JSON project key. The project key file contains information about the project.
1. On the <b>Grant users access to this service account</b> page, scroll to the <b>Create key</b> section.
2. Click <b>+ Create Key</b>.
3. When prompted, select the <b>JSON</b> option.
4. Click <b>Create</b>
5. Save the JSON project key file to your computer. The file will be downloaded to the location you specify (if prompted), or the default download location defined for the web browser you’re currently using.
