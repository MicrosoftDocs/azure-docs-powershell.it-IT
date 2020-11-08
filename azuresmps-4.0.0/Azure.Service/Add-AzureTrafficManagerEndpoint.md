---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029838"
---
# Add-AzureTrafficManagerEndpoint

## Sinossi
Aggiunge un endpoint a un profilo di gestione traffico.

## SINTASSI

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureTrafficManagerEndpoint** aggiunge un endpoint a un profilo di gestione traffico di Microsoft Azure.
Dopo aver aggiunto un endpoint, passa il risultato al cmdlet **set-AzureTrafficManagerProfile** usando l'operatore pipeline.
Questo cmdlet si connette a Azure per salvare le modifiche.

## ESEMPI

### Esempio 1: aggiungere un endpoint a un profilo
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

Il primo comando usa il cmdlet **Get-AzureTrafficManagerProfile** per ottenere il profilo denominato ContosoProfile e lo archivia nella variabile $TrafficManagerProfile.

Il secondo comando aggiunge un endpoint al profilo di Traffic Manager archiviato in $TrafficManagerProfile.
L'endpoint ha il nome di dominio Contoso02App.couldapp.net.
Il comando specifica anche se è abilitato e il relativo tipo.
Il comando passa l'oggetto profile al cmdlet **set-AzureTrafficManagerProfile** per connettersi a Azure per salvare le modifiche.

### Esempio 2: aggiungere un endpoint con una posizione e un peso specificati
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

Questo comando aggiunge un endpoint a un profilo di gestione traffico.
L'endpoint ha il nome di dominio Contoso02App.couldapp.net.
Il comando specifica anche se è abilitato e il relativo tipo.
Il comando specifica anche il peso e la posizione per l'endpoint.
Il comando passa l'oggetto profile a **set-AzureTrafficManagerProfile** per connettersi ad Azure per salvare le modifiche.

## PARAMETRI

### -DomainName
Specifica il nome di dominio dell'endpoint da aggiungere.

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

### -Posizione
Specifica la posizione dell'endpoint aggiunto dal cmdlet.
Deve essere una posizione di Azure.

Questo parametro deve contenere un valore per gli endpoint del tipo "any" o di tipo "TrafficManager" in un profilo con il metodo di bilanciamento del carico impostato su "performance".
I valori possibili sono i nomi delle aree di Azure, come indicato in https://azure.microsoft.com/regions/ .

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

### -MinChildEndpoints
Specifica il numero minimo di endpoint che il profilo annidato deve avere online affinché l'endpoint venga considerato online.

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

### -Stato
Specifica lo stato dell'endpoint di monitoraggio.
I valori validi sono: 

- Abilitato
- Disabilitato

Se specifichi un valore di Enabled, Traffic Manager monitora l'endpoint e il metodo di bilanciamento del carico lo considera quando Gestisci il traffico.

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

### -TrafficManagerProfile
Specifica l'oggetto profilo Traffic Manager a cui aggiungere l'endpoint.

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

### -Digitare
Specifica il tipo di endpoint.
I valori validi sono: 

- CloudService
- AzureWebsite
- TrafficManager

- Qualsiasi 

Se sono presenti più endpoint AzureWebsite, gli endpoint devono trovarsi in diversi datacenter.

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

### -Peso
Specifica il peso dell'endpoint aggiunto dal cmdlet.
L'intervallo di valori valido per questo parametro è 1.000 \[ \] .

Questo parametro viene usato solo per i criteri di bilanciamento del carico di RoundRobin.

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
Questo cmdlet genera un oggetto profilo di Traffic Manager, che contiene informazioni sul profilo aggiornato.

## Note

## COLLEGAMENTI CORRELATI

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


