---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192202"
---
# Update-AzRecoveryServicesAsrProtectionContainerMapping

## Sinossi
Aggiornare il mapping del contenitore di protezione del ripristino di Azure site.

## SINTASSI

### AzureToAzureEnableAutoUpdate (impostazione predefinita)
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureToAzureDisableAutoUpdate
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Update-AzRecoveryServicesAsrProtectionContainerMapping** aggiorna il mapping del contenitore di protezione del ripristino del sito di Azure specificato.

## ESEMPI

### Esempio 1
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

Avviare l'operazione per disabilitare l'aggiornamento automatico per container.

### Esempio 2
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

Avviare l'operazione per disabilitare Enable Auto Update per container.

## PARAMETRI

### -AutomationAccountId
Specifica il accountId di automazione usato per la UDPATE automatica.

```yaml
Type: System.String
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToAzure
Specifica Azure to Azure Protection container.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### -DisableAutoUpdate
Parametro switch per disabilitare l'aggiornamento automatico.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureDisableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoUpdate
Parametro switch per abilitare l'aggiornamento automatico.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Oggetto per il mapping del contenitore di protezione.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping

## OUTPUT

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## Note

## COLLEGAMENTI CORRELATI
