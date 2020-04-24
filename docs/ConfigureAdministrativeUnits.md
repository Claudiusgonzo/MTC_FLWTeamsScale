# Configure Administrative Units

## Steps

1. Update the Teams CSV file [TeamsInformation](../data/teamsInformation.csv) with the Azure AD Administrative Units (AU) that will be created and the UPNs of each administrator for the AU
2. Update the Users CSV file [Users](../data/users.csv) with the Azure AD Administrative Units (AU) members
3. From a PowerShell session, run the script [ConfigureAdministrativeUnits](../scripts/ConfigureAdministrativeUnits.ps1)

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact opencode@microsoft.com with any additional questions or comments.