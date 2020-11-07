---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: d4e58e1fc2da68d9293afa27072a4cf32023f661
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686796"
---
# Get-AzureRmProviderOperation

## Sinossi
Ottiene le operazioni per un provider di risorse Azure che sono a protezione diretta con Azure RBAC.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmProviderOperation [-OperationSearchString] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il Get-AzureRmProviderOperation ottiene le operazioni esposte dai provider di risorse Azure.
Le operazioni possono essere composte per creare ruoli personalizzati in Azure RBAC.
Il comando accetta come input una stringa di ricerca dell'operazione (con i possibili caratteri jolly (*)) che determina i dettagli delle operazioni da visualizzare.

Usare Get-AzureRmProviderOperation * per ottenere tutte le operazioni per tutti i provider di risorse di Azure.

USA Get-AzureRmProviderOperation Microsoft. COMPUTE/* per ottenere tutte le operazioni del provider di risorse Microsoft. Compute.

## ESEMPI

### --------------------------Ottenere tutte le azioni per tutti i provider--------------------------
```
PS C:\> Get-AzureRmProviderOperation *
```

### --------------------------Ottenere azioni per un provider di risorse specifico--------------------------
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### --------------------------Ottenere tutte le azioni che possono essere eseguite sulle macchine virtuali--------------------------
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## PARAMETRI

### -OperationSearchString
Stringa di ricerca dell'operazione (con caratteri jolly possibili (*))

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Stringa
Il parametro ' OperationSearchString ' accetta il valore di tipo ' String ' dalla pipeline

## OUTPUT

### Microsoft. Azure. Commands. resources. Models. PSResourceProviderOperation

## Note
Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment

## COLLEGAMENTI CORRELATI

