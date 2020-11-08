---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023541"
---
# Get-AzureSiteRecoveryRecoveryPlanFile

## Sinossi
Scarica un piano di ripristino di un sito Azure in formato XML.

## SINTASSI

### ByRPObject (impostazione predefinita)
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureSiteRecoveryRecoveryPlanFile** Scarica un piano di ripristino del sito di Azure in formato XML.
È possibile usare questo file per aggiornare il piano di ripristino e quindi caricarlo nel server di ripristino del sito.

Un piano di ripristino raccoglie le macchine virtuali in un gruppo per scopi di failover e ripristino.

## ESEMPI

### Esempio 1: ottenere un file piano di ripristino
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

Questo comando usa il cmdlet **Get-AzureSiteRecoveryRecoveryPlan** per ottenere il piano di ripristino e lo archivia nella variabile $RecoveryPlan.

Il secondo comando usa il cmdlet **GetAzureSiteRecoveryRecoveryPlanFile** per ottenere il file XML del piano di ripristino del sito in $RecoveryPlan.
Il comando Archivia il file XML nel percorso specificato.

## PARAMETRI

### -ID
Specifica l'ID del piano di ripristino da ottenere.

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

### -Path
Specifica il percorso completo in cui archiviare il file XML del piano di ripristino.

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

### -RecoveryPlan
Specifica un oggetto **ASRRecoveryPlan** da cui ottenere il piano di ripristino.
Per ottenere un oggetto **ASRRecoveryPlan** , usa il cmdlet **Get-AzureSiteRecoveryRecoveryPlan** .

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureSiteRecoveryRecoveryPlan](./Get-AzureSiteRecoveryRecoveryPlan.md)


