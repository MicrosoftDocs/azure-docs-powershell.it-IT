---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: 0390e6f156e305c3ba5f34d78dcf33520098bee3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675658"
---
# <span data-ttu-id="d2d9f-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="d2d9f-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="d2d9f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d9f-103">Ottiene i conteggi dei nodi batch per stato di nodo raggruppati per ID pool.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="d2d9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2d9f-104">SYNTAX</span></span>

### <span data-ttu-id="d2d9f-105">AzureBatchPoolNodeCounts (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2d9f-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2d9f-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="d2d9f-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2d9f-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="d2d9f-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2d9f-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="d2d9f-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2d9f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2d9f-109">DESCRIPTION</span></span>
<span data-ttu-id="d2d9f-110">Il cmdlet Get-AzBatchPoolNodeCount consente ai clienti di recuperare i conteggi dei nodi per ogni stato del nodo raggruppati per pool.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="d2d9f-111">I possibili stati dei nodi sono la creazione, il minimo, leavingPool, offline, interrotto, il riavvio, la rigenerazione, l'avvio, l'avviamento, startTaskFailed, sconosciuto, inutilizzabile e waitingForStartTask.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="d2d9f-112">Il cmdlet accetta il parametro PoolId o pool per filtrare solo il pool con l'ID del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="d2d9f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2d9f-113">EXAMPLES</span></span>

### <span data-ttu-id="d2d9f-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d2d9f-114">Example 1</span></span>

```powershell
PS C:\> $batchContext = Get-AzBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="d2d9f-115">I conteggi dei nodi elenco per lo stato del nodo per i pool in contesto dell'account batch corrente.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="d2d9f-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d2d9f-116">Example 2</span></span>

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

<span data-ttu-id="d2d9f-117">Mostra conteggi nodi per stato di nodo per un pool di ID pool specificati.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="d2d9f-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2d9f-118">PARAMETERS</span></span>

### <span data-ttu-id="d2d9f-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d2d9f-119">-BatchContext</span></span>
<span data-ttu-id="d2d9f-120">Istanza di BatchAccountContext da usare per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="d2d9f-121">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="d2d9f-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="d2d9f-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="d2d9f-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d2d9f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2d9f-125">-DefaultProfile</span></span>
<span data-ttu-id="d2d9f-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2d9f-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d2d9f-127">-MaxCount</span></span>
<span data-ttu-id="d2d9f-128">Specifica il numero massimo di pool da restituire.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="d2d9f-129">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-129">The default value is 10.</span></span>

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

### <span data-ttu-id="d2d9f-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="d2d9f-130">-Pool</span></span>
<span data-ttu-id="d2d9f-131">Specifica il **PSCloudPool** per cui ottenere i conteggi dei nodi.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

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

### <span data-ttu-id="d2d9f-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d2d9f-132">-PoolId</span></span>
<span data-ttu-id="d2d9f-133">ID del pool per cui ottenere i conteggi dei nodi.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-133">The id of the pool for which to get node counts.</span></span>

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

### <span data-ttu-id="d2d9f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d9f-134">CommonParameters</span></span>
<span data-ttu-id="d2d9f-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2d9f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d9f-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2d9f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d9f-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2d9f-137">INPUTS</span></span>

### <span data-ttu-id="d2d9f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d2d9f-138">System.String</span></span>

### <span data-ttu-id="d2d9f-139">Microsoft.Azure.Commands.Batch. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="d2d9f-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="d2d9f-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d2d9f-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d2d9f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2d9f-141">OUTPUTS</span></span>

### <span data-ttu-id="d2d9f-142">Microsoft.Azure.Commands.Batch. Models. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="d2d9f-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="d2d9f-143">Note</span><span class="sxs-lookup"><span data-stu-id="d2d9f-143">NOTES</span></span>

## <span data-ttu-id="d2d9f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2d9f-144">RELATED LINKS</span></span>

[<span data-ttu-id="d2d9f-145">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d2d9f-145">Get-AzBatchAccountKeys</span></span>]()

[<span data-ttu-id="d2d9f-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d2d9f-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="d2d9f-147">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="d2d9f-147">Azure Batch Cmdlets</span></span>]()

