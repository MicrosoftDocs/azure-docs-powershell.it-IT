---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: 23aa7e6df5aae820980551db445339ade34ac779
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002269"
---
# <span data-ttu-id="ad5e3-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="ad5e3-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="ad5e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad5e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5e3-103">Imposta l'autorizzazione di accesso pubblico su un contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="ad5e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad5e3-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ad5e3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ad5e3-105">DESCRIPTION</span></span>
<span data-ttu-id="ad5e3-106">Il cmdlet **Set-AzStorageContainerAcl** imposta l'autorizzazione di accesso pubblico sul contenitore di archiviazione specificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="ad5e3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad5e3-107">EXAMPLES</span></span>

### <span data-ttu-id="ad5e3-108">Esempio 1: Impostare l'ACL del contenitore di archiviazione di Azure in base al nome</span><span class="sxs-lookup"><span data-stu-id="ad5e3-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="ad5e3-109">Questo comando crea un contenitore senza accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="ad5e3-110">Esempio 2: Impostare l'ACL del contenitore di archiviazione di Azure usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="ad5e3-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="ad5e3-111">Questo comando recupera tutti i contenitori di archiviazione il cui nome inizia con contenitore e quindi passa il risultato alla pipeline per impostare le autorizzazioni per tutti su Accesso BLOB.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="ad5e3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad5e3-112">PARAMETERS</span></span>

### <span data-ttu-id="ad5e3-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ad5e3-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ad5e3-114">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ad5e3-115">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ad5e3-116">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ad5e3-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ad5e3-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ad5e3-118">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ad5e3-119">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ad5e3-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ad5e3-121">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ad5e3-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ad5e3-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ad5e3-123">-Context</span></span>
<span data-ttu-id="ad5e3-124">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ad5e3-125">È possibile crearla usando il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ad5e3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5e3-126">-DefaultProfile</span></span>
<span data-ttu-id="ad5e3-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad5e3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ad5e3-128">-Name</span></span>
<span data-ttu-id="ad5e3-129">Specifica il nome di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-129">Specifies a container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5e3-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad5e3-130">-PassThru</span></span>
<span data-ttu-id="ad5e3-131">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ad5e3-132">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ad5e3-133">-Permission</span><span class="sxs-lookup"><span data-stu-id="ad5e3-133">-Permission</span></span>
<span data-ttu-id="ad5e3-134">Specifica il livello di accesso pubblico al contenitore.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="ad5e3-135">Per impostazione predefinita, il contenitore e gli eventuali BLOB in esso contenuti sono accessibili solo al proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="ad5e3-136">Per concedere agli utenti anonimi le autorizzazioni di lettura per un contenitore e i relativi BLOB, è possibile impostare le autorizzazioni del contenitore per abilitare l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="ad5e3-137">Gli utenti anonimi possono leggere i BLOB in un contenitore disponibile pubblicamente senza autenticare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="ad5e3-138">I valori accettabili per questo parametro sono: --Container.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="ad5e3-139">Fornisce l'accesso in lettura completo a un contenitore e ai relativi BLOB.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="ad5e3-140">I client possono enumerare i BLOB nel contenitore tramite richiesta anonima, ma non possono enumerare i contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="ad5e3-141">--BLOB.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-141">--Blob.</span></span>
<span data-ttu-id="ad5e3-142">Fornisce l'accesso in lettura ai dati DEI BLOB in un contenitore tramite richiesta anonima, ma non fornisce l'accesso ai dati del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="ad5e3-143">I client non possono enumerare i BLOB nel contenitore usando una richiesta anonima.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="ad5e3-144">--Disattivato.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-144">--Off.</span></span>
<span data-ttu-id="ad5e3-145">Limita l'accesso solo al proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5e3-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ad5e3-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ad5e3-147">Specifica l'intervallo di timeout del lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ad5e3-148">Se prima dell'elaborazione della richiesta da parte del servizio è trascorso l'intervallo specificato, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="ad5e3-149">Timeout sul lato server per ogni richiesta.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="ad5e3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5e3-150">CommonParameters</span></span>
<span data-ttu-id="ad5e3-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad5e3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5e3-152">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad5e3-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5e3-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="ad5e3-153">INPUTS</span></span>

### <span data-ttu-id="ad5e3-154">System.String</span><span class="sxs-lookup"><span data-stu-id="ad5e3-154">System.String</span></span>

### <span data-ttu-id="ad5e3-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ad5e3-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ad5e3-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad5e3-156">OUTPUTS</span></span>

### <span data-ttu-id="ad5e3-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad5e3-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="ad5e3-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="ad5e3-158">NOTES</span></span>

## <span data-ttu-id="ad5e3-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad5e3-159">RELATED LINKS</span></span>

[<span data-ttu-id="ad5e3-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad5e3-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="ad5e3-161">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad5e3-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="ad5e3-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad5e3-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


