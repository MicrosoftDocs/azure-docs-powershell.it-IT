---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029664"
---
# New-AzureTrafficManagerProfile

## Sinossi
Crea un profilo di gestione traffico.

## SINTASSI

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureTrafficManagerProfile** crea un profilo di Microsoft Azure Traffic Manager.

Dopo aver creato un profilo in cui si imposta il valore *LoadBalancingMethod* su "failover", è possibile determinare l'ordine di failover degli endpoint aggiunti al profilo con il cmdlet Add-AzureTrafficManagerEndpoint.
Per altre informazioni, vedere l'esempio 2 seguente.

## ESEMPI

### Esempio 1: creare un profilo di Traffic Manager
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

Questo comando crea un profilo di gestione traffico denominato profilo nel dominio di gestione traffico specificato con un metodo di bilanciamento del carico rotondo Robin, un TTL di 30 secondi, il protocollo di monitoraggio HTTP, la porta di monitoraggio 80 e il percorso specificato.

### Esempio 2: riordinare gli endpoint nell'ordine di failover desiderato
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

### -DomainName
Specifica il nome di dominio del profilo di Traffic Manager.
Deve essere un sottodominio di trafficmanager.net.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

Required: True
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

Required: True
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

Required: True
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome del profilo di Traffic Manager da creare.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -TTL
Specifica il TTL (time-to-Live) DNS che informa i resolver DNS locali della durata della cache delle voci DNS.
I valori validi sono numeri interi compresi tra 30 e 999.999.

```yaml
Type: Int32
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

## OUTPUT

### Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition
Questo cmdlet genera un oggetto profilo di Traffic Manager.

## Note

## COLLEGAMENTI CORRELATI

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


