---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: d029a00a2ddba5974fb473e58b933820e2e14757
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188839"
---
# <span data-ttu-id="b6b7d-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="b6b7d-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="b6b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b7d-103">Imposta la capacità di archiviazione per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="b6b7d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6b7d-104">SYNTAX</span></span>

### <span data-ttu-id="b6b7d-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6b7d-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b6b7d-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="b6b7d-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6b7d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6b7d-107">DESCRIPTION</span></span>
<span data-ttu-id="b6b7d-108">Il cmdlet **Set-AzStorageShareQuota** imposta la capacità di archiviazione per una condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="b6b7d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6b7d-109">EXAMPLES</span></span>

### <span data-ttu-id="b6b7d-110">Esempio 1: Impostare la capacità di archiviazione di una condivisione</span><span class="sxs-lookup"><span data-stu-id="b6b7d-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="b6b7d-111">Questo comando imposta la capacità di archiviazione per una condivisione denominata ContosoShare01 su 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="b6b7d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6b7d-112">PARAMETERS</span></span>

### <span data-ttu-id="b6b7d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b6b7d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b6b7d-114">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b6b7d-115">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b6b7d-116">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b6b7d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b6b7d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b6b7d-118">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b6b7d-119">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b6b7d-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b6b7d-121">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b6b7d-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="b6b7d-123">-Context</span><span class="sxs-lookup"><span data-stu-id="b6b7d-123">-Context</span></span>
<span data-ttu-id="b6b7d-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b6b7d-125">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="b6b7d-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b6b7d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b7d-126">-DefaultProfile</span></span>
<span data-ttu-id="b6b7d-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6b7d-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="b6b7d-128">-Quota</span></span>
<span data-ttu-id="b6b7d-129">Specifica il valore della quota in gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="b6b7d-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="b6b7d-130">Vedere la limitazione delle quote in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="b6b7d-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

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

### <span data-ttu-id="b6b7d-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b6b7d-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b6b7d-132">Specifica la durata del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b6b7d-133">-Condividi</span><span class="sxs-lookup"><span data-stu-id="b6b7d-133">-Share</span></span>
<span data-ttu-id="b6b7d-134">Specifica un **oggetto CloudFileShare** che rappresenta la condivisione per cui questo cmdlet imposta una quota.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="b6b7d-135">Per ottenere un **oggetto CloudFileShare,** usare il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="b6b7d-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b6b7d-136">-ShareName</span></span>
<span data-ttu-id="b6b7d-137">Specifica il nome della condivisione file per cui impostare una quota.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-137">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="b6b7d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b7d-138">CommonParameters</span></span>
<span data-ttu-id="b6b7d-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b7d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b7d-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6b7d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b7d-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6b7d-141">INPUTS</span></span>

### <span data-ttu-id="b6b7d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b6b7d-142">System.String</span></span>

### <span data-ttu-id="b6b7d-143">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b6b7d-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="b6b7d-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6b7d-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b6b7d-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6b7d-145">OUTPUTS</span></span>

### <span data-ttu-id="b6b7d-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="b6b7d-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="b6b7d-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6b7d-147">NOTES</span></span>

## <span data-ttu-id="b6b7d-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6b7d-148">RELATED LINKS</span></span>

[<span data-ttu-id="b6b7d-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b6b7d-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="b6b7d-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="b6b7d-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="b6b7d-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6b7d-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
