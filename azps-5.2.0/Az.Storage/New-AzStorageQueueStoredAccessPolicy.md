---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 65afd4039fb772d1ecf522645fe41154dae42981
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324671"
---
# <span data-ttu-id="7b9f2-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7b9f2-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="7b9f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="7b9f2-103">Crea un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="7b9f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b9f2-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b9f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b9f2-105">DESCRIPTION</span></span>
<span data-ttu-id="7b9f2-106">Il cmdlet **New-AzStorageQueueStoredAccessPolicy** crea un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="7b9f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b9f2-107">EXAMPLES</span></span>

### <span data-ttu-id="7b9f2-108">Esempio 1: creare criteri di accesso archiviati in una coda di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7b9f2-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="7b9f2-109">Questo comando crea un criterio di accesso denominato Policy01 nella coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="7b9f2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b9f2-110">PARAMETERS</span></span>

### <span data-ttu-id="7b9f2-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7b9f2-111">-Context</span></span>
<span data-ttu-id="7b9f2-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7b9f2-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7b9f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b9f2-114">-DefaultProfile</span></span>
<span data-ttu-id="7b9f2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b9f2-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7b9f2-116">-ExpiryTime</span></span>
<span data-ttu-id="7b9f2-117">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="7b9f2-118">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="7b9f2-118">-Permission</span></span>
<span data-ttu-id="7b9f2-119">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="7b9f2-120">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="7b9f2-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="7b9f2-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="7b9f2-121">-Policy</span></span>
<span data-ttu-id="7b9f2-122">Specifica un nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="7b9f2-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="7b9f2-123">-Queue</span></span>
<span data-ttu-id="7b9f2-124">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="7b9f2-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7b9f2-125">-StartTime</span></span>
<span data-ttu-id="7b9f2-126">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="7b9f2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b9f2-127">CommonParameters</span></span>
<span data-ttu-id="7b9f2-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b9f2-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b9f2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b9f2-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b9f2-130">INPUTS</span></span>

### <span data-ttu-id="7b9f2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7b9f2-131">System.String</span></span>

### <span data-ttu-id="7b9f2-132">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7b9f2-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7b9f2-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b9f2-133">OUTPUTS</span></span>

### <span data-ttu-id="7b9f2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7b9f2-134">System.String</span></span>

## <span data-ttu-id="7b9f2-135">Note</span><span class="sxs-lookup"><span data-stu-id="7b9f2-135">NOTES</span></span>

## <span data-ttu-id="7b9f2-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b9f2-136">RELATED LINKS</span></span>

[<span data-ttu-id="7b9f2-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7b9f2-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="7b9f2-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7b9f2-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="7b9f2-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7b9f2-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="7b9f2-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7b9f2-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


