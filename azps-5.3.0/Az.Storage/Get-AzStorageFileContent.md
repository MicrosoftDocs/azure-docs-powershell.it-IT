---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374037"
---
# Get-AzStorageFileContent

## Sinossi
Scarica il contenuto di un file.

## SINTASSI

### ShareName (impostazione predefinita)
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### Condividi
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Directory
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### File
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzStorageFileContent** Scarica il contenuto di un file e lo salva in una destinazione specificata.
Questo cmdlet non restituisce il contenuto del file.

## ESEMPI

### Esempio 1: scaricare un file da una cartella
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Questo comando consente di scaricare un file denominato CurrentDataFile nella cartella ContosoWorkingFolder della condivisione file ContosoShare06 nella cartella corrente.

### Esempio 2: Scarica i file in condivisione file di esempio
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

In questo esempio vengono scaricati i file in condivisione file di esempio

### Esempio 3: scaricare un file di Azure in un file locale e Perserve le proprietà SMB di file di Azure (file Attributtes, ora di creazione del file, ultima ora di scrittura) nel file locale.
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

Questo esempio consente di scaricare un file di Azure in un file locale e di perserves le proprietà SMB di file di Azure (file Attributtes, ora di creazione del file, ultima volta che si scrive) nel file locale.

## PARAMETRI

### -AsJob
Esegui cmdlet in background.

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

### -CheckMd5
Specifica se controllare la somma MD5 per il file scaricato.

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

### -ClientTimeoutPerRequest
Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio. Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta. Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Specifica le chiamate di rete simultanee massime. Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee. Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base. Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo. Il valore predefinito è 10.

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

### -Contesto
Specifica un contesto di archiviazione di Azure. Per ottenere un contesto, usare il cmdlet New-AzStorageContext.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
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

### -Destinazione
Specifica il percorso di destinazione.
Questo cmdlet Scarica il contenuto del file nella posizione specificata da questo parametro.
Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.
Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.
Se si specifica un percorso di un file esistente e non si specifica la *forza*, il cmdlet richiede prima di continuare.
Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Directory
Specifica una cartella come oggetto **CloudFileDirectory** .
Questo cmdlet consente di ottenere contenuto per un file nella cartella specificata da questo parametro.
Per ottenere una directory, usare il cmdlet New-AzStorageDirectory.
Puoi anche usare il cmdlet Get-AzStorageFile per ottenere una directory.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -File
Specifica un file come oggetto **CloudFile** .
Questo cmdlet ottiene il file specificato da questo parametro.
Per ottenere un oggetto **CloudFile** , usa il cmdlet Get-AzStorageFile.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Force
Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.
Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.
Se si specifica un percorso di un file esistente e non si specifica la *forza*, il cmdlet richiede prima di continuare.
Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.

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

### -PassThru
Indica che questo cmdlet restituisce l'oggetto **AzureStorageFile** che esegue il download.

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

### -Path
Specifica il percorso di un file.
Questo cmdlet consente di ottenere il contenuto del file specificato da questo parametro.
Se il file non esiste, questo cmdlet restituisce un errore.

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreserveSMBAttribute
Mantieni le proprietà SMB del file di origine (file Attributtes, ora di creazione del file, ultima ora di scrittura) nel file di destinazione. Questo parametro è disponibile solo in Windows.

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

### -ServerTimeoutPerRequest
Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta. Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Condividi
Specifica un oggetto **CloudFileShare** .
Questo cmdlet Scarica il contenuto del file nel parametro Share this specificato.
Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzStorageShare.
Questo oggetto contiene il contesto di archiviazione.
Se specifichi questo parametro, non specificare il parametro *context* .

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ShareName
Specifica il nome della condivisione file.
Questo cmdlet Scarica il contenuto del file nel parametro Share this specificato.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. storage. file. CloudFileShare

### Microsoft. Azure. storage. file. CloudFileDirectory

### Microsoft. Azure. storage. file. CloudFile

### Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext

## OUTPUT

### Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageFile

## Note

## COLLEGAMENTI CORRELATI

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


