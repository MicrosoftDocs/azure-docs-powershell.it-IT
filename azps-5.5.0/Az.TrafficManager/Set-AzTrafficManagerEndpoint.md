---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182567"
---
# Set-AzTrafficManagerEndpoint

## SYNOPSIS
Aggiorna un endpoint di Gestione traffico.

## SINTASSI

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzTrafficManagerEndpoint** aggiorna un endpoint in Gestione traffico di Azure.
Questo cmdlet aggiorna le impostazioni da un oggetto endpoint locale.
È possibile specificare l'oggetto endpoint usando il *parametro TrafficManagerEndpoint* o la pipeline.

È possibile ottenere un oggetto locale che rappresenta un endpoint usando il cmdlet Get-AzTrafficManagerEndpoint.
Modificare l'oggetto in locale e quindi usare **Set-AzTrafficManagerEndpoint** per eseguire il commit delle modifiche.

## ESEMPI

### Esempio 1: Aggiornare un endpoint
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Il primo comando ottiene un endpoint di Gestione traffico di Azure usando il cmdlet **Get-AzTrafficManagerEndpoint.**
Il comando archivia l'endpoint in locale nella $TrafficManagerEndpoint variabile.

Il secondo comando modifica l'endpoint in locale.
Questo comando modifica il peso del punto finale in 20.

Il terzo comando aggiorna l'endpoint in Gestione traffico in modo che corrisponda al valore locale in $TrafficManagerEndpoint.

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

### -TrafficManagerEndpoint
Specifica un oggetto **TrafficManagerEndpoint** locale.
Questo cmdlet aggiorna Gestione traffico in modo che corrisponda all'oggetto locale.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## OUTPUT

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## NOTE

## COLLEGAMENTI CORRELATI
