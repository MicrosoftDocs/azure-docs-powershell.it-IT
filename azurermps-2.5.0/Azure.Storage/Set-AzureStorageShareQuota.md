---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharequota
schema: 2.0.0
ms.openlocfilehash: 3d2fd2ae65ff343bbe5faeece41194c768bec8c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867169"
---
# <span data-ttu-id="e7cfd-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="e7cfd-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="e7cfd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="e7cfd-103">Imposta la capacità di archiviazione per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-103">Sets the storage capacity for a share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7cfd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7cfd-104">SYNTAX</span></span>

### <span data-ttu-id="e7cfd-105">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="e7cfd-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e7cfd-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="e7cfd-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7cfd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7cfd-107">DESCRIPTION</span></span>
<span data-ttu-id="e7cfd-108">Il cmdlet **set-AzureStorageShareQuota** imposta la capacità di archiviazione per una condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="e7cfd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7cfd-109">EXAMPLES</span></span>

### <span data-ttu-id="e7cfd-110">Esempio 1: impostare la capacità di archiviazione di una condivisione</span><span class="sxs-lookup"><span data-stu-id="e7cfd-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="e7cfd-111">Questo comando imposta la capacità di archiviazione per una condivisione denominata ContosoShare01 in 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="e7cfd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7cfd-112">PARAMETERS</span></span>

### <span data-ttu-id="e7cfd-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e7cfd-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e7cfd-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e7cfd-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e7cfd-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e7cfd-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e7cfd-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e7cfd-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e7cfd-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e7cfd-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e7cfd-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e7cfd-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-122">The default value is 10.</span></span>

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

### <span data-ttu-id="e7cfd-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e7cfd-123">-Context</span></span>
<span data-ttu-id="e7cfd-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e7cfd-125">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="e7cfd-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e7cfd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7cfd-126">-DefaultProfile</span></span>
<span data-ttu-id="e7cfd-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7cfd-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="e7cfd-128">-Quota</span></span>
<span data-ttu-id="e7cfd-129">Specifica il valore di quota in gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="e7cfd-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="e7cfd-130">Vedere la limitazione delle quote in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="e7cfd-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7cfd-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e7cfd-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e7cfd-132">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e7cfd-133">-Condividi</span><span class="sxs-lookup"><span data-stu-id="e7cfd-133">-Share</span></span>
<span data-ttu-id="e7cfd-134">Specifica un oggetto **CloudFileShare** per rappresentare la condivisione per cui questo cmdlet imposta una quota.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="e7cfd-135">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-135">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7cfd-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e7cfd-136">-ShareName</span></span>
<span data-ttu-id="e7cfd-137">Specifica il nome della condivisione file per cui impostare una quota.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-137">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="e7cfd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7cfd-138">CommonParameters</span></span>
<span data-ttu-id="e7cfd-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7cfd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7cfd-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7cfd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7cfd-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7cfd-141">INPUTS</span></span>

### <span data-ttu-id="e7cfd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e7cfd-142">System.String</span></span>

### <span data-ttu-id="e7cfd-143">Microsoft. WindowsAzure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="e7cfd-143">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="e7cfd-144">Parametri: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e7cfd-144">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="e7cfd-145">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e7cfd-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e7cfd-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7cfd-146">OUTPUTS</span></span>

### <span data-ttu-id="e7cfd-147">Microsoft. WindowsAzure. storage. file. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="e7cfd-147">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="e7cfd-148">Note</span><span class="sxs-lookup"><span data-stu-id="e7cfd-148">NOTES</span></span>

## <span data-ttu-id="e7cfd-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7cfd-149">RELATED LINKS</span></span>

[<span data-ttu-id="e7cfd-150">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e7cfd-150">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="e7cfd-151">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e7cfd-151">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="e7cfd-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e7cfd-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
