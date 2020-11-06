---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: f2abe6acd0406f78ba2bb691b562cd0bcbffeb35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508515"
---
# Add-AzureRmTrafficManagerEndpointConfig

## Sinossi
Aggiunge un endpoint a un oggetto profilo di gestione traffico locale.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureRmTrafficManagerEndpointConfig** aggiunge un endpoint a un oggetto profilo di Azure Traffic Manager locale.
Puoi ottenere un profilo usando i cmdlet New-AzureRmTrafficManagerProfile o Get-AzureRmTrafficManagerProfile.

Questo cmdlet opera nell'oggetto profilo locale.
Eseguire il commit delle modifiche apportate al profilo per Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerProfile.
Per creare un endpoint e confermare la modifica in una singola operazione, usare il cmdlet New-AzureRmTrafficManagerEndpoint.

## ESEMPI

### Esempio 1: aggiungere un endpoint a un profilo
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet **Get-AzureRmTrafficManagerProfile** .
Il comando Archivia il profilo locale nella variabile $TrafficManagerProfile.

Il secondo comando aggiunge un endpoint denominato Contoso al profilo archiviato in $TrafficManagerProfile.
Il comando include i dati di configurazione per l'endpoint.
Questo comando modifica solo l'oggetto locale.

Il comando finale aggiorna il profilo di Traffic Manager in Azure in base al valore locale in $TrafficManagerProfile.

## PARAMETRI

### -EndpointLocation
Specifica la posizione dell'endpoint da usare nel metodo di routing del traffico delle prestazioni.
Questo parametro è applicabile solo agli endpoint del tipo ExternalEndpoints o NestedEndpoints.
Devi specificare questo parametro quando viene usato il metodo di routing del traffico delle prestazioni.

Specificare un nome di area di Azure.
Per un elenco completo delle aree di Azure, vedere aree di Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

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

### -EndpointName
Specifica il nome dell'endpoint di gestione traffico che questo cmdlet aggiunge.

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

### -EndpointStatus
Specifica lo stato dell'endpoint.
I valori validi sono: 

- Abilitato 
- Disabilitato 

Se lo stato è abilitato, l'endpoint viene esaminato per l'integrità dell'endpoint ed è incluso nel metodo di routing del traffico.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geomapping
L'elenco delle aree geografiche mappate a questo endpoint quando si usa il metodo di routing del traffico "geografico". Consultare la documentazione di Traffic Manager per un [elenco completo dei valori accettati](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
Specificare un nome di area di Azure.
Per un elenco completo delle aree di Azure, vedere aree di Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priorità
Specifica la priorità assegnata da Traffic Manager all'endpoint.
Questo parametro viene usato solo se il profilo di Traffic Manager è configurato con il metodo di routing prioritario.
I valori validi sono numeri interi compresi tra 1 e 1000.
I valori più bassi rappresentano la priorità più alta.

Se si specifica una priorità, è necessario specificare le priorità per tutti gli endpoint nel profilo e non ci sono due endpoint che condividono lo stesso valore di priorità.
Se non specifichi le priorità, Traffic Manager assegna i valori di priorità predefiniti agli endpoint, a partire da uno (1), nell'ordine in cui il profilo elenca gli endpoint.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Destinazione
Specifica il nome DNS completo dell'endpoint.
Traffic Manager restituisce questo valore nelle risposte DNS quando indirizza il traffico all'endpoint.
Specifica questo parametro solo per il tipo di endpoint ExternalEndpoints.
Per altri tipi di endpoint, specificare invece il parametro *TargetResourceId* .

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

### -TargetResourceId
Specifica l'ID risorsa della destinazione.
Specifica questo parametro solo per i tipi di endpoint AzureEndpoints e NestedEndpoints.
Per il tipo di endpoint ExternalEndpoints, specificare invece il parametro di *destinazione* .

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

### -TrafficManagerProfile
Specifica un oggetto **TrafficManagerProfile** locale.
Questo cmdlet modifica questo oggetto locale.
Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzureRmTrafficManagerProfile.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Digitare
Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di Azure Traffic Manager.
I valori validi sono: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Peso
Specifica il peso assegnato da Traffic Manager all'endpoint.
I valori validi sono numeri interi compresi tra 1 e 1000.
Il valore predefinito è uno (1).
Questo parametro viene usato solo se il profilo di Traffic Manager è configurato con il metodo di routing ponderato.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Questo cmdlet accetta un oggetto **TrafficManagerProfile** per questo cmdlet.

## OUTPUT

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Questo cmdlet restituisce un oggetto **TrafficManagerProfile** modificato.

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Remove-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


