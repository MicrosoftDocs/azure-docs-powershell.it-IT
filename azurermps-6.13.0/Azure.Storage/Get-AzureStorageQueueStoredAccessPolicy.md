---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: d0daabef3f4fe9ef60a90365054e12e869f0856a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685964"
---
# <span data-ttu-id="c7c38-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c7c38-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="c7c38-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7c38-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c38-103">Ottiene i criteri di accesso archiviati o i criteri per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c38-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7c38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7c38-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7c38-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7c38-105">DESCRIPTION</span></span>
<span data-ttu-id="c7c38-106">Il cmdlet **Get-AzureStorageQueueStoredAccessPolicy** elenca i criteri di accesso archiviati o i criteri per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c38-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="c7c38-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7c38-107">EXAMPLES</span></span>

### <span data-ttu-id="c7c38-108">Esempio 1: ottenere un criterio di accesso archiviato nella coda</span><span class="sxs-lookup"><span data-stu-id="c7c38-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="c7c38-109">Questo comando consente di ottenere i criteri di accesso denominati Policy12 nella coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="c7c38-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="c7c38-110">Esempio 2: ottenere tutti i criteri di accesso archiviati nella coda</span><span class="sxs-lookup"><span data-stu-id="c7c38-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="c7c38-111">Questo comando ottiene tutti i criteri di accesso archiviati nella coda denominata coda.</span><span class="sxs-lookup"><span data-stu-id="c7c38-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="c7c38-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7c38-112">PARAMETERS</span></span>

### <span data-ttu-id="c7c38-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c7c38-113">-Context</span></span>
<span data-ttu-id="c7c38-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c38-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c7c38-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c7c38-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c7c38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c38-116">-DefaultProfile</span></span>
<span data-ttu-id="c7c38-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7c38-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="c7c38-118">-Policy</span></span>
<span data-ttu-id="c7c38-119">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="c7c38-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="c7c38-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="c7c38-120">-Queue</span></span>
<span data-ttu-id="c7c38-121">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c38-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="c7c38-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c38-122">CommonParameters</span></span>
<span data-ttu-id="c7c38-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c38-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c38-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7c38-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c38-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7c38-125">INPUTS</span></span>

### <span data-ttu-id="c7c38-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c7c38-126">System.String</span></span>

### <span data-ttu-id="c7c38-127">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c7c38-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c7c38-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7c38-128">OUTPUTS</span></span>

### <span data-ttu-id="c7c38-129">Microsoft. WindowsAzure. storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="c7c38-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="c7c38-130">Note</span><span class="sxs-lookup"><span data-stu-id="c7c38-130">NOTES</span></span>

## <span data-ttu-id="c7c38-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7c38-131">RELATED LINKS</span></span>

[<span data-ttu-id="c7c38-132">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c7c38-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c7c38-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c7c38-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c7c38-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c7c38-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c7c38-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c7c38-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


