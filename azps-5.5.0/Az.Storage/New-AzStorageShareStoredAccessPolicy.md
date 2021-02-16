---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 52f1e3ce96133d0dc2e389f8eabcb18c6c7790c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197535"
---
# <span data-ttu-id="61fb5-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="61fb5-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="61fb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="61fb5-103">Crea criteri di accesso archiviati in una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="61fb5-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="61fb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61fb5-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="61fb5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="61fb5-105">DESCRIPTION</span></span>
<span data-ttu-id="61fb5-106">Il cmdlet **New-AzStorageShareStoredAccessPolicy** crea un criterio di accesso archiviato in una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="61fb5-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="61fb5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61fb5-107">EXAMPLES</span></span>

### <span data-ttu-id="61fb5-108">Esempio 1: Creare criteri di accesso archiviato in una condivisione</span><span class="sxs-lookup"><span data-stu-id="61fb5-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="61fb5-109">Questo comando crea un criterio di accesso archiviato con autorizzazioni complete in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="61fb5-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="61fb5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61fb5-110">PARAMETERS</span></span>

### <span data-ttu-id="61fb5-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="61fb5-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="61fb5-112">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="61fb5-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="61fb5-113">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="61fb5-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="61fb5-114">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="61fb5-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="61fb5-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="61fb5-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="61fb5-116">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="61fb5-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="61fb5-117">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="61fb5-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="61fb5-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="61fb5-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="61fb5-119">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="61fb5-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="61fb5-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="61fb5-120">The default value is 10.</span></span>

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

### <span data-ttu-id="61fb5-121">-Context</span><span class="sxs-lookup"><span data-stu-id="61fb5-121">-Context</span></span>
<span data-ttu-id="61fb5-122">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="61fb5-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="61fb5-123">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="61fb5-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="61fb5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61fb5-124">-DefaultProfile</span></span>
<span data-ttu-id="61fb5-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61fb5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61fb5-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="61fb5-126">-ExpiryTime</span></span>
<span data-ttu-id="61fb5-127">Specifica l'ora in cui i criteri di accesso archiviato non sono più validi.</span><span class="sxs-lookup"><span data-stu-id="61fb5-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61fb5-128">-Permission</span><span class="sxs-lookup"><span data-stu-id="61fb5-128">-Permission</span></span>
<span data-ttu-id="61fb5-129">Specifica le autorizzazioni nei criteri di accesso archiviato per accedere alla condivisione di archiviazione o ai file al di sotto.</span><span class="sxs-lookup"><span data-stu-id="61fb5-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="61fb5-130">È importante notare che si tratta di una stringa, ad esempio `rwd` (per Lettura, Scrittura ed Elimina).</span><span class="sxs-lookup"><span data-stu-id="61fb5-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61fb5-131">-Policy</span><span class="sxs-lookup"><span data-stu-id="61fb5-131">-Policy</span></span>
<span data-ttu-id="61fb5-132">Specifica un nome per i criteri di accesso archiviato.</span><span class="sxs-lookup"><span data-stu-id="61fb5-132">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61fb5-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="61fb5-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="61fb5-134">Specifica la durata del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="61fb5-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="61fb5-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="61fb5-135">-ShareName</span></span>
<span data-ttu-id="61fb5-136">Specifica il nome della condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="61fb5-136">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61fb5-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="61fb5-137">-StartTime</span></span>
<span data-ttu-id="61fb5-138">Specifica l'ora in cui i criteri di accesso archiviato diventano validi.</span><span class="sxs-lookup"><span data-stu-id="61fb5-138">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61fb5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61fb5-139">CommonParameters</span></span>
<span data-ttu-id="61fb5-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61fb5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61fb5-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61fb5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61fb5-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="61fb5-142">INPUTS</span></span>

### <span data-ttu-id="61fb5-143">System.String</span><span class="sxs-lookup"><span data-stu-id="61fb5-143">System.String</span></span>

### <span data-ttu-id="61fb5-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="61fb5-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="61fb5-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61fb5-145">OUTPUTS</span></span>

### <span data-ttu-id="61fb5-146">System.String</span><span class="sxs-lookup"><span data-stu-id="61fb5-146">System.String</span></span>

## <span data-ttu-id="61fb5-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="61fb5-147">NOTES</span></span>

## <span data-ttu-id="61fb5-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61fb5-148">RELATED LINKS</span></span>

[<span data-ttu-id="61fb5-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="61fb5-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="61fb5-150">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="61fb5-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="61fb5-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="61fb5-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="61fb5-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="61fb5-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
