---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301135"
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

### Esempio 1: ottenere tutte le azioni per tutti i provider
```powershell
PS C:\> Get-AzProviderOperation *
```

### Esempio 2: ottenere azioni per un determinato provider di risorse
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Esempio 3: ottenere tutte le azioni che possono essere eseguite sulle macchine virtuali
```powershell
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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. resources. Models. PSResourceProviderOperation

## Note
Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment

## COLLEGAMENTI CORRELATI
