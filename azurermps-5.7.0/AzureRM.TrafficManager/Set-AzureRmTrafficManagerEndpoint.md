---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 99f621824d10b574c7f64fb7653bc4154ba6766e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685968"
---
# Set-AzureRmTrafficManagerEndpoint

## Sinossi
Aggiorna un endpoint di gestione traffico.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmTrafficManagerEndpoint** aggiorna un endpoint in Azure Traffic Manager.
Questo cmdlet aggiorna le impostazioni da un oggetto endpoint locale.
Puoi specificare l'oggetto endpoint usando il parametro *TrafficManagerEndpoint* o usando la pipeline.

Puoi ottenere un oggetto local che rappresenta un endpoint usando il cmdlet Get-AzureRmTrafficManagerEndpoint.
Modificare l'oggetto localmente e quindi usare **set-AzureRmTrafficManagerEndpoint** per eseguire il commit delle modifiche.

## ESEMPI

### Esempio 1: aggiornare un endpoint
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Il primo comando ottiene un endpoint di Azure Traffic Manager usando il cmdlet **Get-AzureRmTrafficManagerEndpoint** .
Il comando Archivia l'endpoint localmente nella variabile $TrafficManagerEndpoint.

Il secondo comando cambia l'endpoint localmente.
Questo comando imposta il peso dell'endpoint su 20.

Il terzo comando Aggiorna l'endpoint in gestione traffico per corrispondere al valore locale in $TrafficManagerEndpoint.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Type: TrafficManagerEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Questo cmdlet accetta un oggetto **TrafficManagerEndpoint** .

## OUTPUT

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Questo cmdlet restituisce un oggetto **TrafficManagerEndpoint** .

## Note

## COLLEGAMENTI CORRELATI

