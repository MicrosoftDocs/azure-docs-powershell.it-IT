---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f676f644cb69880a0b403a4e656ce9cb435b7c77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002382"
---
# <span data-ttu-id="9913e-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9913e-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="9913e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9913e-102">SYNOPSIS</span></span>
<span data-ttu-id="9913e-103">Crea criteri di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9913e-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="9913e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9913e-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9913e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9913e-105">DESCRIPTION</span></span>
<span data-ttu-id="9913e-106">Il cmdlet **New-AzStorageQueueStoredAccessPolicy** crea un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9913e-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="9913e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9913e-107">EXAMPLES</span></span>

### <span data-ttu-id="9913e-108">Esempio 1: Creare criteri di accesso archiviato in una coda di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9913e-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="9913e-109">Questo comando crea un criterio di accesso denominato Policy01 nella coda di archiviazione denominata MyQueue.</span><span class="sxs-lookup"><span data-stu-id="9913e-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="9913e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9913e-110">PARAMETERS</span></span>

### <span data-ttu-id="9913e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9913e-111">-Context</span></span>
<span data-ttu-id="9913e-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9913e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9913e-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9913e-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9913e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9913e-114">-DefaultProfile</span></span>
<span data-ttu-id="9913e-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9913e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9913e-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9913e-116">-ExpiryTime</span></span>
<span data-ttu-id="9913e-117">Specifica l'ora in cui i criteri di accesso archiviato non sono più validi.</span><span class="sxs-lookup"><span data-stu-id="9913e-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="9913e-118">-Permission</span><span class="sxs-lookup"><span data-stu-id="9913e-118">-Permission</span></span>
<span data-ttu-id="9913e-119">Specifica le autorizzazioni nei criteri di accesso archiviato per accedere alla coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9913e-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="9913e-120">È importante notare che si tratta di una stringa, ad esempio `rwd` (per Lettura, Scrittura ed Elimina).</span><span class="sxs-lookup"><span data-stu-id="9913e-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="9913e-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="9913e-121">-Policy</span></span>
<span data-ttu-id="9913e-122">Specifica un nome per i criteri di accesso archiviato.</span><span class="sxs-lookup"><span data-stu-id="9913e-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="9913e-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="9913e-123">-Queue</span></span>
<span data-ttu-id="9913e-124">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9913e-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="9913e-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9913e-125">-StartTime</span></span>
<span data-ttu-id="9913e-126">Specifica l'ora in cui i criteri di accesso archiviato diventano validi.</span><span class="sxs-lookup"><span data-stu-id="9913e-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="9913e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9913e-127">CommonParameters</span></span>
<span data-ttu-id="9913e-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9913e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9913e-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9913e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9913e-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="9913e-130">INPUTS</span></span>

### <span data-ttu-id="9913e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9913e-131">System.String</span></span>

### <span data-ttu-id="9913e-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9913e-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9913e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9913e-133">OUTPUTS</span></span>

### <span data-ttu-id="9913e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9913e-134">System.String</span></span>

## <span data-ttu-id="9913e-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="9913e-135">NOTES</span></span>

## <span data-ttu-id="9913e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9913e-136">RELATED LINKS</span></span>

[<span data-ttu-id="9913e-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9913e-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9913e-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9913e-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="9913e-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9913e-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9913e-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9913e-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


