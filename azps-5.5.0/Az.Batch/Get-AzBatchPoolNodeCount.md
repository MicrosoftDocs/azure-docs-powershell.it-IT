---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: b3b1adfe9549a7b04a1e7c6d57542cef8a40cfd7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205259"
---
# <span data-ttu-id="4d9bf-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="4d9bf-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="4d9bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d9bf-102">SYNOPSIS</span></span>
<span data-ttu-id="4d9bf-103">Recupera i conteggi dei nodi batch per stato del nodo raggruppati per ID pool.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="4d9bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d9bf-104">SYNTAX</span></span>

### <span data-ttu-id="4d9bf-105">AzureBatchPoolNodeCounts (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d9bf-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d9bf-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="4d9bf-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d9bf-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="4d9bf-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d9bf-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="4d9bf-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d9bf-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d9bf-109">DESCRIPTION</span></span>
<span data-ttu-id="4d9bf-110">Il Get-AzBatchPoolNodeCount cmdlet consente ai clienti di ottenere il numero di nodi per ogni stato del nodo raggruppato per pool.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="4d9bf-111">Gli stati del nodo possibili sono: creazione, inattività, uscita dal pool, offline, preattivato, riavvio, riutilizzo, in esecuzione, avvio, avvioAttivitàFailed, sconosciuto, inutilizzabile e in attesaForStartTask.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="4d9bf-112">Il cmdlet accetta il parametro PoolId o Pool per filtrare solo il pool con l'ID pool specificato.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="4d9bf-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d9bf-113">EXAMPLES</span></span>

### <span data-ttu-id="4d9bf-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d9bf-114">Example 1</span></span>
```
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="4d9bf-115">Elenca i conteggi dei nodi per stato del nodo per i pool nel contesto dell'account batch corrente.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="4d9bf-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4d9bf-116">Example 2</span></span>

```powershell
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"
PS C:\> $poolnodecounts.Dedicated

Creating            : 1
Idle                : 1
LeavingPool         : 0
Offline             : 0
Preempted           : 0
Rebooting           : 1
Reimaging           : 0
Running             : 5
Starting            : 0
StartTaskFailed     : 0
Total               : 8
Unknown             : 0
Unusable            : 0
WaitingForStartTask : 0

PS C:\> Get-AzBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="4d9bf-117">Visualizzare il numero di nodi per ogni stato del nodo per un ID pool specificato.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="4d9bf-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d9bf-118">PARAMETERS</span></span>

### <span data-ttu-id="4d9bf-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4d9bf-119">-BatchContext</span></span>
<span data-ttu-id="4d9bf-120">Istanza BatchAccountContext da usare quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="4d9bf-121">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="4d9bf-122">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="4d9bf-123">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="4d9bf-124">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4d9bf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d9bf-125">-DefaultProfile</span></span>
<span data-ttu-id="4d9bf-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d9bf-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4d9bf-127">-MaxCount</span></span>
<span data-ttu-id="4d9bf-128">Specifica il numero massimo di pool da restituire.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="4d9bf-129">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-129">The default value is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9bf-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="4d9bf-130">-Pool</span></span>
<span data-ttu-id="4d9bf-131">Specifica **PSCloudPool per** cui ottenere il numero di nodi.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d9bf-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="4d9bf-132">-PoolId</span></span>
<span data-ttu-id="4d9bf-133">ID del pool di cui ottenere il numero di nodi.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-133">The id of the pool for which to get node counts.</span></span>

```yaml
Type: System.String
Parameter Sets: PoolId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d9bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d9bf-134">CommonParameters</span></span>
<span data-ttu-id="4d9bf-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d9bf-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d9bf-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d9bf-137">INPUTS</span></span>

### <span data-ttu-id="4d9bf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4d9bf-138">System.String</span></span>

### <span data-ttu-id="4d9bf-139">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="4d9bf-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="4d9bf-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4d9bf-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4d9bf-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d9bf-141">OUTPUTS</span></span>

### <span data-ttu-id="4d9bf-142">Microsoft.Azure.Commands.Batch. Models.PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="4d9bf-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="4d9bf-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d9bf-143">NOTES</span></span>

## <span data-ttu-id="4d9bf-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d9bf-144">RELATED LINKS</span></span>

[<span data-ttu-id="4d9bf-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4d9bf-145">Get-AzBatchAccountKey</span></span>]()

[<span data-ttu-id="4d9bf-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4d9bf-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="4d9bf-147">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="4d9bf-147">Azure Batch Cmdlets</span></span>]()

