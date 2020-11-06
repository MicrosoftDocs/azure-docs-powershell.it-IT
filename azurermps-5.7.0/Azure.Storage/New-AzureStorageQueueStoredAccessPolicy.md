---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: ba1759d9efb1c5e624b1ced5cddd03ee79917c4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515875"
---
# <span data-ttu-id="46437-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="46437-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="46437-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46437-102">SYNOPSIS</span></span>
<span data-ttu-id="46437-103">Crea un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="46437-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46437-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46437-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="46437-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46437-105">DESCRIPTION</span></span>
<span data-ttu-id="46437-106">Il cmdlet **New-AzureStorageQueueStoredAccessPolicy** crea un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="46437-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="46437-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46437-107">EXAMPLES</span></span>

### <span data-ttu-id="46437-108">Esempio 1: creare criteri di accesso archiviati in una coda di archiviazione</span><span class="sxs-lookup"><span data-stu-id="46437-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="46437-109">Questo comando crea un criterio di accesso denominato Policy01 nella coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="46437-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="46437-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46437-110">PARAMETERS</span></span>

### <span data-ttu-id="46437-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="46437-111">-Context</span></span>
<span data-ttu-id="46437-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="46437-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="46437-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="46437-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46437-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="46437-114">-ExpiryTime</span></span>
<span data-ttu-id="46437-115">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="46437-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46437-116">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="46437-116">-Permission</span></span>
<span data-ttu-id="46437-117">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="46437-117">Specifies permissions in the stored access policy to access the storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46437-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="46437-118">-Policy</span></span>
<span data-ttu-id="46437-119">Specifica un nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="46437-119">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46437-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="46437-120">-Queue</span></span>
<span data-ttu-id="46437-121">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="46437-121">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46437-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="46437-122">-StartTime</span></span>
<span data-ttu-id="46437-123">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="46437-123">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46437-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46437-124">CommonParameters</span></span>
<span data-ttu-id="46437-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46437-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46437-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46437-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46437-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46437-127">INPUTS</span></span>

### <span data-ttu-id="46437-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="46437-128">IStorageContext</span></span>

<span data-ttu-id="46437-129">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="46437-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="46437-130">Stringa</span><span class="sxs-lookup"><span data-stu-id="46437-130">String</span></span>

<span data-ttu-id="46437-131">Il parametro "Queue" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="46437-131">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="46437-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46437-132">OUTPUTS</span></span>

### <span data-ttu-id="46437-133">System. String</span><span class="sxs-lookup"><span data-stu-id="46437-133">System.String</span></span>

## <span data-ttu-id="46437-134">Note</span><span class="sxs-lookup"><span data-stu-id="46437-134">NOTES</span></span>

## <span data-ttu-id="46437-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46437-135">RELATED LINKS</span></span>

[<span data-ttu-id="46437-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="46437-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="46437-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="46437-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="46437-138">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="46437-138">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="46437-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="46437-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


