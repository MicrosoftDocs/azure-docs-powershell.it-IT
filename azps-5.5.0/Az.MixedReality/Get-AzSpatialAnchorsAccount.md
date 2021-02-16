---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2497b41399c79297726bc82e3232934cbd6768d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194078"
---
# Get-AzSpatialAnchorsAccount

## SYNOPSIS
Ottenere l'account degli ancoraggi nello spaziale

## SINTASSI

### ListParameterSet (impostazione predefinita)
```
Get-AzSpatialAnchorsAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetParameterSet (Impostazione predefinita)
```
Get-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzSpatialAnchorsAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Ottenere o elencare account di ancoraggi nello stato attivo in determinati gruppi di risorse e di sottoscrizione.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : 2f7443d0-2c2b-4514-9b29-a78072a1556f
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/2f7443d0-2c2b-4514-9b29-a78072a1556f/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/demo
Name                : demo
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : ed3273ce-1eeb-42c7-b3b8-fb9896b9801c
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/ed3273ce-1eeb-42c7-b3b8-fb9896b9801c/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/foobar
Name                : foobar
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

Elencare tutti gli ancoraggi nello stato del gruppo di risorse "rg1". 

### Esempio 2
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mrc-anchor-prod.trafficmanager.net
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

Get Spatial Anchors Account "example" in Resource Group "rg1". 

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome account per gli ancoraggi nello spaziale.

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome gruppo di risorse.

```yaml
Type: String
Parameter Sets: ListParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa dell'account degli ancoraggi nello stato spaziale.

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.
Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount

## NOTE

## COLLEGAMENTI CORRELATI
