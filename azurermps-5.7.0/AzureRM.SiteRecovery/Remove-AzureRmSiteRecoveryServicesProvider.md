---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 88b6b83f24edb06871fd87f61fec1732893b0f41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507955"
---
# Remove-AzureRmSiteRecoveryServicesProvider

## Sinossi
Rimuove un provider di servizi di ripristino di Azure sito.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureRmSiteRecoveryServicesProvider** rimuove un provider di servizi di ripristino di Azure sito dal Vault.

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

### -Force
Impone l'esecuzione del comando senza richiedere la conferma dell'utente.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicesProvider
Specifica l'oggetto provider di servizi.

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.

Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### ASRRecoveryServicesProvider
Il parametro ' ServicesProvider ' accetta il valore di tipo ' ASRRecoveryServicesProvider ' dalla pipeline

## OUTPUT

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRJob, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmSiteRecoveryServicesProvider](./Get-AzureRmSiteRecoveryServicesProvider.md)

[Update-AzureRmSiteRecoveryServicesProvider](./Update-AzureRmSiteRecoveryServicesProvider.md)
