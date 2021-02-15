---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195814"
---
# <span data-ttu-id="6aec5-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="6aec5-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="6aec5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aec5-102">SYNOPSIS</span></span>
<span data-ttu-id="6aec5-103">Applica una semplice istruzione Structured Query Language (SQL) ai contenuti di un BLOB e salva solo il sottoinsieme di dati in cui viene eseguita la query in un file locale.</span><span class="sxs-lookup"><span data-stu-id="6aec5-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="6aec5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6aec5-104">SYNTAX</span></span>

### <span data-ttu-id="6aec5-105">NamePipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6aec5-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6aec5-106">BLOBPipeline</span><span class="sxs-lookup"><span data-stu-id="6aec5-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6aec5-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="6aec5-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6aec5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6aec5-108">DESCRIPTION</span></span>
<span data-ttu-id="6aec5-109">Il cmdlet **Get-AzStorageBlobQueryResult** applica una semplice istruzione Structured Query Language (SQL) sui contenuti di un BLOB e salva il sottoinsieme dei dati in query in un file locale.</span><span class="sxs-lookup"><span data-stu-id="6aec5-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="6aec5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6aec5-110">EXAMPLES</span></span>

### <span data-ttu-id="6aec5-111">Esempio 1: Eseguire query su un BLOB</span><span class="sxs-lookup"><span data-stu-id="6aec5-111">Example 1: Query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="6aec5-112">Questo comando esegue una query in ccn di un BLOB con configurazione di input come CSV e configurazione di output come json e salva l'output nel file locale "c:\resultfile.js".</span><span class="sxs-lookup"><span data-stu-id="6aec5-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="6aec5-113">Esempio 2: Eseguire una query su uno snapshot BLOB</span><span class="sxs-lookup"><span data-stu-id="6aec5-113">Example 2: Query a blob snapshot</span></span>
```powershell
PS C:\> $blob = Get-AzStorageBlob -Container $containerName -Blob $blobName -SnapshotTime "2020-07-29T11:08:21.1097874Z" -Context $ctx

PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE _1 LIKE '1%%'"

PS C:\> $result = $blob | Get-AzStorageBlobQueryResult -QueryString $queryString -ResultFile $localFilePath -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
   187064971            1 {ParseError}  



PS C:\> $result.BlobQueryError

Name       Description                                                   IsFatal Position
----       -----------                                                   ------- --------
ParseError Unexpected token '1' at [byte: 3077737]. Expecting token ','.    True  7270632
```

<span data-ttu-id="6aec5-114">Questo comando ottiene prima di tutto un oggetto BLOB per lo snapshot BLOB, quindi esegue una query per lo snapshot BLOB e mostra il risultato include l'errore della query.</span><span class="sxs-lookup"><span data-stu-id="6aec5-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="6aec5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6aec5-115">PARAMETERS</span></span>

### <span data-ttu-id="6aec5-116">-BLOB</span><span class="sxs-lookup"><span data-stu-id="6aec5-116">-Blob</span></span>
<span data-ttu-id="6aec5-117">Nome BLOB</span><span class="sxs-lookup"><span data-stu-id="6aec5-117">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec5-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6aec5-118">-BlobBaseClient</span></span>
<span data-ttu-id="6aec5-119">Oggetto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6aec5-119">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aec5-120">-BLOBContainerClient</span><span class="sxs-lookup"><span data-stu-id="6aec5-120">-BlobContainerClient</span></span>
<span data-ttu-id="6aec5-121">Oggetto BLOBContainerClient</span><span class="sxs-lookup"><span data-stu-id="6aec5-121">BlobContainerClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.BlobContainerClient
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aec5-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6aec5-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6aec5-123">Il tempo massimo di esecuzione sul lato client per ogni richiesta in secondi.</span><span class="sxs-lookup"><span data-stu-id="6aec5-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="6aec5-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6aec5-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6aec5-125">La quantità totale di attività sincronizzate simultanee.</span><span class="sxs-lookup"><span data-stu-id="6aec5-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="6aec5-126">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="6aec5-126">The default value is 10.</span></span>

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

### <span data-ttu-id="6aec5-127">-Container</span><span class="sxs-lookup"><span data-stu-id="6aec5-127">-Container</span></span>
<span data-ttu-id="6aec5-128">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="6aec5-128">Container name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec5-129">-Context</span><span class="sxs-lookup"><span data-stu-id="6aec5-129">-Context</span></span>
<span data-ttu-id="6aec5-130">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="6aec5-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="6aec5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aec5-131">-DefaultProfile</span></span>
<span data-ttu-id="6aec5-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6aec5-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aec5-133">-Force</span><span class="sxs-lookup"><span data-stu-id="6aec5-133">-Force</span></span>
<span data-ttu-id="6aec5-134">Forzare la sovrascrittura del file esistente.</span><span class="sxs-lookup"><span data-stu-id="6aec5-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="6aec5-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="6aec5-135">-InputTextConfiguration</span></span>
<span data-ttu-id="6aec5-136">Configurazione usata per gestire il testo di input della query.</span><span class="sxs-lookup"><span data-stu-id="6aec5-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="6aec5-137">Creare un oggetto configurazione con New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="6aec5-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec5-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="6aec5-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="6aec5-139">Configurazione usata per gestire il testo di output della query.</span><span class="sxs-lookup"><span data-stu-id="6aec5-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="6aec5-140">Creare un oggetto configurazione con New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="6aec5-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec5-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6aec5-141">-PassThru</span></span>
<span data-ttu-id="6aec5-142">Restituisce se la query del BLOB specificato viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="6aec5-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="6aec5-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="6aec5-143">-QueryString</span></span>
<span data-ttu-id="6aec5-144">Stringa di query, vedere altri dettagli in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="6aec5-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec5-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="6aec5-145">-ResultFile</span></span>
<span data-ttu-id="6aec5-146">Percorso file locale per salvare il risultato della query.</span><span class="sxs-lookup"><span data-stu-id="6aec5-146">Local file path to save the query result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec5-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6aec5-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6aec5-148">Timeout del server in ogni richiesta in secondi.</span><span class="sxs-lookup"><span data-stu-id="6aec5-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="6aec5-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="6aec5-149">-SnapshotTime</span></span>
<span data-ttu-id="6aec5-150">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="6aec5-150">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec5-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="6aec5-151">-VersionId</span></span>
<span data-ttu-id="6aec5-152">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="6aec5-152">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec5-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6aec5-153">-Confirm</span></span>
<span data-ttu-id="6aec5-154">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aec5-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aec5-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aec5-155">-WhatIf</span></span>
<span data-ttu-id="6aec5-156">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6aec5-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aec5-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6aec5-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aec5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aec5-158">CommonParameters</span></span>
<span data-ttu-id="6aec5-159">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aec5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aec5-160">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aec5-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aec5-161">INPUT</span><span class="sxs-lookup"><span data-stu-id="6aec5-161">INPUTS</span></span>

### <span data-ttu-id="6aec5-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6aec5-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="6aec5-163">Azure.Storage.Blobs.BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="6aec5-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="6aec5-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6aec5-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6aec5-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6aec5-165">OUTPUTS</span></span>

### <span data-ttu-id="6aec5-166">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6aec5-166">System.Boolean</span></span>

## <span data-ttu-id="6aec5-167">NOTE</span><span class="sxs-lookup"><span data-stu-id="6aec5-167">NOTES</span></span>

## <span data-ttu-id="6aec5-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6aec5-168">RELATED LINKS</span></span>
