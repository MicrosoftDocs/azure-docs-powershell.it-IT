---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 5d73923dd3de630673d9228461397ec1789bd268
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857878"
---
# <span data-ttu-id="cfcae-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cfcae-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="cfcae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cfcae-102">SYNOPSIS</span></span>
<span data-ttu-id="cfcae-103">Elenca le directory e i file per un percorso.</span><span class="sxs-lookup"><span data-stu-id="cfcae-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="cfcae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfcae-104">SYNTAX</span></span>

### <span data-ttu-id="cfcae-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cfcae-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="cfcae-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="cfcae-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="cfcae-107">Directory</span><span class="sxs-lookup"><span data-stu-id="cfcae-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfcae-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfcae-108">DESCRIPTION</span></span>
<span data-ttu-id="cfcae-109">Il cmdlet **Get-AzStorageFile** elenca le directory e i file per la condivisione o la directory specificata.</span><span class="sxs-lookup"><span data-stu-id="cfcae-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="cfcae-110">Specifica il parametro *path* per ottenere un'istanza di una directory o di un file nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="cfcae-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="cfcae-111">Questo cmdlet restituisce gli oggetti **AzureStorageFile** e **AzureStorageDirectory** .</span><span class="sxs-lookup"><span data-stu-id="cfcae-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="cfcae-112">Puoi usare la proprietà della **directory** per distinguere tra cartelle e file.</span><span class="sxs-lookup"><span data-stu-id="cfcae-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="cfcae-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfcae-113">EXAMPLES</span></span>

### <span data-ttu-id="cfcae-114">Esempio 1: elencare le directory in una condivisione</span><span class="sxs-lookup"><span data-stu-id="cfcae-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="cfcae-115">Questo comando elenca solo le directory della condivisione ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="cfcae-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="cfcae-116">Recupera prima entrambi i file e le directory, li passa all'operatore **where** usando l'operatore pipeline, quindi Elimina gli oggetti il cui tipo non è "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="cfcae-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="cfcae-117">Esempio 2: elencare una directory di file</span><span class="sxs-lookup"><span data-stu-id="cfcae-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="cfcae-118">Questo comando elenca i file e le cartelle nella directory ContosoWorkingFolder sotto la condivisione di ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="cfcae-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="cfcae-119">Ottiene prima di tutto l'istanza della directory e quindi lo pipeline al cmdlet **Get-AzStorageFile** per elencare la directory.</span><span class="sxs-lookup"><span data-stu-id="cfcae-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="cfcae-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cfcae-120">PARAMETERS</span></span>

### <span data-ttu-id="cfcae-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cfcae-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cfcae-122">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="cfcae-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cfcae-123">Se la chiamata precedente non riesce entro l'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="cfcae-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cfcae-124">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="cfcae-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cfcae-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cfcae-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cfcae-126">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="cfcae-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cfcae-127">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="cfcae-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cfcae-128">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="cfcae-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cfcae-129">Questo parametro può aiutare a mitigare i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="cfcae-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cfcae-130">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="cfcae-130">The default value is 10.</span></span>

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

### <span data-ttu-id="cfcae-131">-Contesto</span><span class="sxs-lookup"><span data-stu-id="cfcae-131">-Context</span></span>
<span data-ttu-id="cfcae-132">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cfcae-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="cfcae-133">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="cfcae-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cfcae-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfcae-134">-DefaultProfile</span></span>
<span data-ttu-id="cfcae-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfcae-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfcae-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="cfcae-136">-Directory</span></span>
<span data-ttu-id="cfcae-137">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="cfcae-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="cfcae-138">Questo cmdlet ottiene la cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cfcae-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="cfcae-139">Per ottenere una directory, usare il cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="cfcae-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="cfcae-140">Puoi anche usare il cmdlet **Get-AzStorageFile** per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="cfcae-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcae-141">-Path</span><span class="sxs-lookup"><span data-stu-id="cfcae-141">-Path</span></span>
<span data-ttu-id="cfcae-142">Specifica il percorso di una cartella.</span><span class="sxs-lookup"><span data-stu-id="cfcae-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="cfcae-143">Se si omette il parametro *path* , **Get-AzStorageFile** elenca le directory e i file nella directory o nella condivisione file specificata.</span><span class="sxs-lookup"><span data-stu-id="cfcae-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="cfcae-144">Se si include il parametro *path* , **Get-AzStorageFile** restituisce un'istanza di una directory o di un file nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="cfcae-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfcae-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cfcae-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cfcae-146">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="cfcae-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="cfcae-147">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="cfcae-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="cfcae-148">-Condividi</span><span class="sxs-lookup"><span data-stu-id="cfcae-148">-Share</span></span>
<span data-ttu-id="cfcae-149">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="cfcae-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="cfcae-150">Questo cmdlet consente di ottenere un file o una directory dalla condivisione di file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cfcae-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="cfcae-151">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="cfcae-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="cfcae-152">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cfcae-152">This object contains the Storage context.</span></span>
<span data-ttu-id="cfcae-153">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="cfcae-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcae-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cfcae-154">-ShareName</span></span>
<span data-ttu-id="cfcae-155">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="cfcae-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="cfcae-156">Questo cmdlet consente di ottenere un file o una directory dalla condivisione di file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cfcae-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="cfcae-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfcae-157">CommonParameters</span></span>
<span data-ttu-id="cfcae-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfcae-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfcae-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfcae-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfcae-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cfcae-160">INPUTS</span></span>

### <span data-ttu-id="cfcae-161">Microsoft. Azure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="cfcae-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="cfcae-162">Microsoft. Azure. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="cfcae-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="cfcae-163">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cfcae-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cfcae-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfcae-164">OUTPUTS</span></span>

### <span data-ttu-id="cfcae-165">Microsoft. Azure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="cfcae-165">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="cfcae-166">Note</span><span class="sxs-lookup"><span data-stu-id="cfcae-166">NOTES</span></span>

## <span data-ttu-id="cfcae-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfcae-167">RELATED LINKS</span></span>

[<span data-ttu-id="cfcae-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cfcae-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="cfcae-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="cfcae-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="cfcae-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="cfcae-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="cfcae-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cfcae-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="cfcae-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cfcae-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


