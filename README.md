# An Apigee API Proxy that wraps a backend API with Apigee's out-of-the-box OAuth2 implementation
This API Proxy demonstrates the use of Apigee's OAuth2 access token validation policy.  It is meant to be used with the OAuth2 implmentation provided by [this API Proxy project](https://github.com/rcbjLevvel/apigee-api-proxy-oauth2-rh-sso-wrapper).

It sends requests to the [https://jsonplaceholder.typicode.com](https://jsonplaceholder.typicode.com) API.

To protect the access token from the third-party backend, it strips the HTTP Authorization Request header from the request before sending the request to the back end.

These instructions assume a working knowledge of Apigee Edge Public Cloud.

You can setup a free Apigee Edge Public Cloud account [here](https://enterprise.apigee.com).  There are various restrictions put in place on these types of accounts.  But, this API Proxy should be capable of working with those restrictions.

The quickest way to try out this project is to grab the API Proxy in [zip form](https://github.com/rcbjLevvel/apigee-api-proxy-oauth2-protected-api/blob/master/OAuth2Test.zip) and deploy it to your own Apigee Edge Public Cloud organization.

### Prerequisites
To run this project you will need
* *An Apigee Edge account*
* *Working knowledge of Apigee Edge*
* *Access to an OIDC-compliant third-party IdP.

### Installing
1. Install the [OAuth2 Red Hat SSO (OIDC) Wrapper API Proxy](https://github.com/rcbjLevvel/apigee-api-proxy-oauth2-rh-sso-wrapper) per the instructions found [here](https://github.com/rcbjLevvel/apigee-api-proxy-oauth2-rh-sso-wrapper/blob/master/README.md).
2. Install the [OAuth2 + OIDC Debugger](https://github.com/GetLevvel/oauth2-oidc-debugger) per the instrucitons found [here](https://github.com/GetLevvel/oauth2-oidc-debugger/blob/master/README.md).
3. Clone this repository to a local file system.
4. Install the apigeetool by running "npm -g install apigeetool".  If npm (Node Package Manager) is not already installed, then this will also need to be installed.
5. Deploy the API Proxy by running:
  ```
apigeetool deployproxy  -u admin_user_for_org -p admin_password -o apigee_org  -e env_name -n blog-rh-sso-integration -d ${REPOSITORY_HOME}/proxy
  ```
6. Log into the Apigee Edge Public Cloud console [here](https://enterprise.apigee.com).
7. Click on the OAuth2Test Proxy link.
8. Click on the Trace tab.
9. Click the "Start Trace Session" button.
10. Obtain an access token for a test client as described in [this](https://github.com/rcbjLevvel/apigee-api-proxy-oauth2-rh-sso-wrapper) post.
11. 

## Authors
* **Robert C. Broeckelmann Jr.** - *Initial work*

## License
This project is licensed under the Apache 2.0 License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments
