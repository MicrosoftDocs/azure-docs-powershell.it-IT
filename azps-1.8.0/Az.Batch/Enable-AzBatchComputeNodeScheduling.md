---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2922e9b1a37f714b1ccfb19aea86556b9988ccca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684938"
---
# <span data-ttu-id="70a15-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="70a15-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="70a15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70a15-102">SYNOPSIS</span></span>
<span data-ttu-id="70a15-103">Consente la pianificazione delle attività nel nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="70a15-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="70a15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70a15-104">SYNTAX</span></span>

### <span data-ttu-id="70a15-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70a15-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70a15-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="70a15-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70a15-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70a15-107">DESCRIPTION</span></span>
<span data-ttu-id="70a15-108">Il cmdlet **Enable-AzBatchComputeNodeScheduling** Abilita la pianificazione delle attività nel nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="70a15-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="70a15-109">Un nodo COMPUTE è una macchina virtuale di Azure dedicata a un carico di lavoro specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="70a15-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="70a15-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70a15-110">EXAMPLES</span></span>

### <span data-ttu-id="70a15-111">Esempio 1: abilitare la pianificazione delle attività in un nodo Compute</span><span class="sxs-lookup"><span data-stu-id="70a15-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="70a15-112">Questi comandi consentono la pianificazione delle attività nel nodo di calcolo TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="70a15-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="70a15-113">A questo scopo, il primo comando nell'esempio crea un riferimento a un oggetto contenente le chiavi dell'account per l'account batch contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="70a15-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="70a15-114">Questo riferimento oggetto è archiviato in una variabile denominata $context.</span><span class="sxs-lookup"><span data-stu-id="70a15-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="70a15-115">Il secondo comando usa quindi questo riferimento di oggetto e il cmdlet **Enable-AzBatchComputeNodeScheduling** per connettersi al pool e abilitare la pianificazione delle attività in TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="70a15-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="70a15-116">Esempio 2: abilitare la pianificazione delle attività sui nodi di calcolo in un pool</span><span class="sxs-lookup"><span data-stu-id="70a15-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="70a15-117">Questi comandi consentono la pianificazione delle attività in tutti i nodi di calcolo presenti nel pool Pool06.</span><span class="sxs-lookup"><span data-stu-id="70a15-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="70a15-118">Per eseguire questa attività, il primo comando nell'esempio crea un riferimento a un oggetto contenente le chiavi dell'account per l'account batch contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="70a15-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="70a15-119">Questo riferimento oggetto è archiviato in una variabile denominata $context.</span><span class="sxs-lookup"><span data-stu-id="70a15-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="70a15-120">Il secondo comando nell'esempio usa quindi questo riferimento di oggetto e **Get-AzBatchComputeNode** per restituire una raccolta di tutti i nodi di calcolo trovati in Pool06.</span><span class="sxs-lookup"><span data-stu-id="70a15-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="70a15-121">La raccolta viene quindi inviata tramite pipe al cmdlet **Enable-AzBatchComputeNodeScheduling** , che consente la pianificazione delle attività in ogni nodo COMPUTE della raccolta.</span><span class="sxs-lookup"><span data-stu-id="70a15-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="70a15-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70a15-122">PARAMETERS</span></span>

### <span data-ttu-id="70a15-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="70a15-123">-BatchContext</span></span>
<span data-ttu-id="70a15-124">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="70a15-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="70a15-125">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="70a15-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="70a15-126">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="70a15-126">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="70a15-127">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="70a15-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="70a15-128">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="70a15-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="70a15-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="70a15-129">-ComputeNode</span></span>
<span data-ttu-id="70a15-130">Specifica un riferimento a un oggetto al nodo COMPUTE in cui è abilitata la pianificazione delle attività.</span><span class="sxs-lookup"><span data-stu-id="70a15-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="70a15-131">Questo riferimento all'oggetto viene creato usando il cmdlet Get-AzBatchComputeNode e archiviando l'oggetto compute node restituito in una variabile.</span><span class="sxs-lookup"><span data-stu-id="70a15-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="70a15-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a15-132">-DefaultProfile</span></span>
<span data-ttu-id="70a15-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70a15-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a15-134">-ID</span><span class="sxs-lookup"><span data-stu-id="70a15-134">-Id</span></span>
<span data-ttu-id="70a15-135">Specifica l'ID del nodo COMPUTE in cui è abilitata la pianificazione delle attività.</span><span class="sxs-lookup"><span data-stu-id="70a15-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="70a15-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="70a15-136">-PoolId</span></span>
<span data-ttu-id="70a15-137">Specifica l'ID del pool di batch che contiene il nodo COMPUTE in cui è abilitata la pianificazione delle attività.</span><span class="sxs-lookup"><span data-stu-id="70a15-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="70a15-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a15-138">CommonParameters</span></span>
<span data-ttu-id="70a15-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70a15-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a15-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70a15-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a15-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70a15-141">INPUTS</span></span>

### <span data-ttu-id="70a15-142">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="70a15-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="70a15-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="70a15-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="70a15-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70a15-144">OUTPUTS</span></span>

### <span data-ttu-id="70a15-145">System. void</span><span class="sxs-lookup"><span data-stu-id="70a15-145">System.Void</span></span>

## <span data-ttu-id="70a15-146">Note</span><span class="sxs-lookup"><span data-stu-id="70a15-146">NOTES</span></span>

## <span data-ttu-id="70a15-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70a15-147">RELATED LINKS</span></span>

[<span data-ttu-id="70a15-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="70a15-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


