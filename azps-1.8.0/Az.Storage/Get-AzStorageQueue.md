---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: 1f0e9f17ea6d240f9f29f677325173e0bbef38f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676611"
---
# Get-AzStorageQueue

## Sinossi
Elenca le code di archiviazione.

## SINTASSI

### QueueName (impostazione predefinita)
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### QueuePrefix
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzStorageQueue** elenca le code di archiviazione associate a un account di archiviazione di Azure.

## ESEMPI

### Esempio 1: elencare tutte le code di archiviazione di Azure
```
PS C:\>Get-AzStorageQueue
```

Questo comando consente di ottenere un elenco di tutte le code di archiviazione per l'account di archiviazione corrente.

### Esempio 2: elencare le code di archiviazione di Azure usando un carattere jolly
```
PS C:\>Get-AzStorageQueue -Name queue*
```

Questo comando usa un carattere jolly per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.

### Esempio 3: code di archiviazione di elenchi di Azure tramite il prefisso del nome della coda
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

Questo esempio usa il parametro *Prefix* per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.

## PARAMETRI

### -Contesto
Specifica il contesto di archiviazione di Azure.
Puoi crearlo usando il cmdlet **New-AzStorageContext** .

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica un nome.
Se non viene specificato alcun nome, il cmdlet riceve un elenco di tutte le code.
Se viene specificato un nome completo o parziale, il cmdlet ottiene tutte le code che corrispondono al modello di nome.

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefisso
Specifica un prefisso usato nel nome delle code che vuoi ottenere.

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

[New-AzStorageQueue](./New-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


