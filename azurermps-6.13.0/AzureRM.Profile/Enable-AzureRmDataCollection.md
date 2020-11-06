---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
ms.openlocfilehash: 83c7bda6c7b41f857bac9b63afcca07baa6ecd93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521307"
---
# Enable-AzureRmDataCollection

## Sinossi
Consente a Azure PowerShell di raccogliere dati per migliorare l'esperienza utente con i cmdlet di AzurePowerShell.
L'esecuzione di questo cmdlet consente di optare per la raccolta di dati per l'utente corrente nel computer corrente.
Non vengono raccolti dati a meno che non si opti esplicitamente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Enable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Puoi migliorare l'esperienza dell'uso di Microsoft Cloud ed Azure PowerShell optando per la raccolta di dati.
In Azure PowerShell non vengono raccolti dati senza il consenso: è necessario esplicitamente eseguire l'opt-in eseguendo Enable-AzureRmDataCollection o rispondendo a Sì quando in Azure PowerShell viene richiesto di raccogliere i dati al primo avvio di un cmdlet.
Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, per identificare i problemi comuni e migliorare l'esperienza dell'uso di Azure PowerShell.
Microsoft Azure PowerShell non raccoglie dati privati o informazioni personali.
Eseguire il cmdlet Enable-AzureRMDataCollection per abilitare la raccolta dati per l'utente corrente nel computer corrente.
In questo modo verrà impedito agli utenti correnti di richiedere la raccolta dei dati per la prima volta che vengono eseguiti i cmdlet.
Per disabilitare la raccolta dati per l'utente corrente, eseguire il cmdlet Disable-AzureRmDataCollection.

## ESEMPI

### Esempio 1: abilitazione della raccolta dati per l'utente corrente
```
PS C:\> Enable-AzureRmDataCollection
```

Questo esempio Mostra come abilitare la raccolta dati per l'utente corrente.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
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

### Nessuno

## OUTPUT

### System. void

## Note

## COLLEGAMENTI CORRELATI

[Disable-AzureRmDataCollection](./Disable-AzureRmDataCollection.md)

