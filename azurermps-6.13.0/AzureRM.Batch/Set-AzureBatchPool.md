---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: c0f1dc4972e3b71dce74bffb7a72e782774a2734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507612"
---
# <span data-ttu-id="24680-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="24680-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="24680-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24680-102">SYNOPSIS</span></span>
<span data-ttu-id="24680-103">Aggiorna le proprietà di un pool.</span><span class="sxs-lookup"><span data-stu-id="24680-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24680-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24680-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24680-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24680-105">DESCRIPTION</span></span>
<span data-ttu-id="24680-106">Il cmdlet **set-AzureBatchPool** aggiorna le proprietà di un pool nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="24680-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="24680-107">Usa il cmdlet Get-AzureBatchPool per ottenere un oggetto **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="24680-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="24680-108">Modificare le proprietà di tale oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche apportate al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="24680-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="24680-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24680-109">EXAMPLES</span></span>

### <span data-ttu-id="24680-110">Esempio 1: aggiornare un pool</span><span class="sxs-lookup"><span data-stu-id="24680-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="24680-111">Il primo comando ottiene un pool utilizzando **Get-AzureBatchPool** e lo archivia nella variabile $pool.</span><span class="sxs-lookup"><span data-stu-id="24680-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="24680-112">I tre comandi successivi modificano la specifica dell'attività Start nell'oggetto $Pool.</span><span class="sxs-lookup"><span data-stu-id="24680-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="24680-113">Il comando finale aggiorna il servizio batch in base all'oggetto locale in $Pool.</span><span class="sxs-lookup"><span data-stu-id="24680-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="24680-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24680-114">PARAMETERS</span></span>

### <span data-ttu-id="24680-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="24680-115">-BatchContext</span></span>
<span data-ttu-id="24680-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="24680-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="24680-117">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="24680-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="24680-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="24680-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="24680-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="24680-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="24680-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="24680-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="24680-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24680-121">-DefaultProfile</span></span>
<span data-ttu-id="24680-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24680-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24680-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="24680-123">-Pool</span></span>
<span data-ttu-id="24680-124">Specifica il **PSCloudPool** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="24680-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="24680-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24680-125">CommonParameters</span></span>
<span data-ttu-id="24680-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24680-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24680-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24680-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24680-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24680-128">INPUTS</span></span>

### <span data-ttu-id="24680-129">Microsoft.Azure.Commands.Batch. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="24680-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>
<span data-ttu-id="24680-130">Parametri: pool (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24680-130">Parameters: Pool (ByValue)</span></span>

### <span data-ttu-id="24680-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="24680-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="24680-132">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24680-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="24680-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24680-133">OUTPUTS</span></span>

### <span data-ttu-id="24680-134">System. void</span><span class="sxs-lookup"><span data-stu-id="24680-134">System.Void</span></span>

## <span data-ttu-id="24680-135">Note</span><span class="sxs-lookup"><span data-stu-id="24680-135">NOTES</span></span>

## <span data-ttu-id="24680-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24680-136">RELATED LINKS</span></span>

[<span data-ttu-id="24680-137">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="24680-137">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="24680-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="24680-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="24680-139">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="24680-139">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="24680-140">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="24680-140">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="24680-141">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="24680-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


