---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205210"
---
# New-AzBatchResourceFile

## SYNOPSIS
Crea un file di risorse per l'utilizzo da parte di `New-AzBatchTask` .

## SINTASSI

### HttpUrl (impostazione predefinita)
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContainerUrl
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AutoStorageContainerName
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Crea un file di risorse per l'utilizzo da parte di `New-AzBatchTask` .

## ESEMPI

### Esempio 1: Creare un file di risorse da un URL HTTP che punta a un singolo file
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Crea un `PSResourceFile` riferimento a un URL HTTP.

### Esempio 2: Creare un file di risorse da un URL del contenitore di Archiviazione di Azure
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Crea un riferimento a un URL del `PSResourceFile` contenitore di archiviazione di Azure. Tutti i file nel contenitore verranno scaricati nella cartella specificata.

### Esempio 3: Creare un file di risorse da un nome di contenitore Archiviazione automatica
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Crea un riferimento `PSResourceFile` a un nome di contenitore Archiviazione automatica. Tutti i file nel contenitore verranno scaricati nella cartella specificata.

## PARAMETERS

### -AutoStorageContainerName
Nome del contenitore di archiviazione nell'account di archiviazione automatico.

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobPrefix
Ottiene il prefisso BLOB da usare per il download di BLOB da un contenitore archiviazione di Azure.
Verranno scaricati solo i BLOB i cui nomi iniziano con il prefisso specificato.
Il prefisso può essere un nome file parziale o una sottodirectory.
Se non si specificato un prefisso, verranno scaricati tutti i file nel contenitore.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -FileMode
Ottiene l'attributo della modalità di autorizzazione file in formato ottale.
Questa proprietà è applicabile solo se il file di risorse viene scaricato in un nodo Linux.
Se questa proprietà non è specificata per un nodo Linux, il valore predefinito è 0770.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
Posizione nel nodo di elaborazione in cui scaricare i file, rispetto alla directory di lavoro dell'attività. Se si specifica il parametro HttpUrl, filePath è obbligatorio e descrive il percorso in cui verrà scaricato il file, incluso il nome file. In caso contrario, se vengono specificati i parametri AutoStorageContainerName o StorageContainerUrl, FilePath è facoltativo ed è la directory in cui scaricare i file. Nel caso in cui FilePath viene usato come directory, tutte le strutture di directory già associate ai dati di input verranno conservate completamente e aggiunte alla directory FilePath specificata. Il percorso relativo specificato non può uscire dalla directory di lavoro dell'attività, ad esempio usando "..".

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpUrl
URL del file da scaricare.
Se l'URL è Archiviazione BLOB Azure, deve essere leggibile con l'accesso anonimo; il servizio batch non presenta le credenziali durante il download del BLOB.
Esistono due modi per ottenere un URL di questo tipo per un BLOB in Archiviazione di Azure: includere una firma di accesso condiviso che concede autorizzazioni di lettura per il BLOB oppure impostare l'ACL per il BLOB o il contenitore per consentire l'accesso pubblico.

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerUrl
URL del contenitore BLOB all'interno di Archiviazione BLOB di Azure.
Questo URL deve essere leggibile ed elencabile utilizzando l'accesso anonimo; il servizio batch non presenta le credenziali durante il download di BLOB dal contenitore.
Esistono due modi per ottenere un URL di questo tipo per un contenitore in Archiviazione di Azure: includere una firma di accesso condiviso che concede autorizzazioni di lettura per il contenitore oppure impostare l'ACL per il contenitore in modo da consentire l'accesso pubblico.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Batch. Models.PSResourceFile

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzBatchTask](./New-AzBatchTask.md)