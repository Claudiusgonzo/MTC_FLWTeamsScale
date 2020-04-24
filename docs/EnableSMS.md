# Create Teams Message Policies

Enables SMS Sign-in for users

## Prerequisite

The Graph authorization model requires that an application must be consented by a user or administrator prior to accessing an organization’s data.  Creating this app will provide the appropriate read/write permissions for the PowerShell code to update your tenant (with appropriately authorized credentials).

1.	Sign in to portal.azure.com as a global administrator.
2.	Navigate to the Azure AD extension, and click on App registrations in the MANAGE section.
3.	Click on New registration button at the top of the page.
4.  Provide a name for the application that is different from any other application in your tenant’s directory (e.g., “SMS Sign-in API”)
    1.  Leave the supported account type as “Accounts in this organizational directory only”.
    2.  Select Public client for the Redirect URI and enter urn:ietf:wg:oauth:2.0:oob.
5.	Click register.
6.	When the application is registered, copy the Application (client) ID, and save the value for later – we will use it in the script.
6.	Click on Settings, then click on Required permissions.
7.	Click on Add a permission. Click on Microsoft Graph, Delegated Permissions. Select the following permissions:
    1.	Directory.AccessAsUser.All
    2.	Directory.ReadWrite.All
    3.  UserAuthenticationMethod.ReadWrite
    4.  UserAuthenticationMethod.ReadWrite.All
8.	Click on Add a permission. Click on Azure Active Directory Graph, Delegated Permissions and select Directory.ReadWriteAll.  Click add permissions.
9.	At the top of the API Permission page, click Grant admin consent for <your tenant name>, and select yes.


## Steps

1. Update the CSV file [User Information](../data/users.csv) with the Azure AD Administrative Units (AU) that will be created and the UPNs of each administrator for the AU
2. From PowerShell, run the script [EnableSms](../scripts/EnableSms.ps1)

    NOTE
    
    An authentication dialog will open when running the script.

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact opencode@microsoft.com with any additional questions or comments.
