---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191146"
---
# Get-AzStorageUsage

## Sinossi
Ottiene l'utilizzo della risorsa di archiviazione dell'abbonamento corrente.

## SINTASSI

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzStorageUsage** Ottiene l'utilizzo delle risorse per l'archiviazione di Azure per l'abbonamento corrente.

## ESEMPI

### Esempio 1: ottenere l'utilizzo delle risorse di archiviazione della posizione specificata
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

Questo comando consente di ottenere l'utilizzo delle risorse di archiviazione della posizione specificata sotto l'abbonamento corrente.

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

### -Posizione
Indicare per ottenere l'utilizzo delle risorse di archiviazione nella posizione specificata.
Se non specificato, otterrà l'utilizzo delle risorse di archiviazione in tutti i percorsi della sottoscrizione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Management. storage. Models. PSUsage

## Note

## COLLEGAMENTI CORRELATI

[Cmdlet di Azure Storage Manager](./Az.Storage.md)


