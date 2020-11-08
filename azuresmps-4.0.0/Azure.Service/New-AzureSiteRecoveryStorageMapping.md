---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023933"
---
# New-AzureSiteRecoveryStorageMapping

## Sinossi
Crea un mapping tra un oggetto di archiviazione di Azure e un oggetto di archiviazione di ripristino.

## SINTASSI

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureSiteRecoveryStorageMapping** crea un mapping tra un oggetto di archiviazione di Azure primaria gestito e un oggetto di archiviazione di ripristino di Azure sito.

## ESEMPI

### Esempio 1: creare un mapping tra un oggetto di archiviazione e un oggetto di archiviazione di ripristino
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito Azure corrente usando il cmdlet **Get-AzureSiteRecoveryServer** .
Il comando Archivia i server di ripristino del sito nella variabile di matrice $Servers.

Il secondo comando consente di ottenere l'archiviazione di ripristino del sito per il primo server nella matrice $Servers e quindi di archiviarla nel $Storages.

Il comando finale crea un mapping tra la rete principale e la rete di ripristino.
Il comando specifica l'oggetto di archiviazione principale come primo elemento di $Storages.
Il comando specifica l'oggetto di archiviazione di ripristino come secondo elemento di $Storages.

## PARAMETRI

### -PrimaryStorage
Specifica lo spazio di archiviazione principale da associare all'archivio di ripristino.
Per ottenere un oggetto **ASRStorage** , usa il cmdlet Get-AzureSiteRecoveryStorage.

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -RecoveryStorage
Specifica l'oggetto di archiviazione di ripristino.
Questo cmdlet associa l'oggetto di archiviazione principale all'oggetto di archiviazione specificato da questo parametro.
Per ottenere un oggetto **ASRStorage** , USA **Get-AzureSiteRecoveryStorage**.

```yaml
Type: ASRStorage
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

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)

[Get-AzureSiteRecoveryStorageMapping](./Get-AzureSiteRecoveryStorageMapping.md)

[Remove-AzureSiteRecoveryStorageMapping](./Remove-AzureSiteRecoveryStorageMapping.md)


