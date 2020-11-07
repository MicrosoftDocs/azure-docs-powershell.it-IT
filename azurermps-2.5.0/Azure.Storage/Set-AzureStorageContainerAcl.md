---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontaineracl
schema: 2.0.0
ms.openlocfilehash: 95931b9aeb7c3b9f2869bc35115ab49a8aaf901f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865861"
---
# <span data-ttu-id="3eee2-101">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="3eee2-101">Set-AzureStorageContainerAcl</span></span>

## <span data-ttu-id="3eee2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3eee2-102">SYNOPSIS</span></span>
<span data-ttu-id="3eee2-103">Imposta l'autorizzazione di accesso pubblico per un contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3eee2-103">Sets the public access permission to a storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eee2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3eee2-104">SYNTAX</span></span>

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3eee2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3eee2-105">DESCRIPTION</span></span>
<span data-ttu-id="3eee2-106">Il cmdlet **set-AzureStorageContainerAcl** imposta l'autorizzazione di accesso pubblico sul contenitore di archiviazione specificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="3eee2-106">The **Set-AzureStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="3eee2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3eee2-107">EXAMPLES</span></span>

### <span data-ttu-id="3eee2-108">Esempio 1: impostare l'ACL del contenitore di archiviazione di Azure per nome</span><span class="sxs-lookup"><span data-stu-id="3eee2-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="3eee2-109">Questo comando crea un contenitore che non ha accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="3eee2-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="3eee2-110">Esempio 2: impostare l'ACL del contenitore di archiviazione di Azure usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="3eee2-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="3eee2-111">Questo comando consente di ottenere tutti i contenitori di archiviazione il cui nome inizia con container e quindi passa il risultato sulla pipeline per impostare l'autorizzazione per tutti per l'accesso BLOB.</span><span class="sxs-lookup"><span data-stu-id="3eee2-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="3eee2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3eee2-112">PARAMETERS</span></span>

### <span data-ttu-id="3eee2-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3eee2-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3eee2-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="3eee2-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3eee2-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="3eee2-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3eee2-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="3eee2-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3eee2-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3eee2-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3eee2-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="3eee2-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3eee2-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="3eee2-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3eee2-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="3eee2-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3eee2-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="3eee2-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3eee2-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="3eee2-122">The default value is 10.</span></span>

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

### <span data-ttu-id="3eee2-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3eee2-123">-Context</span></span>
<span data-ttu-id="3eee2-124">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3eee2-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3eee2-125">Puoi crearlo usando il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3eee2-125">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3eee2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eee2-126">-DefaultProfile</span></span>
<span data-ttu-id="3eee2-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3eee2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eee2-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="3eee2-128">-Name</span></span>
<span data-ttu-id="3eee2-129">Specifica un nome di contenitore.</span><span class="sxs-lookup"><span data-stu-id="3eee2-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="3eee2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3eee2-130">-PassThru</span></span>
<span data-ttu-id="3eee2-131">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="3eee2-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3eee2-132">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3eee2-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3eee2-133">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="3eee2-133">-Permission</span></span>
<span data-ttu-id="3eee2-134">Specifica il livello di accesso pubblico al contenitore.</span><span class="sxs-lookup"><span data-stu-id="3eee2-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="3eee2-135">Per impostazione predefinita, è possibile accedere al contenitore e a qualsiasi BLOB in esso solo dal proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3eee2-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="3eee2-136">Per concedere agli utenti anonimi le autorizzazioni di lettura per un contenitore e i relativi BLOB, è possibile impostare le autorizzazioni del contenitore per consentire l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="3eee2-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="3eee2-137">Gli utenti anonimi possono leggere i BLOB in un contenitore disponibile pubblicamente senza autenticazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="3eee2-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="3eee2-138">I valori accettabili per questo parametro sono:--container.</span><span class="sxs-lookup"><span data-stu-id="3eee2-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="3eee2-139">Fornisce l'accesso in lettura completo a un contenitore e ai relativi BLOB.</span><span class="sxs-lookup"><span data-stu-id="3eee2-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="3eee2-140">I client possono enumerare i BLOB nel contenitore tramite una richiesta anonima, ma non possono enumerare i contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3eee2-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="3eee2-141">--BLOB.</span><span class="sxs-lookup"><span data-stu-id="3eee2-141">--Blob.</span></span>
<span data-ttu-id="3eee2-142">Fornisce l'accesso in lettura ai dati BLOB in un contenitore tramite una richiesta anonima, ma non consente l'accesso ai dati del contenitore.</span><span class="sxs-lookup"><span data-stu-id="3eee2-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="3eee2-143">I client non possono enumerare i BLOB nel contenitore usando la richiesta anonima.</span><span class="sxs-lookup"><span data-stu-id="3eee2-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="3eee2-144">--Off.</span><span class="sxs-lookup"><span data-stu-id="3eee2-144">--Off.</span></span>
<span data-ttu-id="3eee2-145">Limita l'accesso solo al proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3eee2-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eee2-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3eee2-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3eee2-147">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="3eee2-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3eee2-148">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="3eee2-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="3eee2-149">Timeout lato server per ogni richiesta.</span><span class="sxs-lookup"><span data-stu-id="3eee2-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="3eee2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eee2-150">CommonParameters</span></span>
<span data-ttu-id="3eee2-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eee2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eee2-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eee2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eee2-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3eee2-153">INPUTS</span></span>

### <span data-ttu-id="3eee2-154">System. String</span><span class="sxs-lookup"><span data-stu-id="3eee2-154">System.String</span></span>

### <span data-ttu-id="3eee2-155">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3eee2-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3eee2-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3eee2-156">OUTPUTS</span></span>

### <span data-ttu-id="3eee2-157">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3eee2-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="3eee2-158">Note</span><span class="sxs-lookup"><span data-stu-id="3eee2-158">NOTES</span></span>

## <span data-ttu-id="3eee2-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3eee2-159">RELATED LINKS</span></span>

[<span data-ttu-id="3eee2-160">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3eee2-160">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="3eee2-161">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3eee2-161">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="3eee2-162">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3eee2-162">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)


