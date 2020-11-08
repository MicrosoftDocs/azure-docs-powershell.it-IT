---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: d029a00a2ddba5974fb473e58b933820e2e14757
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193713"
---
# <span data-ttu-id="dccbd-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="dccbd-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="dccbd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dccbd-102">SYNOPSIS</span></span>
<span data-ttu-id="dccbd-103">Imposta la capacità di archiviazione per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="dccbd-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="dccbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dccbd-104">SYNTAX</span></span>

### <span data-ttu-id="dccbd-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dccbd-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="dccbd-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="dccbd-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="dccbd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dccbd-107">DESCRIPTION</span></span>
<span data-ttu-id="dccbd-108">Il cmdlet **set-AzStorageShareQuota** imposta la capacità di archiviazione per una condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="dccbd-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="dccbd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dccbd-109">EXAMPLES</span></span>

### <span data-ttu-id="dccbd-110">Esempio 1: impostare la capacità di archiviazione di una condivisione</span><span class="sxs-lookup"><span data-stu-id="dccbd-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="dccbd-111">Questo comando imposta la capacità di archiviazione per una condivisione denominata ContosoShare01 in 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="dccbd-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="dccbd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dccbd-112">PARAMETERS</span></span>

### <span data-ttu-id="dccbd-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dccbd-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dccbd-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="dccbd-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dccbd-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="dccbd-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dccbd-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="dccbd-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dccbd-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dccbd-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dccbd-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="dccbd-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="dccbd-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="dccbd-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="dccbd-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="dccbd-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="dccbd-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="dccbd-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="dccbd-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="dccbd-122">The default value is 10.</span></span>

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

### <span data-ttu-id="dccbd-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="dccbd-123">-Context</span></span>
<span data-ttu-id="dccbd-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dccbd-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dccbd-125">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="dccbd-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="dccbd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dccbd-126">-DefaultProfile</span></span>
<span data-ttu-id="dccbd-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dccbd-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dccbd-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="dccbd-128">-Quota</span></span>
<span data-ttu-id="dccbd-129">Specifica il valore di quota in gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="dccbd-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="dccbd-130">Vedere la limitazione delle quote in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="dccbd-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: QuotaGiB

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dccbd-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dccbd-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dccbd-132">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="dccbd-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="dccbd-133">-Condividi</span><span class="sxs-lookup"><span data-stu-id="dccbd-133">-Share</span></span>
<span data-ttu-id="dccbd-134">Specifica un oggetto **CloudFileShare** per rappresentare la condivisione per cui questo cmdlet imposta una quota.</span><span class="sxs-lookup"><span data-stu-id="dccbd-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="dccbd-135">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="dccbd-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="dccbd-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="dccbd-136">-ShareName</span></span>
<span data-ttu-id="dccbd-137">Specifica il nome della condivisione file per cui impostare una quota.</span><span class="sxs-lookup"><span data-stu-id="dccbd-137">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dccbd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dccbd-138">CommonParameters</span></span>
<span data-ttu-id="dccbd-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dccbd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dccbd-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dccbd-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dccbd-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dccbd-141">INPUTS</span></span>

### <span data-ttu-id="dccbd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="dccbd-142">System.String</span></span>

### <span data-ttu-id="dccbd-143">Microsoft. Azure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="dccbd-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="dccbd-144">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dccbd-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dccbd-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dccbd-145">OUTPUTS</span></span>

### <span data-ttu-id="dccbd-146">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="dccbd-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="dccbd-147">Note</span><span class="sxs-lookup"><span data-stu-id="dccbd-147">NOTES</span></span>

## <span data-ttu-id="dccbd-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dccbd-148">RELATED LINKS</span></span>

[<span data-ttu-id="dccbd-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dccbd-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="dccbd-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="dccbd-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="dccbd-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dccbd-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
