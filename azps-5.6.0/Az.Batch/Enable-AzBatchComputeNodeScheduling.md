---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2897a21f25ac0a91fec11d83b77c8219d12f88ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995720"
---
# <span data-ttu-id="92e30-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="92e30-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="92e30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92e30-102">SYNOPSIS</span></span>
<span data-ttu-id="92e30-103">Abilita la programmazione delle attività nel nodo di elaborazione specificato.</span><span class="sxs-lookup"><span data-stu-id="92e30-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="92e30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92e30-104">SYNTAX</span></span>

### <span data-ttu-id="92e30-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="92e30-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92e30-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="92e30-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92e30-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="92e30-107">DESCRIPTION</span></span>
<span data-ttu-id="92e30-108">Il cmdlet **Enable-AzBatchComputeNodeScheduling** abilita la pianificazione delle attività nel nodo di elaborazione specificato.</span><span class="sxs-lookup"><span data-stu-id="92e30-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="92e30-109">Un nodo di elaborazione è una macchina virtuale di Azure dedicata a un carico di lavoro specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="92e30-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="92e30-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92e30-110">EXAMPLES</span></span>

### <span data-ttu-id="92e30-111">Esempio 1: Abilitare la programmazione delle attività in un nodo di calcolo</span><span class="sxs-lookup"><span data-stu-id="92e30-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="92e30-112">Questi comandi abilitano la pianificazione delle attività nel nodo di elaborazione tvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="92e30-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="92e30-113">A questo scopo, il primo comando dell'esempio crea un riferimento a un oggetto contenente le chiavi dell'account batch contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="92e30-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="92e30-114">Questo riferimento all'oggetto è archiviato in una variabile denominata $context.</span><span class="sxs-lookup"><span data-stu-id="92e30-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="92e30-115">Il secondo comando usa quindi questo riferimento all'oggetto e il cmdlet **Enable-AzBatchComputeNodeScheduling** per connettersi al pool myPool e abilitare la pianificazione delle attività in tvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="92e30-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="92e30-116">Esempio 2: Abilitare la pianificazione delle attività nei nodi di calcolo in un pool</span><span class="sxs-lookup"><span data-stu-id="92e30-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="92e30-117">Questi comandi abilitano la pianificazione delle attività in tutti i nodi di elaborazione trovati nel pool Pool06.</span><span class="sxs-lookup"><span data-stu-id="92e30-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="92e30-118">Per eseguire questa attività, il primo comando dell'esempio crea un riferimento a un oggetto contenente le chiavi dell'account batch contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="92e30-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="92e30-119">Questo riferimento all'oggetto è archiviato in una variabile denominata $context.</span><span class="sxs-lookup"><span data-stu-id="92e30-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="92e30-120">Il secondo comando nell'esempio usa quindi questo riferimento all'oggetto e **Get-AzBatchComputeNode** per restituire una raccolta di tutti i nodi di calcolo trovati in Pool06.</span><span class="sxs-lookup"><span data-stu-id="92e30-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="92e30-121">Questa raccolta viene quindi reindirizzata al cmdlet **Enable-AzBatchComputeNodeScheduling,** che consente la pianificazione delle attività in ogni nodo di calcolo nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="92e30-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="92e30-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92e30-122">PARAMETERS</span></span>

### <span data-ttu-id="92e30-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="92e30-123">-BatchContext</span></span>
<span data-ttu-id="92e30-124">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="92e30-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="92e30-125">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="92e30-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="92e30-126">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="92e30-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="92e30-127">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="92e30-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="92e30-128">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="92e30-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="92e30-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="92e30-129">-ComputeNode</span></span>
<span data-ttu-id="92e30-130">Specifica un riferimento a un oggetto al nodo di calcolo in cui è abilitata la programmazione delle attività.</span><span class="sxs-lookup"><span data-stu-id="92e30-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="92e30-131">Questo riferimento all'oggetto viene creato usando il cmdlet Get-AzBatchComputeNode e archiviando l'oggetto nodo di calcolo restituito in una variabile.</span><span class="sxs-lookup"><span data-stu-id="92e30-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="92e30-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e30-132">-DefaultProfile</span></span>
<span data-ttu-id="92e30-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92e30-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92e30-134">-Id</span><span class="sxs-lookup"><span data-stu-id="92e30-134">-Id</span></span>
<span data-ttu-id="92e30-135">Specifica l'ID del nodo di calcolo in cui è abilitata la programmazione delle attività.</span><span class="sxs-lookup"><span data-stu-id="92e30-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="92e30-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="92e30-136">-PoolId</span></span>
<span data-ttu-id="92e30-137">Specifica l'ID del pool batch che contiene il nodo di calcolo in cui è abilitata la programmazione delle attività.</span><span class="sxs-lookup"><span data-stu-id="92e30-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="92e30-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e30-138">CommonParameters</span></span>
<span data-ttu-id="92e30-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e30-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e30-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92e30-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e30-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="92e30-141">INPUTS</span></span>

### <span data-ttu-id="92e30-142">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="92e30-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="92e30-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="92e30-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="92e30-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92e30-144">OUTPUTS</span></span>

### <span data-ttu-id="92e30-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="92e30-145">System.Void</span></span>

## <span data-ttu-id="92e30-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="92e30-146">NOTES</span></span>

## <span data-ttu-id="92e30-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92e30-147">RELATED LINKS</span></span>

[<span data-ttu-id="92e30-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="92e30-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


