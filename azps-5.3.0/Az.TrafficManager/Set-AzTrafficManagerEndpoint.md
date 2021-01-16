---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382756"
---
# Set-AzTrafficManagerEndpoint

## Sinossi
Aggiorna un endpoint di gestione traffico.

## SINTASSI

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzTrafficManagerEndpoint** aggiorna un endpoint in Azure Traffic Manager.
Questo cmdlet aggiorna le impostazioni da un oggetto endpoint locale.
Puoi specificare l'oggetto endpoint usando il parametro *TrafficManagerEndpoint* o usando la pipeline.

Puoi ottenere un oggetto local che rappresenta un endpoint usando il cmdlet Get-AzTrafficManagerEndpoint.
Modificare l'oggetto localmente e quindi usare **set-AzTrafficManagerEndpoint** per eseguire il commit delle modifiche.

## ESEMPI

### Esempio 1: aggiornare un endpoint
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Il primo comando ottiene un endpoint di Azure Traffic Manager usando il cmdlet **Get-AzTrafficManagerEndpoint** .
Il comando Archivia l'endpoint localmente nella variabile $TrafficManagerEndpoint.

Il secondo comando cambia l'endpoint localmente.
Questo comando imposta il peso dell'endpoint su 20.

Il terzo comando Aggiorna l'endpoint in gestione traffico per corrispondere al valore locale in $TrafficManagerEndpoint.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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
Questo cmdlet aggiorna Traffic Manager in base a questo oggetto locale.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint

## OUTPUT

### Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint

## Note

## COLLEGAMENTI CORRELATI
