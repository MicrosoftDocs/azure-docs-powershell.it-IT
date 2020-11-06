---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 213e959ecfec178644246f56be11e5b7306ef07f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508991"
---
# Add-AzureRmTrafficManagerIpAddressRange

## Sinossi
Aggiunge un intervallo di indirizzi o una subnet a un oggetto endpoint di gestione traffico locale.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Add-AzureRmTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureRmTrafficManagerIpAddressRange** aggiunge un intervallo di indirizzi IP a un oggetto endpoint di Azure Traffic Manager locale.
Puoi ottenere un endpoint usando i cmdlet New-AzureRmTrafficManagerEndpoint o Get-AzureRmTrafficManagerEndpoint.

Questo cmdlet funziona sull'oggetto endpoint locale.
Eseguire il commit delle modifiche apportate all'endpoint per Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerEndpoint.

## ESEMPI

### Esempio 1: aggiungere intervalli di indirizzi IP a un endpoint
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Con il primo comando viene creato un endpoint di Azure Traffic Manager usando il cmdlet **New-AzureRmTrafficManagerEndpoint** .
Il comando Archivia l'endpoint locale nella variabile $TrafficManagerEndpoint.
Il secondo comando aggiunge l'intervallo di indirizzi IP 1.2.3.4 a 5.6.7.8 all'endpoint archiviato in $TrafficManagerEndpoint.
Il terzo comando aggiunge l'intervallo di indirizzi IP 9.10.11.0 a 9.10.11.255 all'endpoint archiviato in $TrafficManagerEndpoint.
Il quarto comando verifica che l'ambito corrisponda alle dimensioni dell'intervallo, quindi aggiunge l'intervallo di indirizzi IP 12.13.14.0 a 12.13.14.31 all'endpoint archiviato in $TrafficManagerEndpoint.
Il quinto comando aggiunge l'intervallo di indirizzi IP 15.16.17.18 a 15.16.17.18 all'endpoint archiviato in $TrafficManagerEndpoint.
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

### -Last
Specifica l'ultimo indirizzo IP nell'intervallo da aggiungere.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ambito
Specifica l'ambito dell'intervallo di indirizzi IP da aggiungere.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

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
Specifica il primo indirizzo IP nell'intervallo da aggiungere.

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
Questo cmdlet restituisce un oggetto **TrafficManagerEndpoint** modificato.

## Note

## COLLEGAMENTI CORRELATI

[Remove-AzureRmTrafficManagerIpAddressRange](./Remove-AzureRmTrafficManagerIpAddressRange.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)
