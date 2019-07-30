---
external help file:
Module Name: Az.WebSite
online version: https://docs.microsoft.com/en-us/powershell/module/az.website/new-azwebappswiftvirtualnetworkconnectionslot
schema: 2.0.0
---

# New-AzWebAppSwiftVirtualNetworkConnectionSlot

## SYNOPSIS
Integrates this Web App with a Virtual Network.
This requires that 1) \"swiftSupported\" is true when doing a GET against this resource, and 2) that the target Subnet has already been delegated, and is not\nin use by another App Service Plan other than the one this App is in.

## SYNTAX

### Create (Default)
```
New-AzWebAppSwiftVirtualNetworkConnectionSlot -Name <String> -ResourceGroupName <String> -Slot <String>
 -SubscriptionId <String> [-ConnectionEnvelope <ISwiftVirtualNetwork>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### CreateExpanded
```
New-AzWebAppSwiftVirtualNetworkConnectionSlot -Name <String> -ResourceGroupName <String> -Slot <String>
 -SubscriptionId <String> [-Kind <String>] [-SubnetResourceId <String>] [-SwiftSupported]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CreateViaIdentityExpanded
```
New-AzWebAppSwiftVirtualNetworkConnectionSlot -InputObject <IWebSiteIdentity> [-Kind <String>]
 [-SubnetResourceId <String>] [-SwiftSupported] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### CreateViaIdentity
```
New-AzWebAppSwiftVirtualNetworkConnectionSlot -InputObject <IWebSiteIdentity>
 [-ConnectionEnvelope <ISwiftVirtualNetwork>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
Integrates this Web App with a Virtual Network.
This requires that 1) \"swiftSupported\" is true when doing a GET against this resource, and 2) that the target Subnet has already been delegated, and is not\nin use by another App Service Plan other than the one this App is in.

## EXAMPLES

### Example 1: {{ Add title here }}
```powershell
PS C:\> {{ Add code here }}

{{ Add output here }}
```

{{ Add description here }}

### Example 2: {{ Add title here }}
```powershell
PS C:\> {{ Add code here }}

{{ Add output here }}
```

{{ Add description here }}

## PARAMETERS

### -ConnectionEnvelope
Swift Virtual Network Contract.
This is used to enable the new Swift way of doing virtual network integration.
To construct, see NOTES section for CONNECTIONENVELOPE properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WebSite.Models.Api20180201.ISwiftVirtualNetwork
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
Dynamic: False
```

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
Dynamic: False
```

### -InputObject
Identity Parameter

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WebSite.Models.IWebSiteIdentity
Parameter Sets: CreateViaIdentityExpanded, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
Dynamic: False
```

### -Kind
Kind of resource.

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
Dynamic: False
```

### -Name
Name of the app.

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
Dynamic: False
```

### -ResourceGroupName
Name of the resource group to which the resource belongs.

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
Dynamic: False
```

### -Slot
Name of the deployment slot.
If a slot is not specified, the API will add or update connections for the production slot.

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
Dynamic: False
```

### -SubnetResourceId
The Virtual Network subnet's resource ID.
This is the subnet that this Web App will join.
This subnet must have a delegation to Microsoft.Web/serverFarms defined first.

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
Dynamic: False
```

### -SubscriptionId
Your Azure subscription ID.
This is a GUID-formatted string (e.g.
00000000-0000-0000-0000-000000000000).

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
Dynamic: False
```

### -SwiftSupported
A flag that specifies if the scale unit this Web App is on supports Swift integration.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
Dynamic: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
Dynamic: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
Dynamic: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.WebSite.Models.IWebSiteIdentity

### Microsoft.Azure.PowerShell.Cmdlets.WebSite.Models.Api20180201.ISwiftVirtualNetwork

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.WebSite.Models.Api20180201.ISwiftVirtualNetwork

## ALIASES

## NOTES

### COMPLEX PARAMETER PROPERTIES
To create the parameters described below, construct a hash table containing the appropriate properties. For information on hash tables, run Get-Help about_Hash_Tables.

#### CONNECTIONENVELOPE <ISwiftVirtualNetwork>: Swift Virtual Network Contract. This is used to enable the new Swift way of doing virtual network integration.
  - `[Kind <String>]`: Kind of resource.
  - `[SubnetResourceId <String>]`: The Virtual Network subnet's resource ID. This is the subnet that this Web App will join. This subnet must have a delegation to Microsoft.Web/serverFarms defined first.
  - `[SwiftSupported <Boolean?>]`: A flag that specifies if the scale unit this Web App is on supports Swift integration.

## RELATED LINKS
