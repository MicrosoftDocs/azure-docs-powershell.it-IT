---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: e61171faba3661ad1d518641655ad87f06771ae6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997092"
---
# <span data-ttu-id="33e5d-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="33e5d-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="33e5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="33e5d-103">Elenca le directory e i file per un percorso.</span><span class="sxs-lookup"><span data-stu-id="33e5d-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="33e5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33e5d-104">SYNTAX</span></span>

### <span data-ttu-id="33e5d-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33e5d-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="33e5d-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="33e5d-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="33e5d-107">Directory</span><span class="sxs-lookup"><span data-stu-id="33e5d-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="33e5d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="33e5d-108">DESCRIPTION</span></span>
<span data-ttu-id="33e5d-109">Il **cmdlet Get-AzStorageFile** elenca le directory e i file per la condivisione o la directory specificata.</span><span class="sxs-lookup"><span data-stu-id="33e5d-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="33e5d-110">Specificare il *parametro Path* per ottenere un'istanza di una directory o di un file nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="33e5d-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="33e5d-111">Questo cmdlet restituisce gli **oggetti AzureStorageFile** **e AzureStorageDirectory.**</span><span class="sxs-lookup"><span data-stu-id="33e5d-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="33e5d-112">È possibile usare la **proprietà IsDirectory** per distinguere tra cartelle e file.</span><span class="sxs-lookup"><span data-stu-id="33e5d-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="33e5d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33e5d-113">EXAMPLES</span></span>

### <span data-ttu-id="33e5d-114">Esempio 1: Elencare le directory in una condivisione</span><span class="sxs-lookup"><span data-stu-id="33e5d-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="33e5d-115">Questo comando elenca solo le directory nella condivisione ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="33e5d-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="33e5d-116">Recupera prima i file e le directory, li passa all'operatore **where** usando l'operatore della pipeline, quindi elimina tutti gli oggetti il cui tipo non è "AzureStorageFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="33e5d-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="33e5d-117">Esempio 2: Elencare una directory file</span><span class="sxs-lookup"><span data-stu-id="33e5d-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="33e5d-118">Questo comando elenca i file e le cartelle nella directory ContosoWorkingFolder nella condivisione ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="33e5d-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="33e5d-119">Ottiene prima l'istanza della directory, quindi la pipeline al cmdlet **Get-AzStorageFile** per elencare la directory.</span><span class="sxs-lookup"><span data-stu-id="33e5d-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="33e5d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33e5d-120">PARAMETERS</span></span>

### <span data-ttu-id="33e5d-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="33e5d-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="33e5d-122">Specifica l'intervallo di timeout del lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="33e5d-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="33e5d-123">Se la chiamata precedente non riesce entro l'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="33e5d-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="33e5d-124">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="33e5d-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="33e5d-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="33e5d-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="33e5d-126">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="33e5d-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="33e5d-127">È possibile usare questo parametro per limitare la simultaneità per limitare l'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="33e5d-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="33e5d-128">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="33e5d-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="33e5d-129">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="33e5d-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="33e5d-130">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="33e5d-130">The default value is 10.</span></span>

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

### <span data-ttu-id="33e5d-131">-Context</span><span class="sxs-lookup"><span data-stu-id="33e5d-131">-Context</span></span>
<span data-ttu-id="33e5d-132">Specifica un contesto di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="33e5d-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="33e5d-133">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33e5d-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="33e5d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e5d-134">-DefaultProfile</span></span>
<span data-ttu-id="33e5d-135">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33e5d-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33e5d-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="33e5d-136">-Directory</span></span>
<span data-ttu-id="33e5d-137">Specifica una cartella come oggetto **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="33e5d-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="33e5d-138">Questo cmdlet ottiene la cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="33e5d-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="33e5d-139">Per ottenere una directory, usare il cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="33e5d-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="33e5d-140">È anche possibile usare il cmdlet **Get-AzStorageFile** per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="33e5d-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="33e5d-141">-Path</span><span class="sxs-lookup"><span data-stu-id="33e5d-141">-Path</span></span>
<span data-ttu-id="33e5d-142">Specifica il percorso di una cartella.</span><span class="sxs-lookup"><span data-stu-id="33e5d-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="33e5d-143">Se si omette il *parametro Path,* **Get-AzStorageFile** elenca le directory e i file nella directory o nella condivisione file specificata.</span><span class="sxs-lookup"><span data-stu-id="33e5d-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="33e5d-144">Se si include il *parametro Path,* **Get-AzStorageFile** restituisce un'istanza di una directory o di un file nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="33e5d-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

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

### <span data-ttu-id="33e5d-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="33e5d-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="33e5d-146">Specifica l'intervallo di timeout sul lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="33e5d-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="33e5d-147">Se prima dell'elaborazione della richiesta da parte del servizio è trascorso l'intervallo specificato, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="33e5d-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="33e5d-148">-Condividi</span><span class="sxs-lookup"><span data-stu-id="33e5d-148">-Share</span></span>
<span data-ttu-id="33e5d-149">Specifica un **oggetto CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="33e5d-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="33e5d-150">Questo cmdlet ottiene un file o una directory dalla condivisione file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="33e5d-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="33e5d-151">Per ottenere un **oggetto CloudFileShare,** usare il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="33e5d-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="33e5d-152">Questo oggetto contiene il contesto Archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33e5d-152">This object contains the Storage context.</span></span>
<span data-ttu-id="33e5d-153">Se si specifica questo parametro, non specificare il *parametro Context.*</span><span class="sxs-lookup"><span data-stu-id="33e5d-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="33e5d-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="33e5d-154">-ShareName</span></span>
<span data-ttu-id="33e5d-155">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="33e5d-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="33e5d-156">Questo cmdlet ottiene un file o una directory dalla condivisione file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="33e5d-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="33e5d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e5d-157">CommonParameters</span></span>
<span data-ttu-id="33e5d-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33e5d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e5d-159">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33e5d-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e5d-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="33e5d-160">INPUTS</span></span>

### <span data-ttu-id="33e5d-161">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="33e5d-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="33e5d-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="33e5d-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="33e5d-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="33e5d-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="33e5d-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33e5d-164">OUTPUTS</span></span>

### <span data-ttu-id="33e5d-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="33e5d-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="33e5d-166">NOTE</span><span class="sxs-lookup"><span data-stu-id="33e5d-166">NOTES</span></span>

## <span data-ttu-id="33e5d-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33e5d-167">RELATED LINKS</span></span>

[<span data-ttu-id="33e5d-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="33e5d-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="33e5d-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="33e5d-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="33e5d-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="33e5d-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="33e5d-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="33e5d-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="33e5d-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="33e5d-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


