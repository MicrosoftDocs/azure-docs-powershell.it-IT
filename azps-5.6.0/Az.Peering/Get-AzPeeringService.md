---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 4ce8e54b2ee5f43b9196263af5285af826aa9d01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989490"
---
# Get-AzPeeringService

## SYNOPSIS
Ottenere un elenco di oggetti servizio di peering di un singolo oggetto.

## SINTASSI

### ByResourceGroupName (Impostazione predefinita)
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByResourceGroupAndName
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByResourceId
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Recupera i servizi di peering per un abbonamento

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

Ottiene un servizio di peering per un gruppo di risorse

### Esempio 2
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

Ottiene un servizio di peering per un gruppo di risorse e il nome

### Esempio 3
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

Ottiene un servizio di peering in base all'ID risorsa

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

### -Name
Nome univoco di PSCollectioning.

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Creare o usare il nome di un gruppo di risorse esistente.

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### System.String

## OUTPUT

### Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioningService

## NOTE

## COLLEGAMENTI CORRELATI
