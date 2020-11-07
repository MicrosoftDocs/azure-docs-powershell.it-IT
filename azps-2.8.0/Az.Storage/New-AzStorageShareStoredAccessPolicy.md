---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: a4013543cfd96a1aaae591a9f1b1ed4b6da46155
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855265"
---
# <span data-ttu-id="4cac6-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cac6-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="4cac6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4cac6-102">SYNOPSIS</span></span>
<span data-ttu-id="4cac6-103">Crea un criterio di accesso archiviato in una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4cac6-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="4cac6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cac6-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4cac6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cac6-105">DESCRIPTION</span></span>
<span data-ttu-id="4cac6-106">Il cmdlet **New-AzStorageShareStoredAccessPolicy** crea un criterio di accesso archiviato in una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4cac6-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="4cac6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cac6-107">EXAMPLES</span></span>

### <span data-ttu-id="4cac6-108">Esempio 1: creare un criterio di accesso archiviato in una condivisione</span><span class="sxs-lookup"><span data-stu-id="4cac6-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="4cac6-109">Questo comando crea un criterio di accesso archiviato con l'autorizzazione completa in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="4cac6-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="4cac6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4cac6-110">PARAMETERS</span></span>

### <span data-ttu-id="4cac6-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cac6-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4cac6-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="4cac6-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4cac6-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4cac6-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4cac6-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4cac6-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4cac6-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4cac6-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4cac6-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="4cac6-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4cac6-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="4cac6-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4cac6-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="4cac6-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4cac6-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="4cac6-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4cac6-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="4cac6-120">The default value is 10.</span></span>

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

### <span data-ttu-id="4cac6-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4cac6-121">-Context</span></span>
<span data-ttu-id="4cac6-122">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4cac6-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4cac6-123">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="4cac6-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4cac6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cac6-124">-DefaultProfile</span></span>
<span data-ttu-id="4cac6-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4cac6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cac6-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4cac6-126">-ExpiryTime</span></span>
<span data-ttu-id="4cac6-127">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="4cac6-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="4cac6-128">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="4cac6-128">-Permission</span></span>
<span data-ttu-id="4cac6-129">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla condivisione di archiviazione o ai file sotto di essa.</span><span class="sxs-lookup"><span data-stu-id="4cac6-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="4cac6-130">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="4cac6-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="4cac6-131">-Policy</span><span class="sxs-lookup"><span data-stu-id="4cac6-131">-Policy</span></span>
<span data-ttu-id="4cac6-132">Specifica un nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="4cac6-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="4cac6-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cac6-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4cac6-134">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="4cac6-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4cac6-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4cac6-135">-ShareName</span></span>
<span data-ttu-id="4cac6-136">Specifica il nome della condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4cac6-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="4cac6-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4cac6-137">-StartTime</span></span>
<span data-ttu-id="4cac6-138">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="4cac6-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="4cac6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cac6-139">CommonParameters</span></span>
<span data-ttu-id="4cac6-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cac6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cac6-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cac6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cac6-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4cac6-142">INPUTS</span></span>

### <span data-ttu-id="4cac6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4cac6-143">System.String</span></span>

### <span data-ttu-id="4cac6-144">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4cac6-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4cac6-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cac6-145">OUTPUTS</span></span>

### <span data-ttu-id="4cac6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4cac6-146">System.String</span></span>

## <span data-ttu-id="4cac6-147">Note</span><span class="sxs-lookup"><span data-stu-id="4cac6-147">NOTES</span></span>

## <span data-ttu-id="4cac6-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cac6-148">RELATED LINKS</span></span>

[<span data-ttu-id="4cac6-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cac6-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="4cac6-150">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4cac6-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4cac6-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cac6-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="4cac6-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cac6-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
