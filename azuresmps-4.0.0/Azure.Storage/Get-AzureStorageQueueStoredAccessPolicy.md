---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552b1e638034cf0cec5825b742af4984b688cec3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507059"
---
# <span data-ttu-id="9e182-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9e182-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="9e182-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e182-102">SYNOPSIS</span></span>
<span data-ttu-id="9e182-103">Ottiene i criteri di accesso archiviati o i criteri per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e182-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="9e182-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e182-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e182-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e182-105">DESCRIPTION</span></span>
<span data-ttu-id="9e182-106">Il cmdlet **Get-AzureStorageQueueStoredAccessPolicy** elenca i criteri di accesso archiviati o i criteri per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e182-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="9e182-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e182-107">EXAMPLES</span></span>

### <span data-ttu-id="9e182-108">Esempio 1: ottenere un criterio di accesso archiviato nella coda</span><span class="sxs-lookup"><span data-stu-id="9e182-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="9e182-109">Questo comando consente di ottenere i criteri di accesso denominati Policy12 nella coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="9e182-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="9e182-110">Esempio 2: ottenere tutti i criteri di accesso archiviati nella coda</span><span class="sxs-lookup"><span data-stu-id="9e182-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="9e182-111">Questo comando ottiene tutti i criteri di accesso archiviati nella coda denominata coda.</span><span class="sxs-lookup"><span data-stu-id="9e182-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="9e182-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e182-112">PARAMETERS</span></span>

### <span data-ttu-id="9e182-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9e182-113">-Context</span></span>
<span data-ttu-id="9e182-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e182-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9e182-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9e182-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9e182-116">-Policy</span><span class="sxs-lookup"><span data-stu-id="9e182-116">-Policy</span></span>
<span data-ttu-id="9e182-117">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="9e182-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e182-118">-Queue</span><span class="sxs-lookup"><span data-stu-id="9e182-118">-Queue</span></span>
<span data-ttu-id="9e182-119">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e182-119">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="9e182-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e182-120">CommonParameters</span></span>
<span data-ttu-id="9e182-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e182-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e182-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e182-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e182-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e182-123">INPUTS</span></span>

## <span data-ttu-id="9e182-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e182-124">OUTPUTS</span></span>

## <span data-ttu-id="9e182-125">Note</span><span class="sxs-lookup"><span data-stu-id="9e182-125">NOTES</span></span>

## <span data-ttu-id="9e182-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e182-126">RELATED LINKS</span></span>

[<span data-ttu-id="9e182-127">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9e182-127">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9e182-128">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9e182-128">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9e182-129">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9e182-129">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9e182-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9e182-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


