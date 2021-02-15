---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2e444fba12f0ffebfd3d6679293cac31fc574e93
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190887"
---
# <span data-ttu-id="7a84f-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a84f-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="7a84f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a84f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a84f-103">Ottiene i criteri di accesso archiviati per una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7a84f-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="7a84f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a84f-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7a84f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7a84f-105">DESCRIPTION</span></span>
<span data-ttu-id="7a84f-106">Il cmdlet **Get-AzStorageShareStoredAccessPolicy** ottiene i criteri di accesso archiviato per una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7a84f-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="7a84f-107">Per ottenere un criterio specifico, specificarlo in base al nome.</span><span class="sxs-lookup"><span data-stu-id="7a84f-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="7a84f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a84f-108">EXAMPLES</span></span>

### <span data-ttu-id="7a84f-109">Esempio 1: Ottenere criteri di accesso archiviati in una condivisione</span><span class="sxs-lookup"><span data-stu-id="7a84f-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="7a84f-110">Questo comando ottiene un criterio di accesso archiviato denominato GeneralPolicy in ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="7a84f-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="7a84f-111">Esempio 2: Ottenere tutti i criteri di accesso archiviato nella condivisione</span><span class="sxs-lookup"><span data-stu-id="7a84f-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="7a84f-112">Questo comando recupera tutti i criteri di accesso archiviati in ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="7a84f-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="7a84f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a84f-113">PARAMETERS</span></span>

### <span data-ttu-id="7a84f-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7a84f-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7a84f-115">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="7a84f-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7a84f-116">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="7a84f-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7a84f-117">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="7a84f-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7a84f-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7a84f-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7a84f-119">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="7a84f-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7a84f-120">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="7a84f-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7a84f-121">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="7a84f-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7a84f-122">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="7a84f-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7a84f-123">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="7a84f-123">The default value is 10.</span></span>

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

### <span data-ttu-id="7a84f-124">-Context</span><span class="sxs-lookup"><span data-stu-id="7a84f-124">-Context</span></span>
<span data-ttu-id="7a84f-125">Specifica un contesto di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7a84f-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="7a84f-126">Per ottenere un contesto, usare il cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="7a84f-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7a84f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a84f-127">-DefaultProfile</span></span>
<span data-ttu-id="7a84f-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a84f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a84f-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="7a84f-129">-Policy</span></span>
<span data-ttu-id="7a84f-130">Specifica il nome del criterio di accesso archiviato che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a84f-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a84f-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7a84f-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7a84f-132">Specifica la durata del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="7a84f-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7a84f-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7a84f-133">-ShareName</span></span>
<span data-ttu-id="7a84f-134">Specifica il nome della condivisione di archiviazione per cui questo cmdlet ottiene i criteri.</span><span class="sxs-lookup"><span data-stu-id="7a84f-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="7a84f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a84f-135">CommonParameters</span></span>
<span data-ttu-id="7a84f-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a84f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a84f-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a84f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a84f-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="7a84f-138">INPUTS</span></span>

### <span data-ttu-id="7a84f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7a84f-139">System.String</span></span>

### <span data-ttu-id="7a84f-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7a84f-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7a84f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a84f-141">OUTPUTS</span></span>

### <span data-ttu-id="7a84f-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="7a84f-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="7a84f-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="7a84f-143">NOTES</span></span>

## <span data-ttu-id="7a84f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a84f-144">RELATED LINKS</span></span>

[<span data-ttu-id="7a84f-145">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7a84f-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="7a84f-146">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a84f-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="7a84f-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a84f-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="7a84f-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a84f-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
