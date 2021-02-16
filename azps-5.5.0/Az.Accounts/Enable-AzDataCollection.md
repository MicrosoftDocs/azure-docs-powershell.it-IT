---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195438"
---
# Enable-AzDataCollection

## SYNOPSIS
Consente ad Azure PowerShell di raccogliere dati per migliorare l'esperienza utente con i cmdlet di Azure PowerShell. Eseguendo questo cmdlet si acconsente esplicitamente alla raccolta dei dati per l'utente corrente nel computer corrente. I dati vengono raccolti per impostazione predefinita, a meno che tu non lo rifiuti esplicitamente.

## SINTASSI

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE

Il `Enable-AzDataCollection` cmdlet viene usato per acconsentire esplicitamente alla raccolta dei dati. Azure PowerShell raccoglie automaticamente i dati di telemetria per impostazione predefinita. Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, identificare i problemi comuni e migliorare l'esperienza di Azure PowerShell.
Microsoft Azure PowerShell non raccoglie dati privati o personali. Per disabilitare la raccolta dei dati, è necessario rifiutare esplicitamente `Disable-AzDataCollection` l'esecuzione.

## ESEMPI

### Esempio 1: Abilitazione della raccolta dei dati per l'utente corrente

L'esempio seguente mostra come abilitare la raccolta dei dati per l'utente corrente.

```powershell
Enable-AzDataCollection
```

## PARAMETERS

### -DefaultProfile

Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -Confirm

Chiede conferma prima di eseguire il cmdlet.

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

Mostra cosa accadrebbe se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

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

Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](/powershell/module/microsoft.powershell.core/about/about_commonparameters)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### System.Void

## NOTE

## COLLEGAMENTI CORRELATI

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
