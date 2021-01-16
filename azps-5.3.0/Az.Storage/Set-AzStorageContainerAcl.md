---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: a23df1d7f6af188557c8e949f116e3dd12351c49
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376151"
---
# <span data-ttu-id="0ebbb-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="0ebbb-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="0ebbb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ebbb-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebbb-103">Imposta l'autorizzazione di accesso pubblico per un contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="0ebbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ebbb-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0ebbb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ebbb-105">DESCRIPTION</span></span>
<span data-ttu-id="0ebbb-106">Il cmdlet **set-AzStorageContainerAcl** imposta l'autorizzazione di accesso pubblico sul contenitore di archiviazione specificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="0ebbb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ebbb-107">EXAMPLES</span></span>

### <span data-ttu-id="0ebbb-108">Esempio 1: impostare l'ACL del contenitore di archiviazione di Azure per nome</span><span class="sxs-lookup"><span data-stu-id="0ebbb-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="0ebbb-109">Questo comando crea un contenitore che non ha accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="0ebbb-110">Esempio 2: impostare l'ACL del contenitore di archiviazione di Azure usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="0ebbb-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="0ebbb-111">Questo comando consente di ottenere tutti i contenitori di archiviazione il cui nome inizia con container e quindi passa il risultato sulla pipeline per impostare l'autorizzazione per tutti per l'accesso BLOB.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="0ebbb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ebbb-112">PARAMETERS</span></span>

### <span data-ttu-id="0ebbb-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0ebbb-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0ebbb-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0ebbb-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0ebbb-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0ebbb-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0ebbb-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0ebbb-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0ebbb-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0ebbb-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0ebbb-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0ebbb-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-122">The default value is 10.</span></span>

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

### <span data-ttu-id="0ebbb-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0ebbb-123">-Context</span></span>
<span data-ttu-id="0ebbb-124">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="0ebbb-125">Puoi crearlo usando il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0ebbb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebbb-126">-DefaultProfile</span></span>
<span data-ttu-id="0ebbb-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ebbb-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ebbb-128">-Name</span></span>
<span data-ttu-id="0ebbb-129">Specifica un nome di contenitore.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="0ebbb-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ebbb-130">-PassThru</span></span>
<span data-ttu-id="0ebbb-131">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0ebbb-132">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0ebbb-133">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="0ebbb-133">-Permission</span></span>
<span data-ttu-id="0ebbb-134">Specifica il livello di accesso pubblico al contenitore.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="0ebbb-135">Per impostazione predefinita, è possibile accedere al contenitore e a qualsiasi BLOB in esso solo dal proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="0ebbb-136">Per concedere agli utenti anonimi le autorizzazioni di lettura per un contenitore e i relativi BLOB, è possibile impostare le autorizzazioni del contenitore per consentire l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="0ebbb-137">Gli utenti anonimi possono leggere i BLOB in un contenitore disponibile pubblicamente senza autenticazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="0ebbb-138">I valori accettabili per questo parametro sono:--container.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="0ebbb-139">Fornisce l'accesso in lettura completo a un contenitore e ai relativi BLOB.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="0ebbb-140">I client possono enumerare i BLOB nel contenitore tramite una richiesta anonima, ma non possono enumerare i contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="0ebbb-141">--BLOB.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-141">--Blob.</span></span>
<span data-ttu-id="0ebbb-142">Fornisce l'accesso in lettura ai dati BLOB in un contenitore tramite una richiesta anonima, ma non consente l'accesso ai dati del contenitore.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="0ebbb-143">I client non possono enumerare i BLOB nel contenitore usando la richiesta anonima.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="0ebbb-144">--Off.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-144">--Off.</span></span>
<span data-ttu-id="0ebbb-145">Limita l'accesso solo al proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-145">Restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="0ebbb-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0ebbb-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0ebbb-147">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="0ebbb-148">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="0ebbb-149">Timeout lato server per ogni richiesta.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="0ebbb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebbb-150">CommonParameters</span></span>
<span data-ttu-id="0ebbb-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebbb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebbb-152">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ebbb-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebbb-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ebbb-153">INPUTS</span></span>

### <span data-ttu-id="0ebbb-154">System. String</span><span class="sxs-lookup"><span data-stu-id="0ebbb-154">System.String</span></span>

### <span data-ttu-id="0ebbb-155">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0ebbb-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0ebbb-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ebbb-156">OUTPUTS</span></span>

### <span data-ttu-id="0ebbb-157">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0ebbb-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="0ebbb-158">Note</span><span class="sxs-lookup"><span data-stu-id="0ebbb-158">NOTES</span></span>

## <span data-ttu-id="0ebbb-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ebbb-159">RELATED LINKS</span></span>

[<span data-ttu-id="0ebbb-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0ebbb-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="0ebbb-161">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0ebbb-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="0ebbb-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0ebbb-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


