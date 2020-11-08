---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023752"
---
# Set-AzureTrafficManagerProfile

## Sinossi
Aggiorna le proprietà di un profilo di gestione traffico.

## SINTASSI

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureTrafficManagerProfile** aggiorna le proprietà di un profilo di gestione traffico di Microsoft Azure.

Per i profili per cui è stato impostato il valore *LoadBalancingMethod* su "failover", è possibile determinare l'ordine di failover degli endpoint aggiunti al profilo con il cmdlet Add-AzureTrafficManagerEndpoint.
Per altre informazioni, vedere l'esempio 3 seguente.

## ESEMPI

### Esempio 1: impostare il TTL per un profilo di gestione traffico
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

Questo comando imposta il TTL su 60 secondi per l'oggetto MyTrafficManagerProfile del profilo di Traffic Manager.

### Esempio 2: impostare diversi valori per un profilo
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

Questo comando ottiene un profilo di gestione traffico denominato profilo tramite il cmdlet **Get-AzureTrafficManagerProfile** .
Il profilo usa il metodo di bilanciamento del carico RoundRobin, un TTL di 30 secondi, il protocollo HTTP monitor, la porta del monitor e il percorso relativo di un profilo di gestione traffico.

### Esempio 3: riordinare gli endpoint nell'ordine di failover desiderato
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

In questo esempio vengono riordinati gli endpoint aggiunti a my profile all'ordine di failover desiderato.

Il primo comando ottiene l'oggetto profilo Traffic Manager denominato profilo e archivia l'oggetto nella variabile $Profile.

Il secondo comando Riordina gli endpoint dalla matrice Endpoints all'ordine in cui deve essere eseguito il failover.

L'ultimo comando Aggiorna il profilo di Traffic Manager archiviato in $Profile con il nuovo ordine di endpoint.

## PARAMETRI

### -LoadBalancingMethod
Specifica il metodo di bilanciamento del carico da usare per distribuire la connessione.
I valori validi sono: 

- Prestazioni
- Failover
- RoundRobin

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorPort
Specifica la porta utilizzata per monitorare l'integrità dell'endpoint.
I valori validi sono valori interi maggiori di 0 e minore o uguale a 65.535.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorProtocol
Specifica il protocollo da usare per monitorare l'integrità degli endpoint.
I valori validi sono: 

- Http
- Https

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorRelativePath
Specifica il percorso relativo al nome di dominio dell'endpoint da sondare per lo stato di integrità.
Il percorso deve soddisfare le restrizioni seguenti: 

- Il percorso deve essere compreso tra 1 e 1000 caratteri.
- Deve iniziare con una barra di avanzamento/.
- Non deve contenere elementi XML \<\> .
- Non deve contenere barre doppie,//.
- Non deve contenere caratteri di escape HTML non validi.
Ad esempio,% XY.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome del profilo di Traffic Manager da aggiornare.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet. Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Specifica l'oggetto profilo Traffic Manager usato per impostare il profilo.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -TTL
Specifica il TTL (time-to-Live) DNS che informa i resolver DNS locali della durata della cache delle voci DNS.
I valori validi sono un numero intero compreso tra 30 e 999.999.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

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

### Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition
Questo cmdlet genera un oggetto profilo di Traffic Manager.

## Note

## COLLEGAMENTI CORRELATI

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)


