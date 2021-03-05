---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: fbd5adc202886ae987f7739ac24d1dadbc0d41d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981437"
---
# <span data-ttu-id="d1285-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1285-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="d1285-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1285-102">SYNOPSIS</span></span>
<span data-ttu-id="d1285-103">Recupera i criteri di accesso archiviati per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d1285-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="d1285-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1285-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1285-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d1285-105">DESCRIPTION</span></span>
<span data-ttu-id="d1285-106">Il cmdlet **Get-AzStorageQueueStoredAccessPolicy** elenca i criteri di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d1285-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="d1285-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1285-107">EXAMPLES</span></span>

### <span data-ttu-id="d1285-108">Esempio 1: Ottenere criteri di accesso archiviati nella coda</span><span class="sxs-lookup"><span data-stu-id="d1285-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="d1285-109">Questo comando recupera i criteri di accesso denominati Policy12 nella coda di archiviazione denominata MyQueue.</span><span class="sxs-lookup"><span data-stu-id="d1285-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="d1285-110">Esempio 2: Recuperare tutti i criteri di accesso archiviato nella coda</span><span class="sxs-lookup"><span data-stu-id="d1285-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="d1285-111">Questo comando recupera tutti i criteri di accesso archiviati nella coda denominata MyQueue.</span><span class="sxs-lookup"><span data-stu-id="d1285-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="d1285-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1285-112">PARAMETERS</span></span>

### <span data-ttu-id="d1285-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d1285-113">-Context</span></span>
<span data-ttu-id="d1285-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d1285-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d1285-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d1285-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d1285-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1285-116">-DefaultProfile</span></span>
<span data-ttu-id="d1285-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1285-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1285-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="d1285-118">-Policy</span></span>
<span data-ttu-id="d1285-119">Specifica i criteri di accesso archiviato, che includono le autorizzazioni per questo token di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="d1285-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="d1285-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="d1285-120">-Queue</span></span>
<span data-ttu-id="d1285-121">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d1285-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="d1285-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1285-122">CommonParameters</span></span>
<span data-ttu-id="d1285-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1285-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1285-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1285-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1285-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="d1285-125">INPUTS</span></span>

### <span data-ttu-id="d1285-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d1285-126">System.String</span></span>

### <span data-ttu-id="d1285-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1285-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d1285-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1285-128">OUTPUTS</span></span>

### <span data-ttu-id="d1285-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="d1285-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="d1285-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="d1285-130">NOTES</span></span>

## <span data-ttu-id="d1285-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1285-131">RELATED LINKS</span></span>

[<span data-ttu-id="d1285-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1285-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d1285-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1285-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d1285-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1285-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d1285-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1285-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


