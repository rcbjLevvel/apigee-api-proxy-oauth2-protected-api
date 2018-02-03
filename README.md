# An Apigee API Proxy that wraps Red Hat SSO with the out-of-the-box OAuth2 implementation
This API Proxy demonstrates wrapping a third-party OAuth2/OIDC compliant Identity Provider (IdP) with Apigee's OAuth2 implementation.

These instructions assume a working knowledge of Apigee Edge Public Cloud.

You can setup a free Apigee Edge Public Cloud account [here](https://enterprise.apigee.com).  There are various restrictions put in place on these types of accounts.  But, this API Proxy should be capable of working with those restrictions.

The quickest way to try out this project is to grab the API Proxy in [zip form](https://github.com/rcbjLevvel/apigee-api-proxy-oauth2-rh-sso-wrapper/blob/master/blog-rh-sso-integration.zip) and deploy it to your own Apigee Edge Public Cloud organization.

### Prerequisites
To run this project you will need
* *An Apigee Edge account*
* *Working knowledge of Apigee Edge*
* *Access to an OIDC-compliant third-party IdP.

### Installing
1. Clone this repository to a local file system.
2. Install the apigeetool by running "npm -g install apigeetool".  If npm (Node Package Manager) is not already installed, then this will also need to be installed.
3. Deploy the API Proxy by running:
  ```
apigeetool deployproxy  -u admin_user_for_org -p admin_password -o apigee_org  -e env_name -n blog-rh-sso-integration -d ${REPOSITORY_HOME}/proxy
  ```
4. Log into the Apigee Edge Public Cloud console [here](https://enterprise.apigee.com).
## Authors
* **Robert C. Broeckelmann Jr.** - *Initial work*

## License
This project is licensed under the Apache 2.0 License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments
