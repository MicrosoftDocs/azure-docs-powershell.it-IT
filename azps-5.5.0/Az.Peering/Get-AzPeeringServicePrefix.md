---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: fef6f1615bb2e3dd9d3bb19738ea6cef393235aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202286"
---
# Get-AzPeeringServicePrefix

## SYNOPSIS
Ottiene un elenco di prefissi del servizio di peering per una sottoscrizione.

## SINTASSI

### ByResourceGroupAndName (impostazione predefinita)
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceId
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Elencare i prefissi del servizio di peering per gli oggetti del servizio di peering

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

Ottiene i prefissi per un servizio di peering in base ai comandi di piping.

### Esempio 2
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

Ottiene un prefisso specifico per un servizio di peering in base all'ID risorsa.

### Esempio 3
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

Ottiene un prefisso specifico per un servizio di peering in base all'ID risorsa.

### Esempio 4
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

Ottiene un prefisso specifico per un servizio di peering con attributi espansi

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expand
Visualizzare gli eventi per un prefisso di un servizio di peering

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome univoco di PSCollectioning.

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeeringServiceName
Nome del servizio di peering. Usare New-AzPeeringService cmdlet per un nuovo servizio di peering o un Get-AzPeeringService per un elenco.

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeeringServiceObject
Usare un Get-AzPeeringService

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Creare o usare il nome di un gruppo di risorse esistente.

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Il nome stringa dell'ID risorsa.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioningService

### System.String

## OUTPUT

### Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPreingServicePrefix

## NOTE

## COLLEGAMENTI CORRELATI
