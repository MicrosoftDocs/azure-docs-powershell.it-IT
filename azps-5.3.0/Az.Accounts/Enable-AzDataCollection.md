---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479183"
---
# Enable-AzDataCollection

## Sinossi
Consente a Azure PowerShell di raccogliere dati per migliorare l'esperienza utente con i cmdlet di PowerShell di Azure. L'esecuzione di questo cmdlet consente di optare per la raccolta di dati per l'utente corrente nel computer corrente. I dati vengono raccolti per impostazione predefinita, a meno che non vengano esplicitamente rifiutati.

## SINTASSI

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione

Il `Enable-AzDataCollection` cmdlet viene usato per l'opt-in per la raccolta dei dati. Azure PowerShell raccoglie automaticamente i dati di telemetria per impostazione predefinita. Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, per identificare i problemi comuni e per migliorare l'esperienza di Azure PowerShell.
Microsoft Azure PowerShell non raccoglie dati personali o privati. Per disabilitare la raccolta dati, è necessario disconnettersi esplicitamente eseguendo `Disable-AzDataCollection` .

## ESEMPI

### Esempio 1: abilitazione della raccolta dati per l'utente corrente

L'esempio seguente mostra come abilitare la raccolta di dati per l'utente corrente.

```powershell
Enable-AzDataCollection
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

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
