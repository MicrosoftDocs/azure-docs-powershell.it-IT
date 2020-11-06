---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
ms.openlocfilehash: 64e3857ddd9a9bb00b94e3e550c6be33722990a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508996"
---
# Get-AzureRmStorageContainer

## Sinossi
Ottiene o elenca i contenitori BLOB di archiviazione

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### AccountName (impostazione predefinita)
```
Get-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AccountObject
```
Get-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmStorageContainer** Ottiene o elenca i contenitori BLOB di archiviazione

## ESEMPI

### Esempio 1: ottenere un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" 
```

Questo comando ottiene un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.

### Esempio 2: elencare tutti i contenitori BLOB di archiviazione di un account di archiviazione
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" 
```

Questo comando elenca tutti i contenitori BLOB di archiviazione di un account di archiviazione con il nome dell'account di archiviazione.

### Esempio 3: ottenere un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" 
```

Questo comando ottiene un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome contenitore

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccount
Oggetto account di archiviazione

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Nome dell'account di archiviazione.

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Management. storage. Models. PSContainer

## Note

## COLLEGAMENTI CORRELATI

