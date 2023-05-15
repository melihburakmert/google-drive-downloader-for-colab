# Google Drive Downloader For Google Colab

This notebook allows you to download a revision of a file from Google Drive to your Google Colab workspace.

Normally, when you mount your drive into your runner, file revisions are not visible on the list, therefore you cannot copy the file to your workspace directly.

You can access the revision by using downloadLink through Drive console, however, to download directly into your workspace via HTTP,  you need to be authenticated.

Also you will be out-of-memory if you try to download the files larger than your runner's memory.

The notebook allows you to see your files and revisions, goes through required authentication steps and downloads the file in chunks.

## Prerequistes

Have a look at the [references](##References) first.

1. Create a project under Google Cloud Console https://console.cloud.google.com/
2. Create OAuth client ID in https://console.cloud.google.com/apis/credentials
- Create consent screen if you don't have yet https://console.cloud.google.com/apis/credentials/consent
- Add your user email under test users
- On create client id page:
 - Application type: Web application
 - Authorised redirect URIs: http://localhost:8081/
3. Download client secrets json, upload to your workspace.

## References

- https://support.google.com/cloud/answer/6158849?hl=en
- https://developers.google.com/identity/protocols/oauth2