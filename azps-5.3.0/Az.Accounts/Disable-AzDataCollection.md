---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479192"
---
# Disable-AzDataCollection

## Sinossi
Opta per la raccolta di dati per migliorare i cmdlet di PowerShell di Azure. I dati vengono raccolti per impostazione predefinita, a meno che non vengano esplicitamente rifiutati.

## SINTASSI

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione

Il `Disable-AzDataCollection` cmdlet viene usato per rifiutare la raccolta dei dati. Azure PowerShell raccoglie automaticamente i dati di telemetria per impostazione predefinita. Per disabilitare la raccolta dati, è necessario escludere esplicitamente l'opzione. Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, per identificare i problemi comuni e per migliorare l'esperienza di Azure PowerShell. Microsoft Azure PowerShell non raccoglie dati personali o privati. Se in precedenza è stato scelto, eseguire il `Enable-AzDataCollection` cmdlet per riattivare la raccolta dati per l'utente corrente nel computer corrente.

## ESEMPI

### Esempio 1: disabilitazione della raccolta dati per l'utente corrente

L'esempio seguente mostra come disabilitare la raccolta dati per l'utente corrente.

```powershell
Disable-AzDataCollection
```

## PARAMETRI

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

Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INGRESSI

### Nessuno

## OUTPUT

### System. void

## Note

## COLLEGAMENTI CORRELATI

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
