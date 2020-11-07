---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 701b2dd3f2f0faef764cd8b1b64dd6cf88ef069b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676603"
---
# <span data-ttu-id="def69-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="def69-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="def69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="def69-102">SYNOPSIS</span></span>
<span data-ttu-id="def69-103">Ottiene i criteri di accesso archiviati per una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="def69-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="def69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="def69-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="def69-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="def69-105">DESCRIPTION</span></span>
<span data-ttu-id="def69-106">Il cmdlet **Get-AzStorageShareStoredAccessPolicy** ottiene i criteri di accesso archiviati per una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="def69-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="def69-107">Per ottenere un criterio specifico, specificarlo per nome.</span><span class="sxs-lookup"><span data-stu-id="def69-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="def69-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="def69-108">EXAMPLES</span></span>

### <span data-ttu-id="def69-109">Esempio 1: ottenere un criterio di accesso archiviato in una condivisione</span><span class="sxs-lookup"><span data-stu-id="def69-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="def69-110">Questo comando ottiene un criterio di accesso archiviato denominato GeneralPolicy in ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="def69-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="def69-111">Esempio 2: ottenere tutti i criteri di accesso archiviati in Condividi</span><span class="sxs-lookup"><span data-stu-id="def69-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="def69-112">Questo comando ottiene tutti i criteri di accesso archiviati in ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="def69-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="def69-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="def69-113">PARAMETERS</span></span>

### <span data-ttu-id="def69-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="def69-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="def69-115">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="def69-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="def69-116">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="def69-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="def69-117">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="def69-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="def69-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="def69-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="def69-119">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="def69-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="def69-120">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="def69-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="def69-121">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="def69-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="def69-122">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="def69-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="def69-123">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="def69-123">The default value is 10.</span></span>

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

### <span data-ttu-id="def69-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="def69-124">-Context</span></span>
<span data-ttu-id="def69-125">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="def69-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="def69-126">Per ottenere un contesto, usa il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="def69-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="def69-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def69-127">-DefaultProfile</span></span>
<span data-ttu-id="def69-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="def69-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="def69-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="def69-129">-Policy</span></span>
<span data-ttu-id="def69-130">Specifica il nome dei criteri di accesso archiviati ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="def69-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="def69-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="def69-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="def69-132">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="def69-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="def69-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="def69-133">-ShareName</span></span>
<span data-ttu-id="def69-134">Specifica il nome della condivisione di archiviazione per cui questo cmdlet ottiene i criteri.</span><span class="sxs-lookup"><span data-stu-id="def69-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="def69-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def69-135">CommonParameters</span></span>
<span data-ttu-id="def69-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def69-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def69-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="def69-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def69-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="def69-138">INPUTS</span></span>

### <span data-ttu-id="def69-139">System. String</span><span class="sxs-lookup"><span data-stu-id="def69-139">System.String</span></span>

### <span data-ttu-id="def69-140">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="def69-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="def69-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="def69-141">OUTPUTS</span></span>

### <span data-ttu-id="def69-142">Microsoft. WindowsAzure. storage. file. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="def69-142">Microsoft.WindowsAzure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="def69-143">Note</span><span class="sxs-lookup"><span data-stu-id="def69-143">NOTES</span></span>

## <span data-ttu-id="def69-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="def69-144">RELATED LINKS</span></span>

[<span data-ttu-id="def69-145">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="def69-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="def69-146">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="def69-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="def69-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="def69-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="def69-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="def69-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)