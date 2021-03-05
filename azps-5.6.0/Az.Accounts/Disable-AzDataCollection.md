---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 54af80b230c3cb031e8927a82ec3536cc1a81ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999080"
---
# Disable-AzDataCollection

## SYNOPSIS
Rifiuta esplicitamente di raccogliere dati per migliorare i cmdlet di Azure PowerShell. I dati vengono raccolti per impostazione predefinita, a meno che tu non lo rifiuti esplicitamente.

## SINTASSI

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE

Il `Disable-AzDataCollection` cmdlet viene usato per rifiutare esplicitamente la raccolta dei dati. Azure PowerShell raccoglie automaticamente i dati di telemetria per impostazione predefinita. Per disabilitare la raccolta dei dati, è necessario rifiutare esplicitamente. Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, identificare i problemi comuni e migliorare l'esperienza di Azure PowerShell. Microsoft Azure PowerShell non raccoglie dati privati o personali. Se in precedenza si è scelto di rifiutare esplicitamente, eseguire il cmdlet per abilitare nuovamente la raccolta dei dati per l'utente `Enable-AzDataCollection` corrente nel computer corrente.

## ESEMPI

### Esempio 1: Disabilitazione della raccolta dei dati per l'utente corrente

L'esempio seguente mostra come disabilitare la raccolta dei dati per l'utente corrente.

```powershell
Disable-AzDataCollection
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### System.Void

## NOTE

## COLLEGAMENTI CORRELATI

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
