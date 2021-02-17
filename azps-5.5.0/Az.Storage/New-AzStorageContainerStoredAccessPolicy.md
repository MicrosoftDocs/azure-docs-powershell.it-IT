---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: eb51b8c4e33f45d637354f85be049295626afdd6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198422"
---
# <span data-ttu-id="65b33-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65b33-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="65b33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65b33-102">SYNOPSIS</span></span>
<span data-ttu-id="65b33-103">Crea criteri di accesso archiviato per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="65b33-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="65b33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65b33-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="65b33-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="65b33-105">DESCRIPTION</span></span>
<span data-ttu-id="65b33-106">Il cmdlet **New-AzStorageContainerStoredAccessPolicy** crea un criterio di accesso archiviato per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="65b33-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="65b33-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65b33-107">EXAMPLES</span></span>

### <span data-ttu-id="65b33-108">Esempio 1: Creare criteri di accesso archiviati in un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="65b33-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="65b33-109">Questo comando crea un criterio di accesso denominato Policy01 nel contenitore di archiviazione denominato MyContainer.</span><span class="sxs-lookup"><span data-stu-id="65b33-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="65b33-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65b33-110">PARAMETERS</span></span>

### <span data-ttu-id="65b33-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="65b33-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="65b33-112">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="65b33-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="65b33-113">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="65b33-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="65b33-114">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="65b33-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="65b33-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="65b33-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="65b33-116">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="65b33-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="65b33-117">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="65b33-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="65b33-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="65b33-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="65b33-119">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="65b33-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="65b33-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="65b33-120">The default value is 10.</span></span>

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

### <span data-ttu-id="65b33-121">-Container</span><span class="sxs-lookup"><span data-stu-id="65b33-121">-Container</span></span>
<span data-ttu-id="65b33-122">Specifica il nome del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="65b33-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="65b33-123">-Context</span><span class="sxs-lookup"><span data-stu-id="65b33-123">-Context</span></span>
<span data-ttu-id="65b33-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="65b33-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="65b33-125">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="65b33-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="65b33-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b33-126">-DefaultProfile</span></span>
<span data-ttu-id="65b33-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65b33-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65b33-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="65b33-128">-ExpiryTime</span></span>
<span data-ttu-id="65b33-129">Specifica l'ora in cui i criteri di accesso archiviato non sono più validi.</span><span class="sxs-lookup"><span data-stu-id="65b33-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="65b33-130">-Permission</span><span class="sxs-lookup"><span data-stu-id="65b33-130">-Permission</span></span>
<span data-ttu-id="65b33-131">Specifica le autorizzazioni nel criterio di accesso archiviato per accedere al contenitore.</span><span class="sxs-lookup"><span data-stu-id="65b33-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="65b33-132">È importante notare che si tratta di una stringa, ad esempio `rwd` (per Lettura, Scrittura ed Elimina).</span><span class="sxs-lookup"><span data-stu-id="65b33-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="65b33-133">-Policy</span><span class="sxs-lookup"><span data-stu-id="65b33-133">-Policy</span></span>
<span data-ttu-id="65b33-134">Specifica un criterio di accesso archiviato, che include le autorizzazioni per questo token di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="65b33-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="65b33-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="65b33-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="65b33-136">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="65b33-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="65b33-137">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="65b33-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="65b33-138">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="65b33-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="65b33-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="65b33-139">-StartTime</span></span>
<span data-ttu-id="65b33-140">Specifica l'ora in cui i criteri di accesso archiviato diventano validi.</span><span class="sxs-lookup"><span data-stu-id="65b33-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="65b33-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b33-141">CommonParameters</span></span>
<span data-ttu-id="65b33-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b33-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b33-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65b33-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b33-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="65b33-144">INPUTS</span></span>

### <span data-ttu-id="65b33-145">System.String</span><span class="sxs-lookup"><span data-stu-id="65b33-145">System.String</span></span>

### <span data-ttu-id="65b33-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="65b33-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="65b33-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65b33-147">OUTPUTS</span></span>

### <span data-ttu-id="65b33-148">System.String</span><span class="sxs-lookup"><span data-stu-id="65b33-148">System.String</span></span>

## <span data-ttu-id="65b33-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="65b33-149">NOTES</span></span>

## <span data-ttu-id="65b33-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65b33-150">RELATED LINKS</span></span>

[<span data-ttu-id="65b33-151">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65b33-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="65b33-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="65b33-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="65b33-153">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65b33-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="65b33-154">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65b33-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


