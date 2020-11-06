---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3b84deae0307114efa274cdfa6fc708d1b268ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507071"
---
# <span data-ttu-id="e05a1-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="e05a1-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="e05a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e05a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e05a1-103">Elenca le directory e i file per un percorso.</span><span class="sxs-lookup"><span data-stu-id="e05a1-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="e05a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e05a1-104">SYNTAX</span></span>

### <span data-ttu-id="e05a1-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e05a1-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="e05a1-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="e05a1-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e05a1-107">Directory</span><span class="sxs-lookup"><span data-stu-id="e05a1-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e05a1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e05a1-108">DESCRIPTION</span></span>
<span data-ttu-id="e05a1-109">Il cmdlet **Get-AzureStorageFile** elenca le directory e i file per la condivisione o la directory specificata.</span><span class="sxs-lookup"><span data-stu-id="e05a1-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="e05a1-110">Specifica il parametro *path* per ottenere un'istanza di una directory o di un file nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="e05a1-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>

<span data-ttu-id="e05a1-111">Questo cmdlet restituisce gli oggetti **AzureStorageFile** e **AzureStorageDirectory** .</span><span class="sxs-lookup"><span data-stu-id="e05a1-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="e05a1-112">Puoi usare la proprietà della **directory** per distinguere tra cartelle e file.</span><span class="sxs-lookup"><span data-stu-id="e05a1-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="e05a1-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e05a1-113">EXAMPLES</span></span>

### <span data-ttu-id="e05a1-114">Esempio 1: elencare le directory in una condivisione</span><span class="sxs-lookup"><span data-stu-id="e05a1-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "share1" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="e05a1-115">Questo comando elenca solo le directory della condivisione ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="e05a1-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="e05a1-116">Recupera prima entrambi i file e le directory, li passa all'operatore **where** usando l'operatore pipeline, quindi Elimina gli oggetti il cui tipo non è "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="e05a1-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="e05a1-117">Esempio 2: elencare una directory di file</span><span class="sxs-lookup"><span data-stu-id="e05a1-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="e05a1-118">Questo comando elenca i file e le cartelle nella directory ContosoWorkingFolder sotto la condivisione di ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="e05a1-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="e05a1-119">Ottiene prima di tutto l'istanza della directory e quindi lo pipeline al cmdlet **Get-AzureStorageFile** per elencare la directory.</span><span class="sxs-lookup"><span data-stu-id="e05a1-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="e05a1-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e05a1-120">PARAMETERS</span></span>

### <span data-ttu-id="e05a1-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e05a1-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e05a1-122">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="e05a1-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e05a1-123">Se la chiamata precedente non riesce entro l'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e05a1-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e05a1-124">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e05a1-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05a1-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e05a1-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e05a1-126">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="e05a1-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e05a1-127">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="e05a1-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e05a1-128">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="e05a1-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e05a1-129">Questo parametro può aiutare a mitigare i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="e05a1-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e05a1-130">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="e05a1-130">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05a1-131">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e05a1-131">-Context</span></span>
<span data-ttu-id="e05a1-132">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e05a1-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e05a1-133">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e05a1-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e05a1-134">-Directory</span><span class="sxs-lookup"><span data-stu-id="e05a1-134">-Directory</span></span>
<span data-ttu-id="e05a1-135">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="e05a1-135">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="e05a1-136">Questo cmdlet ottiene la cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e05a1-136">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="e05a1-137">Per ottenere una directory, usare il cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="e05a1-137">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="e05a1-138">Puoi anche usare il cmdlet **Get-AzureStorageFile** per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="e05a1-138">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e05a1-139">-Path</span><span class="sxs-lookup"><span data-stu-id="e05a1-139">-Path</span></span>
<span data-ttu-id="e05a1-140">Specifica il percorso di una cartella.</span><span class="sxs-lookup"><span data-stu-id="e05a1-140">Specifies the path of a folder.</span></span>

<span data-ttu-id="e05a1-141">Se si omette il parametro *path* , **Get-AzureStorageFile** elenca le directory e i file nella directory o nella condivisione file specificata.</span><span class="sxs-lookup"><span data-stu-id="e05a1-141">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="e05a1-142">Se si include il parametro *path* , **Get-AzureStorageFile** restituisce un'istanza di una directory o di un file nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="e05a1-142">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05a1-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e05a1-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e05a1-144">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="e05a1-144">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="e05a1-145">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e05a1-145">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05a1-146">-Condividi</span><span class="sxs-lookup"><span data-stu-id="e05a1-146">-Share</span></span>
<span data-ttu-id="e05a1-147">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="e05a1-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="e05a1-148">Questo cmdlet consente di ottenere un file o una directory dalla condivisione di file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e05a1-148">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="e05a1-149">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="e05a1-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="e05a1-150">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e05a1-150">This object contains the Storage context.</span></span>
<span data-ttu-id="e05a1-151">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="e05a1-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e05a1-152">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e05a1-152">-ShareName</span></span>
<span data-ttu-id="e05a1-153">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="e05a1-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="e05a1-154">Questo cmdlet consente di ottenere un file o una directory dalla condivisione di file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e05a1-154">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05a1-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05a1-155">CommonParameters</span></span>
<span data-ttu-id="e05a1-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05a1-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05a1-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05a1-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05a1-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e05a1-158">INPUTS</span></span>

## <span data-ttu-id="e05a1-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e05a1-159">OUTPUTS</span></span>

## <span data-ttu-id="e05a1-160">Note</span><span class="sxs-lookup"><span data-stu-id="e05a1-160">NOTES</span></span>

## <span data-ttu-id="e05a1-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e05a1-161">RELATED LINKS</span></span>

[<span data-ttu-id="e05a1-162">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e05a1-162">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="e05a1-163">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="e05a1-163">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="e05a1-164">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="e05a1-164">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="e05a1-165">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="e05a1-165">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="e05a1-166">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e05a1-166">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


