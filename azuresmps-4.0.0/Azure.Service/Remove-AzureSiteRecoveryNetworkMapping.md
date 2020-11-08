---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029572"
---
# Remove-AzureSiteRecoveryNetworkMapping

## Sinossi
Rimuove un mapping di rete da un Vault di ripristino del sito.

## SINTASSI

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureSiteRecoveryNetworkMapping** rimuove un mapping di rete dall'archivio di ripristino del sito di Azure corrente.

## ESEMPI

### Esempio 1: rimuovere il mapping tra una rete e una rete di ripristino
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito Azure corrente usando il cmdlet **Get-AzureSiteRecoveryServer** .
Il comando Archivia i server di ripristino del sito nella variabile di matrice $Servers.

Il secondo comando ottiene il mapping tra la rete principale e la rete di ripristino e lo archivia nella variabile $NetworkMapping.
Il comando specifica il server primario per il mapping di rete come primo elemento di $Servers.
Il comando specifica il server per la rete di ripristino come secondo elemento di $Servers.

Il comando finale rimuove il mapping di rete in $NetworkMapping.

### Esempio 2: rimuovere il mapping tra una rete e una rete di macchine virtuali di Azure
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito corrente.
Il comando Archivia i server di ripristino del sito nella variabile di matrice $Servers.

Il secondo comando ottiene un mapping tra la rete principale e una rete di macchine virtuali di Azure e lo archivia nella variabile $NetworkMapping.
Il comando specifica il server principale per la rete come primo elemento di $Servers.
Il comando specifica il parametro *Azure* .
Di conseguenza, il comando ottiene il mapping a una rete di macchine virtuali di Azure.

Il comando finale rimuove il mapping di rete in $NetworkMapping.

## PARAMETRI

### -NetworkMapping
Specifica il mapping di rete da rimuovere.

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureSiteRecoveryNetworkMapping](./Get-AzureSiteRecoveryNetworkMapping.md)

[New-AzureSiteRecoveryNetworkMapping](./New-AzureSiteRecoveryNetworkMapping.md)

[Get-AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)


