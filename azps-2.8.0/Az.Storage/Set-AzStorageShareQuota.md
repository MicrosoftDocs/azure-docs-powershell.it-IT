---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: 095d43d41ebc2bcccb770171e668cb737fb40834
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673792"
---
# <span data-ttu-id="516e0-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="516e0-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="516e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="516e0-102">SYNOPSIS</span></span>
<span data-ttu-id="516e0-103">Imposta la capacità di archiviazione per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="516e0-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="516e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="516e0-104">SYNTAX</span></span>

### <span data-ttu-id="516e0-105">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="516e0-105">ShareName</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="516e0-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="516e0-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="516e0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="516e0-107">DESCRIPTION</span></span>
<span data-ttu-id="516e0-108">Il cmdlet **set-AzStorageShareQuota** imposta la capacità di archiviazione per una condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="516e0-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="516e0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="516e0-109">EXAMPLES</span></span>

### <span data-ttu-id="516e0-110">Esempio 1: impostare la capacità di archiviazione di una condivisione</span><span class="sxs-lookup"><span data-stu-id="516e0-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="516e0-111">Questo comando imposta la capacità di archiviazione per una condivisione denominata ContosoShare01 in 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="516e0-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="516e0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="516e0-112">PARAMETERS</span></span>

### <span data-ttu-id="516e0-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="516e0-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="516e0-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="516e0-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="516e0-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="516e0-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="516e0-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="516e0-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="516e0-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="516e0-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="516e0-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="516e0-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="516e0-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="516e0-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="516e0-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="516e0-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="516e0-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="516e0-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="516e0-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="516e0-122">The default value is 10.</span></span>

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

### <span data-ttu-id="516e0-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="516e0-123">-Context</span></span>
<span data-ttu-id="516e0-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="516e0-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="516e0-125">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="516e0-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="516e0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="516e0-126">-DefaultProfile</span></span>
<span data-ttu-id="516e0-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="516e0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="516e0-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="516e0-128">-Quota</span></span>
<span data-ttu-id="516e0-129">Specifica il valore di quota in gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="516e0-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="516e0-130">Vedere la limitazione delle quote in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="516e0-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

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

### <span data-ttu-id="516e0-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="516e0-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="516e0-132">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="516e0-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="516e0-133">-Condividi</span><span class="sxs-lookup"><span data-stu-id="516e0-133">-Share</span></span>
<span data-ttu-id="516e0-134">Specifica un oggetto **CloudFileShare** per rappresentare la condivisione per cui questo cmdlet imposta una quota.</span><span class="sxs-lookup"><span data-stu-id="516e0-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="516e0-135">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="516e0-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="516e0-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="516e0-136">-ShareName</span></span>
<span data-ttu-id="516e0-137">Specifica il nome della condivisione file per cui impostare una quota.</span><span class="sxs-lookup"><span data-stu-id="516e0-137">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="516e0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="516e0-138">CommonParameters</span></span>
<span data-ttu-id="516e0-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="516e0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="516e0-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="516e0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="516e0-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="516e0-141">INPUTS</span></span>

### <span data-ttu-id="516e0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="516e0-142">System.String</span></span>

### <span data-ttu-id="516e0-143">Microsoft. Azure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="516e0-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="516e0-144">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="516e0-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="516e0-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="516e0-145">OUTPUTS</span></span>

### <span data-ttu-id="516e0-146">Microsoft. Azure. storage. file. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="516e0-146">Microsoft.Azure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="516e0-147">Note</span><span class="sxs-lookup"><span data-stu-id="516e0-147">NOTES</span></span>

## <span data-ttu-id="516e0-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="516e0-148">RELATED LINKS</span></span>

[<span data-ttu-id="516e0-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="516e0-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="516e0-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="516e0-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="516e0-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="516e0-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
