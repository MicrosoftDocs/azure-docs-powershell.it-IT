---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029869"
---
# Stop-AzureSiteRecoveryJob

## Sinossi
Interrompe un processo di ripristino del sito.

## SINTASSI

### ByObject (impostazione predefinita)
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Stop-AzureSiteRecoveryJob** arresta un processo di ripristino di Azure site.

## ESEMPI

### Esempio 1: arrestare tutti i processi
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

Il primo comando ottiene i processi di ripristino dei siti di Azure per il Vault di ripristino del sito di Azure corrente usando il cmdlet **Get-AzureSiteRecoveryJob** e quindi archivia i risultati nella variabile $Jobs.

Il secondo comando arresta i processi specificati da $Jobs.

## PARAMETRI

### -ID
Specifica l'ID del processo da interrompere.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Specifica il processo da interrompere.

```yaml
Type: ASRJob
Parameter Sets: ByObject
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

[Get-AzureSiteRecoveryJob](./Get-AzureSiteRecoveryJob.md)

[Riavviare-AzureSiteRecoveryJob](./Restart-AzureSiteRecoveryJob.md)

[Curriculum vitae-AzureSiteRecoveryJob](./Resume-AzureSiteRecoveryJob.md)


