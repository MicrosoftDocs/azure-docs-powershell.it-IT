---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: a8326afbeb6d71d54ec861eb3ec65868e7e230bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956990"
---
# Get-AzExpressRoutePortLinkConfig

## SYNOPSIS
Ottiene una configurazione del collegamento ExpressRoutePort.

## SINTASSI

### ResourceNameParameterSet (impostazione predefinita)
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzExpressRoutePortLinkConfig** recupera la configurazione di un collegamento di expressRoutePort.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

Recupera la configurazione Link1 di ExpressRoutePort $erport

### Esempio 2
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

Ottiene la configurazione del collegamento con resourceId $id in ExpressRoutePort $erport

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

### -ExpressRoutePort
Riferimento della risorsa ExpressRoutePort.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name
Nome del collegamento.

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ResourceId del collegamento.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

### Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink

## NOTE

## COLLEGAMENTI CORRELATI
