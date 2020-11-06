---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 7eaadd8c80fff6491983a3e1d9c750227eba43cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508508"
---
# New-AzureRmTrafficManagerEndpoint

## Sinossi
Crea un endpoint in un profilo di gestione traffico.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmTrafficManagerEndpoint** crea un endpoint in un profilo di gestione traffico di Azure.

Questo cmdlet consente di eseguire il commit di ogni nuovo endpoint nel servizio gestione traffico.
Per aggiungere più endpoint a un oggetto profilo di gestione traffico locale e eseguire il commit delle modifiche in una singola operazione, usare il cmdlet Add-AzureRmTrafficManagerEndpointConfig.

## ESEMPI

### Esempio 1: creare un endpoint esterno per un profilo
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Questo comando crea un endpoint esterno denominato Contoso nel profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11.

### Esempio 2: creare un endpoint Azure per un profilo
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

Questo comando crea un endpoint Azure denominato Contoso nel profilo denominato ContosoProfile nel gruppo di risorse ResouceGroup11.
L'endpoint di Azure punta a Azure Web App il cui ID di gestione delle risorse di Azure viene assegnato dal percorso URI in *TargetResourceId*.
Il comando non specifica il parametro *EndpointLocation* perché la risorsa dell'app Web fornisce la posizione.

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
L'elenco delle aree geografiche mappate a questo endpoint quando si usa il metodo di routing del traffico "geografico". Consultare la documentazione di Traffic Manager per un elenco completo dei valori accettati.
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

### -Nome
Specifica il nome dell'endpoint di gestione traffico creato dal cmdlet.

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

### -ProfileName
Specifica il nome di un profilo di gestione traffico a cui questo cmdlet aggiunge un endpoint.
Per ottenere un profilo, usare i cmdlet New-AzureRmTrafficManagerProfile o Get-AzureRmTrafficManagerProfile.

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

### -ResourceGroupName
Specifica il nome di un gruppo di risorse.
Questo cmdlet crea un endpoint di gestione traffico nel gruppo specificato da questo parametro.

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

### -Digitare
Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di gestione traffico.
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

## OUTPUT

### Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint

## Note

## COLLEGAMENTI CORRELATI

[Disable-AzureRmTrafficManagerEndpoint](./Disable-AzureRmTrafficManagerEndpoint.md)

[Enable-AzureRmTrafficManagerEndpoint](./Enable-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerEndpoint](./Get-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpoint](./Remove-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


