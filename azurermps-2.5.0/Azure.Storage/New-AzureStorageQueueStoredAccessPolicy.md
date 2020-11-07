---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 054a5d979a13f5592f062f729e4c8c393a35134a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866590"
---
# <span data-ttu-id="e02de-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e02de-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="e02de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e02de-102">SYNOPSIS</span></span>
<span data-ttu-id="e02de-103">Crea un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e02de-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e02de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e02de-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e02de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e02de-105">DESCRIPTION</span></span>
<span data-ttu-id="e02de-106">Il cmdlet **New-AzureStorageQueueStoredAccessPolicy** crea un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e02de-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="e02de-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e02de-107">EXAMPLES</span></span>

### <span data-ttu-id="e02de-108">Esempio 1: creare criteri di accesso archiviati in una coda di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e02de-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="e02de-109">Questo comando crea un criterio di accesso denominato Policy01 nella coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="e02de-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="e02de-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e02de-110">PARAMETERS</span></span>

### <span data-ttu-id="e02de-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e02de-111">-Context</span></span>
<span data-ttu-id="e02de-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e02de-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e02de-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e02de-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e02de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02de-114">-DefaultProfile</span></span>
<span data-ttu-id="e02de-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e02de-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e02de-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e02de-116">-ExpiryTime</span></span>
<span data-ttu-id="e02de-117">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="e02de-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="e02de-118">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="e02de-118">-Permission</span></span>
<span data-ttu-id="e02de-119">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e02de-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="e02de-120">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="e02de-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="e02de-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="e02de-121">-Policy</span></span>
<span data-ttu-id="e02de-122">Specifica un nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="e02de-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="e02de-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="e02de-123">-Queue</span></span>
<span data-ttu-id="e02de-124">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e02de-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="e02de-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e02de-125">-StartTime</span></span>
<span data-ttu-id="e02de-126">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="e02de-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="e02de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02de-127">CommonParameters</span></span>
<span data-ttu-id="e02de-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02de-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e02de-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02de-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e02de-130">INPUTS</span></span>

### <span data-ttu-id="e02de-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e02de-131">System.String</span></span>

### <span data-ttu-id="e02de-132">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e02de-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e02de-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e02de-133">OUTPUTS</span></span>

### <span data-ttu-id="e02de-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e02de-134">System.String</span></span>

## <span data-ttu-id="e02de-135">Note</span><span class="sxs-lookup"><span data-stu-id="e02de-135">NOTES</span></span>

## <span data-ttu-id="e02de-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e02de-136">RELATED LINKS</span></span>

[<span data-ttu-id="e02de-137">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e02de-137">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e02de-138">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e02de-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e02de-139">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e02de-139">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e02de-140">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e02de-140">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


