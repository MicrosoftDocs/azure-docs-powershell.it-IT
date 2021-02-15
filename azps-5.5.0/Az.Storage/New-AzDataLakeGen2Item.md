---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190871"
---
# New-AzDataLakeGen2Item

## SYNOPSIS
Creare un file o una directory in un filesystem.

## SINTASSI

### File (impostazione predefinita)
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Directory
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzDataLakeGen2Item** crea un file o una directory in un Filesystem in un account di archiviazione di Azure.
Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione. Questo tipo di account può essere creato eseguire il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalZone $true".

## ESEMPI

### Esempio 1: Creare una directory con autorizzazioni, Umask, proprietà e metadati specificati
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

Questo comando crea una directory con autorizzazioni, Umask, proprietà e metadati specificati

### Esempio 2: Creare(caricare) un file data lake da un file di origine locale e il cmdlet viene eseguito in background
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

Questo comando crea(carica) un file data lake da un file di origine locale e il cmdlet viene eseguito in background.

## PARAMETERS

### -AsJob
Eseguire il cmdlet in background

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
La quantità totale di attività sincronizzate simultanee. Il valore predefinito è 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Oggetto contesto archiviazione di Azure

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
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -Directory
Indica che il nuovo elemento è una directory e non un file.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Directory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileSystem
Nome filesystem

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

### -Force
Se il test viene superato, il nuovo elemento viene creato senza alcun prompt

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadata
Specifica i metadati per la directory o il file creato.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Percorso nel file system specificato che deve essere creato.
Può essere un file o una directory nel formato 'directory/file.txt' o 'directory1/directory2/'

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Permission
Imposta le autorizzazioni di accesso POSIX per il proprietario del file, il gruppo proprietario del file e altri utenti.
A ogni classe può essere concessa l'autorizzazione di lettura, scrittura o esecuzione.
Symbolic (rwxrw-rw-) è supportato.

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

### -Proprietà
Specifica le proprietà per la directory o il file creato. Le proprietà supportate per il file sono: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.
Le proprietà supportate per la directory sono: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Source
Specificare il percorso del file di origine locale che verrà caricato in un file GEN2 della finestra dei dati.

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Umask
Quando si crea un nuovo elemento e la directory padre non ha un ACL predefinito, la umask limita le autorizzazioni per la creazione del file o della directory.
L'autorizzazione risultante viene concessa da p & ^u, dove p è l'autorizzazione e l'utente è il umask.
Symbolic (rwxrw-rw-) è supportato.

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

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## OUTPUT

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item

## NOTE

## COLLEGAMENTI CORRELATI
