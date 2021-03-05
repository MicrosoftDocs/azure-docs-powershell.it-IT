---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 61e38afcccccd6a96e92983d24442740351320ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016045"
---
# Get-AzProviderOperation

## SYNOPSIS
Ottiene le operazioni per un provider di risorse di Azure a protezione diretta con il controllo degli accessi in base al ruolo di Azure.

## SINTASSI

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
LGet-AzProviderOperation ottiene le operazioni esposte dai provider di risorse di Azure.
Le operazioni possono essere composte per creare ruoli personalizzati in Azure RBAC.
Il comando accetta come input una stringa di ricerca dell'operazione (con possibili caratteri jolly( ) caratteri che determina i *dettagli delle operazioni da visualizzare. Usare Get-AzProviderOperation * per ottenere tutte le operazioni per tutti i provider di risorse di Azure. Usare Get-AzProviderOperation Microsoft.Compute/* per ottenere tutte le operazioni del provider di risorse Microsoft.Compute.

## ESEMPI

### Esempio 1: Ottenere tutte le azioni per tutti i provider
```powershell
PS C:\> Get-AzProviderOperation *
```

### Esempio 2: Ottenere le azioni per un determinato provider di risorse
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Esempio 3: Ottenere tutte le azioni che possono essere eseguite nelle macchine virtuali
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## PARAMETERS

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -OperationSearchString
Stringa di ricerca dell'operazione (con possibili caratteri jolly (*)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation

## NOTE
Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione

## COLLEGAMENTI CORRELATI
