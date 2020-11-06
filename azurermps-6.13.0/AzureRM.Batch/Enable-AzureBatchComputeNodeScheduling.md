---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: e00a1a923afdd8a851416e872028a30ce1e04a55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517603"
---
# <span data-ttu-id="48839-101">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="48839-101">Enable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="48839-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48839-102">SYNOPSIS</span></span>
<span data-ttu-id="48839-103">Consente la pianificazione delle attività nel nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="48839-103">Enables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48839-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48839-104">SYNTAX</span></span>

### <span data-ttu-id="48839-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48839-105">Id (Default)</span></span>
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48839-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="48839-106">InputObject</span></span>
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48839-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48839-107">DESCRIPTION</span></span>
<span data-ttu-id="48839-108">Il cmdlet **Enable-AzureBatchComputeNodeScheduling** Abilita la pianificazione delle attività nel nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="48839-108">The **Enable-AzureBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="48839-109">Un nodo COMPUTE è una macchina virtuale di Azure dedicata a un carico di lavoro specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48839-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="48839-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48839-110">EXAMPLES</span></span>

### <span data-ttu-id="48839-111">Esempio 1: abilitare la pianificazione delle attività in un nodo Compute</span><span class="sxs-lookup"><span data-stu-id="48839-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="48839-112">Questi comandi consentono la pianificazione delle attività nel nodo di calcolo TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="48839-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="48839-113">A questo scopo, il primo comando nell'esempio crea un riferimento a un oggetto contenente le chiavi dell'account per l'account batch contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="48839-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="48839-114">Questo riferimento oggetto è archiviato in una variabile denominata $context.</span><span class="sxs-lookup"><span data-stu-id="48839-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="48839-115">Il secondo comando usa quindi questo riferimento di oggetto e il cmdlet **Enable-AzureBatchComputeNodeScheduling** per connettersi al pool e abilitare la pianificazione delle attività in TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="48839-115">The second command then uses this object reference and the **Enable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="48839-116">Esempio 2: abilitare la pianificazione delle attività sui nodi di calcolo in un pool</span><span class="sxs-lookup"><span data-stu-id="48839-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="48839-117">Questi comandi consentono la pianificazione delle attività in tutti i nodi di calcolo presenti nel pool Pool06.</span><span class="sxs-lookup"><span data-stu-id="48839-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="48839-118">Per eseguire questa attività, il primo comando nell'esempio crea un riferimento a un oggetto contenente le chiavi dell'account per l'account batch contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="48839-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="48839-119">Questo riferimento oggetto è archiviato in una variabile denominata $context.</span><span class="sxs-lookup"><span data-stu-id="48839-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="48839-120">Il secondo comando nell'esempio usa quindi questo riferimento di oggetto e **Get-AzureBatchComputeNode** per restituire una raccolta di tutti i nodi di calcolo trovati in Pool06.</span><span class="sxs-lookup"><span data-stu-id="48839-120">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="48839-121">La raccolta viene quindi inviata tramite pipe al cmdlet **Enable-AzureBatchComputeNodeScheduling** , che consente la pianificazione delle attività in ogni nodo COMPUTE della raccolta.</span><span class="sxs-lookup"><span data-stu-id="48839-121">That collection is then piped to the **Enable-AzureBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="48839-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48839-122">PARAMETERS</span></span>

### <span data-ttu-id="48839-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="48839-123">-BatchContext</span></span>
<span data-ttu-id="48839-124">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="48839-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="48839-125">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="48839-125">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="48839-126">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="48839-126">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="48839-127">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="48839-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="48839-128">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="48839-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="48839-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="48839-129">-ComputeNode</span></span>
<span data-ttu-id="48839-130">Specifica un riferimento a un oggetto al nodo COMPUTE in cui è abilitata la pianificazione delle attività.</span><span class="sxs-lookup"><span data-stu-id="48839-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="48839-131">Questo riferimento all'oggetto viene creato usando il cmdlet Get-AzureBatchComputeNode e archiviando l'oggetto compute node restituito in una variabile.</span><span class="sxs-lookup"><span data-stu-id="48839-131">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48839-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48839-132">-DefaultProfile</span></span>
<span data-ttu-id="48839-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48839-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48839-134">-ID</span><span class="sxs-lookup"><span data-stu-id="48839-134">-Id</span></span>
<span data-ttu-id="48839-135">Specifica l'ID del nodo COMPUTE in cui è abilitata la pianificazione delle attività.</span><span class="sxs-lookup"><span data-stu-id="48839-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48839-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="48839-136">-PoolId</span></span>
<span data-ttu-id="48839-137">Specifica l'ID del pool di batch che contiene il nodo COMPUTE in cui è abilitata la pianificazione delle attività.</span><span class="sxs-lookup"><span data-stu-id="48839-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48839-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48839-138">CommonParameters</span></span>
<span data-ttu-id="48839-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48839-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48839-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48839-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48839-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48839-141">INPUTS</span></span>

### <span data-ttu-id="48839-142">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="48839-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="48839-143">Parametri: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="48839-143">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="48839-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="48839-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="48839-145">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="48839-145">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="48839-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48839-146">OUTPUTS</span></span>

### <span data-ttu-id="48839-147">System. void</span><span class="sxs-lookup"><span data-stu-id="48839-147">System.Void</span></span>

## <span data-ttu-id="48839-148">Note</span><span class="sxs-lookup"><span data-stu-id="48839-148">NOTES</span></span>

## <span data-ttu-id="48839-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48839-149">RELATED LINKS</span></span>

[<span data-ttu-id="48839-150">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="48839-150">Disable-AzureBatchComputeNodeScheduling</span></span>](./Disable-AzureBatchComputeNodeScheduling.md)


