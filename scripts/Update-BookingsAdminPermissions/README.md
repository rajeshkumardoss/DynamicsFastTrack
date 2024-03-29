# Microsoft FastTrack Open Source - Update-BookingsAdminPermissions

This script is used to search for all Bookings mailboxes and add/remove Administrators to them. Then you can export a list of mailbox permissions to a CSV file. 

## Usage

You'll need to install the Exchange Online module to use this PowerShell script. 

```PowerShell
Install-Module ExchangeOnline
```

## Examples

Report on all Bookings's mailboxes's permissions.

```PowerShell
.\Update-BookingsAdminPermissions.ps1 -ExportCSVFilePath "C:\path\to\export.csv"
```
    
Add users "User1@Contoso.com" and "User2@Contoso.com" to all Bookings's mailboxes's permissions and then Export a CSV of all Bookings's Mailboxes's permissions.

```PowerShell
.\Update-BookingsAdminPermissions.ps1 -AddUser "User1@Contoso.com","User2@Contoso.com" -ExportCSVFilePath C:\path\to\export.csv
```
    
Remove users "User3@Contoso.com" and "User4@Contoso.com" from all Bookings's mailboxes's permissions and then Export a CSV of all Bookings's Mailboxes's permissions.

```PowerShell
.\Update-BookingsAdminPermissions.ps1 -RemoveUser "User3@Contoso.com","User4@Contoso.com" -ExportCSVFilePath C:\path\to\export.csv
```
    
Add users "User1@Contoso.com" and "User2@Contoso.com" to all Bookings's mailboxes's permissions, Remove users "User3@Contoso.com" and "User4@Contoso.com" from all Bookings's mailboxes's permissions, and then Export a CSV of all Bookings's Mailboxes's permissions.

```PowerShell
.\Update-BookingsAdminPermissions.ps1 -AddUser "User1@Contoso.com","User2@Contoso.com" -RemoveUser "User3@Contoso.com","User4@Contoso.com" -ExportCSVFilePath C:\path\to\export.csv
```

### Output columns

- Identity
- User
- AccessRights
- ObjectState

## Applies To

- Exchange Online
- Bookings

## Author

|Author|Original Publish Date
|----|--------------------------
|Nick Bear|04-01-2022|
|David Whitney|04-01-2022|

## Issues

Please report any issues you find to the [issues list](https://github.com/microsoft/FastTrack/issues).

## Support Statement

The scripts, samples, and tools made available through the FastTrack Open Source initiative are provided as-is. These resources are developed in partnership with the community and do not represent official Microsoft software. As such, support is not available through premier or other Microsoft support channels. If you find an issue or have questions please reach out through the issues list and we'll do our best to assist, however there is no associated SLA.

## Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Legal Notices

Microsoft and any contributors grant you a license to the Microsoft documentation and other content in this repository under the [MIT License](https://opensource.org/licenses/MIT), see the [LICENSE](LICENSE) file, and grant you a license to any code in the repository under the [MIT License](https://opensource.org/licenses/MIT), see the [LICENSE-CODE](LICENSE-CODE) file.

Microsoft, Windows, Microsoft Azure and/or other Microsoft products and services referenced in the documentation may be either trademarks or registered trademarks of Microsoft in the United States and/or other countries. The licenses for this project do not grant you rights to use any Microsoft names, logos, or trademarks. Microsoft's general trademark guidelines can be found at http://go.microsoft.com/fwlink/?LinkID=254653.

Privacy information can be found at https://privacy.microsoft.com/en-us/

Microsoft and any contributors reserve all others rights, whether under their respective copyrights, patents,
or trademarks, whether by implication, estoppel or otherwise.
