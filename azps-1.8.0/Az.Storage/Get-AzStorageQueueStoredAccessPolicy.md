---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 77e51cbc29c740ecd1b7631a8da5f255b6168fa4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676612"
---
# <span data-ttu-id="69edb-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69edb-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="69edb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69edb-102">SYNOPSIS</span></span>
<span data-ttu-id="69edb-103">Ottiene i criteri di accesso archiviati o i criteri per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="69edb-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="69edb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69edb-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69edb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69edb-105">DESCRIPTION</span></span>
<span data-ttu-id="69edb-106">Il cmdlet **Get-AzStorageQueueStoredAccessPolicy** elenca i criteri di accesso archiviati o i criteri per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="69edb-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="69edb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69edb-107">EXAMPLES</span></span>

### <span data-ttu-id="69edb-108">Esempio 1: ottenere un criterio di accesso archiviato nella coda</span><span class="sxs-lookup"><span data-stu-id="69edb-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="69edb-109">Questo comando consente di ottenere i criteri di accesso denominati Policy12 nella coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="69edb-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="69edb-110">Esempio 2: ottenere tutti i criteri di accesso archiviati nella coda</span><span class="sxs-lookup"><span data-stu-id="69edb-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="69edb-111">Questo comando ottiene tutti i criteri di accesso archiviati nella coda denominata coda.</span><span class="sxs-lookup"><span data-stu-id="69edb-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="69edb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69edb-112">PARAMETERS</span></span>

### <span data-ttu-id="69edb-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="69edb-113">-Context</span></span>
<span data-ttu-id="69edb-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="69edb-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="69edb-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="69edb-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="69edb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69edb-116">-DefaultProfile</span></span>
<span data-ttu-id="69edb-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69edb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69edb-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="69edb-118">-Policy</span></span>
<span data-ttu-id="69edb-119">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="69edb-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="69edb-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="69edb-120">-Queue</span></span>
<span data-ttu-id="69edb-121">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="69edb-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="69edb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69edb-122">CommonParameters</span></span>
<span data-ttu-id="69edb-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69edb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69edb-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69edb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69edb-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69edb-125">INPUTS</span></span>

### <span data-ttu-id="69edb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="69edb-126">System.String</span></span>

### <span data-ttu-id="69edb-127">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="69edb-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="69edb-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69edb-128">OUTPUTS</span></span>

### <span data-ttu-id="69edb-129">Microsoft. WindowsAzure. storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="69edb-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="69edb-130">Note</span><span class="sxs-lookup"><span data-stu-id="69edb-130">NOTES</span></span>

## <span data-ttu-id="69edb-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69edb-131">RELATED LINKS</span></span>

[<span data-ttu-id="69edb-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69edb-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="69edb-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69edb-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="69edb-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69edb-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="69edb-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="69edb-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

