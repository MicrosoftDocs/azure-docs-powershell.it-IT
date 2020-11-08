---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201596"
---
# New-AzBatchResourceFile

## Sinossi
Crea un file di risorse per l'utilizzo `New-AzBatchTask` .

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

## Descrizione
Crea un file di risorse per l'utilizzo `New-AzBatchTask` .

## ESEMPI

### Esempio 1: creare un file di risorse da un URL HTTP che punta a un singolo file
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Crea un `PSResourceFile` riferimento a un URL http.

### Esempio 2: creare un file di risorse da un URL del contenitore di archiviazione di Azure
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Crea un `PSResourceFile` riferimento a un URL del contenitore di archiviazione di Azure. Tutti i file nel contenitore verranno scaricati nella cartella specificata.

### Esempio 3: creare un file di risorse da un nome di contenitore di archiviazione automatico
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Crea un `PSResourceFile` riferimento a un nome di contenitore di archiviazione automatico. Tutti i file nel contenitore verranno scaricati nella cartella specificata.

## PARAMETRI

### -AutoStorageContainerName
Nome del contenitore di archiviazione nell'account di archiviazione automatica.

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
Ottiene il prefisso BLOB da usare per il download di BLOB da un contenitore di archiviazione di Azure.
Verranno scaricati solo i BLOB i cui nomi iniziano con il prefisso specificato.
Questo prefisso può essere un nome di file parziale o una sottodirectory.
Se non si specifica un prefisso, verranno scaricati tutti i file nel contenitore.

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
Posizione del nodo Compute a cui scaricare i file, relativo alla directory di lavoro dell'attività. Se il parametro HttpUrl è specificato, il filePath è obbligatorio e descrive il percorso in cui verrà scaricato il file, incluso il nome del documento. In caso contrario, se sono specificati i parametri AutoStorageContainerName o StorageContainerUrl, filePath è facoltativo ed è la directory in cui scaricare i file. Nel caso in cui FilePath viene usato come directory, qualsiasi struttura di directory già associata ai dati di input verrà mantenuta integralmente e accodata alla directory FilePath specificata. Il percorso relativo specificato non può uscire dalla directory di lavoro dell'attività, ad esempio usando "..".

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
Se l'URL è archiviazione BLOB di Azure, deve essere leggibile usando l'accesso anonimo; in altri casi, il servizio batch non presenta alcuna credenziale durante il download del BLOB.
Esistono due modi per ottenere un URL di questo tipo per un BLOB in Azure Storage: includere una firma di accesso condiviso (SAS) che concede le autorizzazioni di lettura per il BLOB o imposta l'ACL per il BLOB o il relativo contenitore per consentire l'accesso pubblico.

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
URL del contenitore di BLOB nell'archiviazione BLOB di Azure.
Questo URL deve essere leggibile ed elencabile usando l'accesso anonimo; il servizio batch non presenta credenziali durante il download di BLOB dal contenitore.
Esistono due modi per ottenere un URL di questo tipo per un contenitore in Azure Storage: includere una firma di accesso condiviso (SAS) che concede le autorizzazioni di lettura per il contenitore o imposta l'ACL per il contenitore per consentire l'accesso pubblico.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Batch. Models. PSResourceFile

## Note

## COLLEGAMENTI CORRELATI

[New-AzBatchTask](./New-AzBatchTask.md)