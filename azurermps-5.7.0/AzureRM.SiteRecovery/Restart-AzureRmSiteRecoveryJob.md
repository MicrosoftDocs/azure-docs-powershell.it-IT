---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/restart-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 17486f4a22e488a147fcdd8a8e085c7900fc8147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507939"
---
# Restart-AzureRmSiteRecoveryJob

## Sinossi
Riavvia un processo di ripristino del sito di Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ByObject (impostazione predefinita)
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Restart-AzureRmSiteRecoveryJob riavvia** un processo di ripristino del sito di Azure.

## ESEMPI

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Specifica l'oggetto processo di ripristino del sito.

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

### -Nome
Specifica il nome univoco per il processo.

```yaml
Type: String
Parameter Sets: ByName
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

### ASRJob
Il parametro "Job" accetta il valore di tipo "ASRJob" dalla pipeline

## OUTPUT

### Microsoft. Azure. Commands. SiteRecovery. ASRJob

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmSiteRecoveryJob](./Get-AzureRmSiteRecoveryJob.md)

[Curriculum vitae-AzureRmSiteRecoveryJob](./Resume-AzureRmSiteRecoveryJob.md)

[Stop-AzureRmSiteRecoveryJob](./Stop-AzureRmSiteRecoveryJob.md)
