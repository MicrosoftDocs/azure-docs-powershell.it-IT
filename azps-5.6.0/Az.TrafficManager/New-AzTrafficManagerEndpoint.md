---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6d9ec806c1456f572991f7c72189c47abbe9ffe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987292"
---
# New-AzTrafficManagerEndpoint

## SYNOPSIS
Crea un endpoint in un profilo di Gestione traffico.

## SINTASSI

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzTrafficManagerEndpoint** crea un endpoint in un profilo di Gestione traffico di Azure.

Questo cmdlet esegue il commit di ogni nuovo endpoint nel servizio Di gestione del traffico.
Per aggiungere più endpoint a un oggetto profilo di Gestione traffico locale ed eseguire il commit delle modifiche in una singola operazione, usare il cmdlet Add-AzTrafficManagerEndpointConfig locale.

## ESEMPI

### Esempio 1: Creare un endpoint esterno per un profilo
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Questo comando crea un endpoint esterno denominato contoso nel profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11.

### Esempio 2: Creare un endpoint di Azure per un profilo
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

Questo comando crea un endpoint di Azure denominato contoso nel profilo denominato ContosoProfile nel gruppo di risorse ResourceGroup11.
L'endpoint di Azure punta all'app Web di Azure per cui l'ID di Gestione risorse di Azure viene assegnato dal percorso URI in *TargetResourceId.*
Il comando non specifica il parametro *EndpointLocation* perché la risorsa Web App fornisce la posizione.

## PARAMETERS

### -CustomHeader
Elenco di coppie di nomi di intestazione e valori personalizzati per le richieste di risposta.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -EndpointLocation
Specifica la posizione dell'endpoint da usare nel metodo di routing del traffico delle prestazioni.
Questo parametro è applicabile solo agli endpoint di tipo ExternalEndpoints o NestedEndpoints.
È necessario specificare questo parametro quando viene usato il metodo di routing del traffico delle prestazioni.

Specifica un nome di area geografica Azure.
Per un elenco completo delle aree geografiche di Azure, vedere Aree geografiche di Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .

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

Se lo stato è Abilitato, è probabile che l'integrità dell'endpoint sia inclusa nel metodo di routing del traffico.

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

### -GeoMapping
Elenco di aree geografiche mappato a questo endpoint quando si usa il metodo di routing del traffico "Geografico". Per un elenco completo dei valori accettati, consultare la documentazione di Gestione traffico.

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

### -MinEndpoints
Specifica un nome di area geografica Azure.
Per un elenco completo delle aree geografiche di Azure, vedere Aree geografiche di Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .

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

### -Name
Specifica il nome dell'endpoint di Gestione traffico creato dal cmdlet.

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

### -Priority
Specifica la priorità assegnata da Gestione traffico all'endpoint.
Questo parametro viene usato solo se il profilo di Gestione traffico è configurato con il metodo di instradamento del traffico prioritario.
I valori validi sono numeri interi da 1 a 1000.
I valori inferiori rappresentano la priorità più alta.

Se si specifica una priorità, è necessario specificare le priorità in tutti gli endpoint del profilo e nessun endpoint può condividere lo stesso valore di priorità.
Se non si specificano le priorità, Gestione traffico assegna valori di priorità predefiniti agli endpoint, a partire da uno (1), nell'ordine in cui il profilo elenca gli endpoint.

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
Specifica il nome di un profilo di Gestione traffico a cui questo cmdlet aggiunge un endpoint.
Per ottenere un profilo, usare i cmdlet New-AzTrafficManagerProfile o Get-AzTrafficManagerProfile di accesso.

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
Questo cmdlet crea un endpoint di Gestione traffico nel gruppo specificato da questo parametro.

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

### -SubnetMapping
L'elenco di intervalli di indirizzi o subnet mappati a questo endpoint quando si usa il metodo di routing del traffico "Subnet".

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Target
Specifica il nome DNS completo dell'endpoint.
Gestione traffico restituisce questo valore nelle risposte DNS quando indirizza il traffico a questo endpoint.
Specificare questo parametro solo per il tipo di endpoint ExternalEndpoints.
Per altri tipi di endpoint, specificare *invece il parametro TargetResourceId.*

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
Specificare questo parametro solo per i tipi di endpoint AzureEndpoints e NestedEndpoints.
Per il tipo di endpoint ExternalEndpoints, specificare *il parametro Target.*

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

### -Type
Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di Gestione traffico.
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

### -Spessore
Specifica il peso assegnato da Gestione traffico all'endpoint.
I valori validi sono numeri interi da 1 a 1000.
Il valore predefinito è 1 (1).
Questo parametro viene usato solo se il profilo di Gestione traffico è configurato con il metodo weighted traffic-routing.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## NOTE

## COLLEGAMENTI CORRELATI

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


