---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: d18a6bdc9a2064e21507c909005692d5d21c63f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518363"
---
# <span data-ttu-id="cc5cf-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cc5cf-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="cc5cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cc5cf-102">SYNOPSIS</span></span>
<span data-ttu-id="cc5cf-103">Aggiorna le proprietà di un pool.</span><span class="sxs-lookup"><span data-stu-id="cc5cf-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc5cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc5cf-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc5cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc5cf-105">DESCRIPTION</span></span>
<span data-ttu-id="cc5cf-106">Il cmdlet **set-AzureBatchPool** aggiorna le proprietà di un pool nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5cf-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="cc5cf-107">Usa il cmdlet Get-AzureBatchPool per ottenere un oggetto **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="cc5cf-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="cc5cf-108">Modificare le proprietà di tale oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche apportate al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="cc5cf-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="cc5cf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc5cf-109">EXAMPLES</span></span>

### <span data-ttu-id="cc5cf-110">Esempio 1: aggiornare un pool</span><span class="sxs-lookup"><span data-stu-id="cc5cf-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="cc5cf-111">Il primo comando ottiene un pool utilizzando **Get-AzureBatchPool** e lo archivia nella variabile $pool.</span><span class="sxs-lookup"><span data-stu-id="cc5cf-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>

<span data-ttu-id="cc5cf-112">I tre comandi successivi modificano la specifica dell'attività Start nell'oggetto $Pool.</span><span class="sxs-lookup"><span data-stu-id="cc5cf-112">The next three commands modify the start task specification on the $Pool object.</span></span>

<span data-ttu-id="cc5cf-113">Il comando finale aggiorna il servizio batch in base all'oggetto locale in $Pool.</span><span class="sxs-lookup"><span data-stu-id="cc5cf-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="cc5cf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cc5cf-114">PARAMETERS</span></span>

### <span data-ttu-id="cc5cf-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cc5cf-115">-BatchContext</span></span>
<span data-ttu-id="cc5cf-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="cc5cf-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cc5cf-117">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="cc5cf-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5cf-118">-Pool</span><span class="sxs-lookup"><span data-stu-id="cc5cf-118">-Pool</span></span>
<span data-ttu-id="cc5cf-119">Specifica il **PSCloudPool** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="cc5cf-119">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc5cf-120">-DefaultProfile</span></span>
<span data-ttu-id="cc5cf-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5cf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc5cf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc5cf-122">CommonParameters</span></span>
<span data-ttu-id="cc5cf-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc5cf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc5cf-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc5cf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc5cf-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cc5cf-125">INPUTS</span></span>

### <span data-ttu-id="cc5cf-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cc5cf-126">BatchAccountContext</span></span>
<span data-ttu-id="cc5cf-127">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="cc5cf-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="cc5cf-128">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="cc5cf-128">PSCloudPool</span></span>
<span data-ttu-id="cc5cf-129">Il parametro "pool" accetta il valore di tipo "PSCloudPool" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="cc5cf-129">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="cc5cf-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc5cf-130">OUTPUTS</span></span>

## <span data-ttu-id="cc5cf-131">Note</span><span class="sxs-lookup"><span data-stu-id="cc5cf-131">NOTES</span></span>

## <span data-ttu-id="cc5cf-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc5cf-132">RELATED LINKS</span></span>

[<span data-ttu-id="cc5cf-133">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cc5cf-133">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="cc5cf-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cc5cf-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cc5cf-135">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cc5cf-135">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="cc5cf-136">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cc5cf-136">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="cc5cf-137">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="cc5cf-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


