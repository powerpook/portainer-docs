# Authenticate via OAuth

## Configuring OAuth authentication in Portainer

From the menu select **Settings** then select **Authentication**. Under the **Authentication method** section click **OAuth**.

![](../../../.gitbook/assets/authentication-oauth-1.gif)

In the next screen, enter the credentials provided by your OAuth provider, using the table below as a guide.

| Field/Option | Overview |
| :--- | :--- |
| Use SSO | Enable SSO so that the OAuth provider won't be forced to ask for credentials when users are in a current logged-in session. |
| Hide internal authentication prompt | Hide the ability to log in through internal authentication. This feature is only available in Portainer Business Edition. |
| Automatic user provisioning | If toggled on, users who exist at the OAuth provider's end will automatically be created in Portainer \(you can define a default team to put those users in while this option is on\). If toggled off, you'll need to [create users](../../users/add.md) in Portainer manually. |

![](../../../.gitbook/assets/authentication-oauth-2.png)

| Field/Option | Overview |
| :--- | :--- |
| Client ID | Enter the public identifier of the OAuth application. |
| Client secret | Enter the token access to the OAuth application. |
| Authorization URL | Enter the URL used to authenticate against the OAuth provider \(will redirect users to the OAuth provider login screen\). |
| Access token URL | Enter the URL used to exchange a valid OAuth authentication code for an access token. |
| Resource URL | Enter the URL used by Portainer to retrieve information about authenticated users. |
| Redirect URL | Enter the URL used by the OAuth provider to redirect users after they are successfully authenticated. You should set this to your Portainer instance URL. |
| Logout URL | Enter the URL used by the OAuth provider to log users out. |
| User identifier | Enter the identifier that Portainer will use to create accounts for authenticated users. Retrieved from the resource server specified in the **Resource URL** field. |
| Scopes | Required by the OAuth provider to retrieve information about authenticated users. See your provider's own documentation for more information. |

![](../../../.gitbook/assets/authentication-oauth-3.png)

When you're finished, click **Save settings**.

## Giving endpoint access to OAuth teams and users

See [Managing user access to endpoints](../../endpoints/access.md).

## Examples

These examples show OAuth configuration for Azure, Google, GitHub and Keycloak.

* The client ID is known as 'application ID' in the MSFT world.
* The tenant ID \(grayed information in the screenshot\), is a GUID specific to your ID.

### Azure

![](../../../.gitbook/assets/authentication-oauth-azure.png)

### Google

![](../../../.gitbook/assets/authentication-oauth-3.png)

### GitHub

![](../../../.gitbook/assets/authentication-oauth-github.png)

### Keycloak

![](../../../.gitbook/assets/authentication-oauth-keycloak.png)
