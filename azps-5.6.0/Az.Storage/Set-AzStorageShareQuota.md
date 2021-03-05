---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: 132ad47cd52f258b78ac944342d86979a69abbe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007549"
---
# <span data-ttu-id="eb603-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="eb603-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="eb603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb603-102">SYNOPSIS</span></span>
<span data-ttu-id="eb603-103">Imposta la capacità di archiviazione per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="eb603-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="eb603-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb603-104">SYNTAX</span></span>

### <span data-ttu-id="eb603-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eb603-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="eb603-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="eb603-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb603-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eb603-107">DESCRIPTION</span></span>
<span data-ttu-id="eb603-108">Il cmdlet **Set-AzStorageShareQuota** imposta la capacità di archiviazione per una condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="eb603-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="eb603-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb603-109">EXAMPLES</span></span>

### <span data-ttu-id="eb603-110">Esempio 1: Impostare la capacità di archiviazione di una condivisione</span><span class="sxs-lookup"><span data-stu-id="eb603-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="eb603-111">Questo comando imposta la capacità di archiviazione per una condivisione denominata ContosoShare01 su 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="eb603-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="eb603-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb603-112">PARAMETERS</span></span>

### <span data-ttu-id="eb603-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eb603-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="eb603-114">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="eb603-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="eb603-115">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="eb603-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="eb603-116">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="eb603-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="eb603-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="eb603-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="eb603-118">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="eb603-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="eb603-119">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="eb603-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="eb603-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="eb603-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="eb603-121">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="eb603-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="eb603-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="eb603-122">The default value is 10.</span></span>

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

### <span data-ttu-id="eb603-123">-Context</span><span class="sxs-lookup"><span data-stu-id="eb603-123">-Context</span></span>
<span data-ttu-id="eb603-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="eb603-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="eb603-125">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="eb603-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="eb603-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb603-126">-DefaultProfile</span></span>
<span data-ttu-id="eb603-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb603-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb603-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="eb603-128">-Quota</span></span>
<span data-ttu-id="eb603-129">Specifica il valore della quota in gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="eb603-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="eb603-130">Vedere la limitazione delle quote in https://docs.microsoft.com/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="eb603-130">See the quota limitation in https://docs.microsoft.com/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

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

### <span data-ttu-id="eb603-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eb603-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="eb603-132">Specifica la durata del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="eb603-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="eb603-133">-Condividi</span><span class="sxs-lookup"><span data-stu-id="eb603-133">-Share</span></span>
<span data-ttu-id="eb603-134">Specifica un **oggetto CloudFileShare** che rappresenta la condivisione per cui questo cmdlet imposta una quota.</span><span class="sxs-lookup"><span data-stu-id="eb603-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="eb603-135">Per ottenere un **oggetto CloudFileShare,** usare il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="eb603-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="eb603-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="eb603-136">-ShareName</span></span>
<span data-ttu-id="eb603-137">Specifica il nome della condivisione file per cui impostare una quota.</span><span class="sxs-lookup"><span data-stu-id="eb603-137">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="eb603-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb603-138">CommonParameters</span></span>
<span data-ttu-id="eb603-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb603-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb603-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb603-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb603-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="eb603-141">INPUTS</span></span>

### <span data-ttu-id="eb603-142">System.String</span><span class="sxs-lookup"><span data-stu-id="eb603-142">System.String</span></span>

### <span data-ttu-id="eb603-143">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="eb603-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="eb603-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb603-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eb603-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb603-145">OUTPUTS</span></span>

### <span data-ttu-id="eb603-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="eb603-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="eb603-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="eb603-147">NOTES</span></span>

## <span data-ttu-id="eb603-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb603-148">RELATED LINKS</span></span>

[<span data-ttu-id="eb603-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="eb603-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="eb603-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="eb603-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="eb603-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb603-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
