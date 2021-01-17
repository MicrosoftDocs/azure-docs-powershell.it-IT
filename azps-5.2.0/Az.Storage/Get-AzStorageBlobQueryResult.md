---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349675"
---
# <span data-ttu-id="59265-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="59265-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="59265-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59265-102">SYNOPSIS</span></span>
<span data-ttu-id="59265-103">Applica un'istruzione SQL (Structured Query Language) semplice nel contenuto di un BLOB e salva solo il sottoinsieme interrogato dei dati in un file locale.</span><span class="sxs-lookup"><span data-stu-id="59265-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="59265-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59265-104">SYNTAX</span></span>

### <span data-ttu-id="59265-105">NamePipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59265-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59265-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="59265-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59265-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="59265-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59265-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59265-108">DESCRIPTION</span></span>
<span data-ttu-id="59265-109">Il cmdlet **Get-AzStorageBlobQueryResult** applica una semplice istruzione SQL (Structured Query Language) sul contenuto di un BLOB e salva il sottoinsieme interrogato dei dati in un file locale.</span><span class="sxs-lookup"><span data-stu-id="59265-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="59265-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59265-110">EXAMPLES</span></span>

### <span data-ttu-id="59265-111">Esempio 1: eseguire una query su un BLOB</span><span class="sxs-lookup"><span data-stu-id="59265-111">Example 1: Query a blob</span></span>
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

<span data-ttu-id="59265-112">Questo comando esegue una query su un BLOB succsssfully con la configurazione di input come CSV e la configurazione di output come JSON e salva l'output nel file locale "c:\resultfile.jsattivato".</span><span class="sxs-lookup"><span data-stu-id="59265-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="59265-113">Esempio 2: eseguire una query su uno snapshot BLOB</span><span class="sxs-lookup"><span data-stu-id="59265-113">Example 2: Query a blob snapshot</span></span>
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

<span data-ttu-id="59265-114">Questo comando ottiene prima di tutto un oggetto BLOB per lo snapshot BLOB, quindi esegue una query nello snapshot BLOB e Mostra il risultato include l'errore della query.</span><span class="sxs-lookup"><span data-stu-id="59265-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="59265-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59265-115">PARAMETERS</span></span>

### <span data-ttu-id="59265-116">-BLOB</span><span class="sxs-lookup"><span data-stu-id="59265-116">-Blob</span></span>
<span data-ttu-id="59265-117">Nome BLOB</span><span class="sxs-lookup"><span data-stu-id="59265-117">Blob name</span></span>

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

### <span data-ttu-id="59265-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="59265-118">-BlobBaseClient</span></span>
<span data-ttu-id="59265-119">Oggetto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="59265-119">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="59265-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="59265-120">-BlobContainerClient</span></span>
<span data-ttu-id="59265-121">Oggetto BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="59265-121">BlobContainerClient Object</span></span>

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

### <span data-ttu-id="59265-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="59265-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="59265-123">Il tempo di esecuzione massimo lato client per ogni richiesta in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="59265-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="59265-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="59265-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="59265-125">La quantità totale di attività asincrone simultanee.</span><span class="sxs-lookup"><span data-stu-id="59265-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="59265-126">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="59265-126">The default value is 10.</span></span>

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

### <span data-ttu-id="59265-127">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="59265-127">-Container</span></span>
<span data-ttu-id="59265-128">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="59265-128">Container name</span></span>

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

### <span data-ttu-id="59265-129">-Contesto</span><span class="sxs-lookup"><span data-stu-id="59265-129">-Context</span></span>
<span data-ttu-id="59265-130">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="59265-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="59265-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59265-131">-DefaultProfile</span></span>
<span data-ttu-id="59265-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59265-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59265-133">-Force</span><span class="sxs-lookup"><span data-stu-id="59265-133">-Force</span></span>
<span data-ttu-id="59265-134">Forza per sovrascrivere il file esistente.</span><span class="sxs-lookup"><span data-stu-id="59265-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="59265-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="59265-135">-InputTextConfiguration</span></span>
<span data-ttu-id="59265-136">La configurazione usata per gestire il testo dell'input della query.</span><span class="sxs-lookup"><span data-stu-id="59265-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="59265-137">Creare l'oggetto di configurazione con New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="59265-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="59265-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="59265-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="59265-139">La configurazione usata per gestire il testo dell'output della query.</span><span class="sxs-lookup"><span data-stu-id="59265-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="59265-140">Creare l'oggetto di configurazione con New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="59265-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="59265-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59265-141">-PassThru</span></span>
<span data-ttu-id="59265-142">Restituirà se il blob specificato viene interrogato correttamente.</span><span class="sxs-lookup"><span data-stu-id="59265-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="59265-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="59265-143">-QueryString</span></span>
<span data-ttu-id="59265-144">Stringa di query, vedere altri dettagli in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="59265-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

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

### <span data-ttu-id="59265-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="59265-145">-ResultFile</span></span>
<span data-ttu-id="59265-146">Percorso file locale per salvare il risultato della query.</span><span class="sxs-lookup"><span data-stu-id="59265-146">Local file path to save the query result.</span></span>

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

### <span data-ttu-id="59265-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="59265-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="59265-148">Timeout del server per ogni richiesta in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="59265-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="59265-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="59265-149">-SnapshotTime</span></span>
<span data-ttu-id="59265-150">BLOB SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="59265-150">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="59265-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="59265-151">-VersionId</span></span>
<span data-ttu-id="59265-152">BLOB VersionId</span><span class="sxs-lookup"><span data-stu-id="59265-152">Blob VersionId</span></span>

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

### <span data-ttu-id="59265-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59265-153">-Confirm</span></span>
<span data-ttu-id="59265-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59265-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59265-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59265-155">-WhatIf</span></span>
<span data-ttu-id="59265-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59265-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59265-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59265-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59265-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59265-158">CommonParameters</span></span>
<span data-ttu-id="59265-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59265-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59265-160">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59265-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59265-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59265-161">INPUTS</span></span>

### <span data-ttu-id="59265-162">Azure. storage. Blobs. Specialized. BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="59265-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="59265-163">Azure. storage. Blobs. BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="59265-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="59265-164">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="59265-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="59265-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59265-165">OUTPUTS</span></span>

### <span data-ttu-id="59265-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59265-166">System.Boolean</span></span>

## <span data-ttu-id="59265-167">Note</span><span class="sxs-lookup"><span data-stu-id="59265-167">NOTES</span></span>

## <span data-ttu-id="59265-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59265-168">RELATED LINKS</span></span>
