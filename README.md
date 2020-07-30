# Express.Licensing

Express.Licensing allows limiting application capabilities through a licencing mechanism

### Versions

Released verisons are listed below

| Version | Change log |
| ------ | ------ |
| 1.1 | FFin.Ecnription 1.1, Microsoft.AES 1.1 |



### Usage
Check if product is licensed
```csharp
var productUID = _configuration.GetSection("Licensing:Keys")
var el = new ExpressLicense(productUID);
var isLicened = el.IsProductLicensed();
```
Get all licensing information
```csharp
var isLicened = el.GetLicenseInfo();
```
Renders license information in a human readable paragraph string
```csharp
var isLicened = el.GetViewText();
```
Installs + Opens license file
```csharp
el.OpenLicense();
```
Download license file (Returns a memory stream - For ASP.NET)
```csharp
el.DownloadLicense();
```
Download license viewer  (Returns a memory stream - For ASP.NET)
```csharp
el.DownloadLicenseViewer();
```
