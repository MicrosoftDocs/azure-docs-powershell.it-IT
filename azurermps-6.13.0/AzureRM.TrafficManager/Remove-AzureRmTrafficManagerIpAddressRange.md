---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 5bb661dbc5a65b9a245fcfa35cdc194bbcded1eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508956"
---
# Remove-AzureRmTrafficManagerIpAddressRange

## Sinossi
Rimuove un intervallo di indirizzi o una subnet da un oggetto endpoint di gestione traffico locale.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Remove-AzureRmTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureRmTrafficManagerIpAddressRange** rimuove un intervallo di indirizzi IP da un oggetto endpoint di Azure Traffic Manager locale.
Puoi ottenere un endpoint usando i cmdlet New-AzureRmTrafficManagerEndpoint o Get-AzureRmTrafficManagerEndpoint.

Questo cmdlet funziona sull'oggetto endpoint locale.
Eseguire il commit delle modifiche apportate all'endpoint per Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerEndpoint.

## ESEMPI

### Esempio 1: rimuovere gli intervalli di indirizzi IP da un endpoint
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Il primo comando ottiene l'endpoint Azure denominato Contoso dal profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $TrafficManagerEndpoint.
Il secondo comando rimuove un intervallo di indirizzi IP dall'endpoint archiviato in $TrafficManagerEndpoint.
Il comando finale aggiorna l'endpoint in gestione traffico per corrispondere al valore locale in $TrafficManagerEndpoint.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
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
Questo cmdlet modifica questo oggetto locale.
Per ottenere un oggetto **TrafficManagerEndpoint** , usa il cmdlet Get-AzureRmTrafficManagerEndpoint o New-AzureRmTrafficManagerEndpoint.

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Primo
Specifica il primo indirizzo IP nell'intervallo da rimuovere.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Questo cmdlet accetta un oggetto **TrafficManagerEndpoint** per questo cmdlet.

## OUTPUT

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Questo cmdlet restituisce un oggetto TrafficManagerEndpoint modificato.

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureRmTrafficManagerIpAddressRange](./Add-AzureRmTrafficManagerIpAddressRange.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerEndpoint.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)
