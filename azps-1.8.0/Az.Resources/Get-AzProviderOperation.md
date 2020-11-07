---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bd0483cf03ac5cff224824cc41b3fab994006acb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677385"
---
# Get-AzProviderOperation

## Sinossi
Ottiene le operazioni per un provider di risorse Azure che sono a protezione diretta con Azure RBAC.

## SINTASSI

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il Get-AzProviderOperation ottiene le operazioni esposte dai provider di risorse Azure.
Le operazioni possono essere composte per creare ruoli personalizzati in Azure RBAC.
Il comando accetta come input una stringa di ricerca dell'operazione (con i caratteri jolly () possibili) *che determina i dettagli delle operazioni da visualizzare. Usare Get-AzProviderOperation * per ottenere tutte le operazioni per tutti i provider di risorse di Azure. USA Get-AzProviderOperation Microsoft. Compute/* per ottenere tutte le operazioni del provider di risorse Microsoft. Compute.

## ESEMPI

### Ottenere tutte le azioni per tutti i provider
```
PS C:\> Get-AzProviderOperation *
```

### Ottenere azioni per un determinato provider di risorse
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Ottenere tutte le azioni che è possibile eseguire nelle macchine virtuali
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## PARAMETRI

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
Stringa di ricerca dell'operazione (con caratteri jolly possibili (*))

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. resources. Models. PSResourceProviderOperation

## Note
Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment

## COLLEGAMENTI CORRELATI
