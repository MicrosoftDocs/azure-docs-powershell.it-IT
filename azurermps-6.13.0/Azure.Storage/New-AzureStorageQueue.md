---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 62fc501c267e388498cb1563206d2efac083c058
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512084"
---
# New-AzureStorageQueue

## Sinossi
Crea una coda di archiviazione.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureStorageQueue** crea una coda di archiviazione in Azure.

## ESEMPI

### Esempio 1: creare una coda di archiviazione di Azure
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

Questo esempio crea una coda di archiviazione denominata queueabc.

### Esempio 2: creare più code di archiviazione di Azure
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

Questo esempio crea più code di archiviazione.
Usa il metodo Split della classe String .NET e quindi passa i nomi sulla pipeline.

## PARAMETRI

### -Contesto
Specifica il contesto di archiviazione di Azure.
Puoi crearlo usando il cmdlet New-AzureStorageContext.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -Nome
Specifica un nome per la coda.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext

## OUTPUT

### Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageQueue

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorageQueue](./Get-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


