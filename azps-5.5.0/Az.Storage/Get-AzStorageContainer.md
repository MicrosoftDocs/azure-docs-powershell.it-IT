---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 0c26899b772fd21772b625cb057e141071767002
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178207"
---
# <span data-ttu-id="52c3b-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="52c3b-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="52c3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="52c3b-103">Elenca i contenitori di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52c3b-103">Lists the storage containers.</span></span>

## <span data-ttu-id="52c3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52c3b-104">SYNTAX</span></span>

### <span data-ttu-id="52c3b-105">ContainerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52c3b-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="52c3b-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="52c3b-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="52c3b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="52c3b-107">DESCRIPTION</span></span>
<span data-ttu-id="52c3b-108">Il cmdlet **Get-AzStorageContainer** elenca i contenitori di archiviazione associati all'account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="52c3b-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="52c3b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52c3b-109">EXAMPLES</span></span>

### <span data-ttu-id="52c3b-110">Esempio 1: Ottenere il BLOB di Archiviazione di Azure in base al nome</span><span class="sxs-lookup"><span data-stu-id="52c3b-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="52c3b-111">Questo esempio usa un carattere jolly per restituire un elenco di tutti i contenitori il cui nome inizia con contenitore.</span><span class="sxs-lookup"><span data-stu-id="52c3b-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="52c3b-112">Esempio 2: Ottenere il contenitore Archiviazione di Azure in base al prefisso del nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="52c3b-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="52c3b-113">Questo esempio usa il *parametro Prefix* per restituire un elenco di tutti i contenitori il cui nome inizia con contenitore.</span><span class="sxs-lookup"><span data-stu-id="52c3b-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="52c3b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52c3b-114">PARAMETERS</span></span>

### <span data-ttu-id="52c3b-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="52c3b-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="52c3b-116">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="52c3b-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="52c3b-117">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="52c3b-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="52c3b-118">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="52c3b-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="52c3b-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="52c3b-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="52c3b-120">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="52c3b-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="52c3b-121">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="52c3b-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="52c3b-122">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="52c3b-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="52c3b-123">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="52c3b-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="52c3b-124">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="52c3b-124">The default value is 10.</span></span>

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

### <span data-ttu-id="52c3b-125">-Context</span><span class="sxs-lookup"><span data-stu-id="52c3b-125">-Context</span></span>
<span data-ttu-id="52c3b-126">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52c3b-126">Specifies the storage context.</span></span>
<span data-ttu-id="52c3b-127">Per crearla, è possibile usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="52c3b-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="52c3b-128">Le autorizzazioni del contenitore non vengono recuperate quando si usa un contesto di archiviazione creato dal token di firma di accesso condiviso, perché le autorizzazioni del contenitore di query richiedono l'autorizzazione chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52c3b-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="52c3b-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="52c3b-129">-ContinuationToken</span></span>
<span data-ttu-id="52c3b-130">Specifica un token di continuazione per l'elenco BLOB.</span><span class="sxs-lookup"><span data-stu-id="52c3b-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52c3b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c3b-131">-DefaultProfile</span></span>
<span data-ttu-id="52c3b-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52c3b-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52c3b-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="52c3b-133">-MaxCount</span></span>
<span data-ttu-id="52c3b-134">Specifica il numero massimo di oggetti restituiti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52c3b-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="52c3b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="52c3b-135">-Name</span></span>
<span data-ttu-id="52c3b-136">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="52c3b-136">Specifies the container name.</span></span>
<span data-ttu-id="52c3b-137">Se il nome del contenitore è vuoto, il cmdlet elenca tutti i contenitori.</span><span class="sxs-lookup"><span data-stu-id="52c3b-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="52c3b-138">In caso contrario, elenca tutti i contenitori che corrispondono al nome specificato o al criterio del nome normale.</span><span class="sxs-lookup"><span data-stu-id="52c3b-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52c3b-139">-Prefix</span><span class="sxs-lookup"><span data-stu-id="52c3b-139">-Prefix</span></span>
<span data-ttu-id="52c3b-140">Specifica un prefisso usato nel nome del contenitore o dei contenitori da ottenere.</span><span class="sxs-lookup"><span data-stu-id="52c3b-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="52c3b-141">È possibile usarla per trovare tutti i contenitori che iniziano con la stessa stringa, ad esempio "my" o "test".</span><span class="sxs-lookup"><span data-stu-id="52c3b-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52c3b-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="52c3b-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="52c3b-143">Specifica l'intervallo di timeout del lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="52c3b-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="52c3b-144">Se prima dell'elaborazione della richiesta da parte del servizio è trascorso l'intervallo specificato, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="52c3b-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="52c3b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c3b-145">CommonParameters</span></span>
<span data-ttu-id="52c3b-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52c3b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c3b-147">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52c3b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c3b-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="52c3b-148">INPUTS</span></span>

### <span data-ttu-id="52c3b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="52c3b-149">System.String</span></span>

### <span data-ttu-id="52c3b-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="52c3b-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="52c3b-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52c3b-151">OUTPUTS</span></span>

### <span data-ttu-id="52c3b-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="52c3b-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="52c3b-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="52c3b-153">NOTES</span></span>

## <span data-ttu-id="52c3b-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52c3b-154">RELATED LINKS</span></span>

[<span data-ttu-id="52c3b-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="52c3b-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="52c3b-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="52c3b-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="52c3b-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="52c3b-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


