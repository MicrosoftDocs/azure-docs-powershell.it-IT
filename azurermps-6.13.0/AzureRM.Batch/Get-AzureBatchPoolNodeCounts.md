---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolnodecounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolNodeCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolNodeCounts.md
ms.openlocfilehash: 6cd15b6a8ee59982bf328f751a20807835f54513
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686642"
---
# <span data-ttu-id="b9121-101">Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="b9121-101">Get-AzureBatchPoolNodeCounts</span></span>

## <span data-ttu-id="b9121-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9121-102">SYNOPSIS</span></span>
<span data-ttu-id="b9121-103">Ottiene i conteggi dei nodi batch per stato di nodo raggruppati per ID pool.</span><span class="sxs-lookup"><span data-stu-id="b9121-103">Gets Batch node counts per node state grouped by pool id.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9121-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9121-104">SYNTAX</span></span>

### <span data-ttu-id="b9121-105">AzureBatchPoolNodeCounts (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9121-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzureBatchPoolNodeCounts -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9121-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="b9121-106">PoolId</span></span>
```
Get-AzureBatchPoolNodeCounts [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9121-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="b9121-107">ParentObject</span></span>
```
Get-AzureBatchPoolNodeCounts [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9121-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="b9121-108">ODataFilter</span></span>
```
Get-AzureBatchPoolNodeCounts [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9121-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9121-109">DESCRIPTION</span></span>
<span data-ttu-id="b9121-110">Il cmdlet Get-AzureBatchPoolNodeCounts consente ai clienti di recuperare i conteggi dei nodi per ogni stato del nodo raggruppati per pool.</span><span class="sxs-lookup"><span data-stu-id="b9121-110">The Get-AzureBatchPoolNodeCounts cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="b9121-111">I possibili stati dei nodi sono la creazione, il minimo, leavingPool, offline, interrotto, il riavvio, la rigenerazione, l'avvio, l'avviamento, startTaskFailed, sconosciuto, inutilizzabile e waitingForStartTask.</span><span class="sxs-lookup"><span data-stu-id="b9121-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="b9121-112">Il cmdlet accetta il parametro PoolId o pool per filtrare solo il pool con l'ID del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="b9121-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="b9121-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9121-113">EXAMPLES</span></span>

### <span data-ttu-id="b9121-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b9121-114">Example 1</span></span>

```powershell
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzureBatchPoolNodeCounts -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="b9121-115">I conteggi dei nodi elenco per lo stato del nodo per i pool in contesto dell'account batch corrente.</span><span class="sxs-lookup"><span data-stu-id="b9121-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="b9121-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b9121-116">Example 2</span></span>

```powershell
PS C:\> Get-AzureBatchPoolNodeCounts -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzureBatchPoolNodeCounts -BatchContext $batchContext -PoolId "contosopool1"
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

PS C:\> Get-AzureBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzureBatchPoolNodeCounts -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="b9121-117">Mostra conteggi nodi per stato di nodo per un pool di ID pool specificati.</span><span class="sxs-lookup"><span data-stu-id="b9121-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="b9121-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9121-118">PARAMETERS</span></span>

### <span data-ttu-id="b9121-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b9121-119">-BatchContext</span></span>
<span data-ttu-id="b9121-120">Istanza di BatchAccountContext da usare per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b9121-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="b9121-121">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b9121-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="b9121-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="b9121-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="b9121-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b9121-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="b9121-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b9121-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b9121-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9121-125">-DefaultProfile</span></span>
<span data-ttu-id="b9121-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9121-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9121-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b9121-127">-MaxCount</span></span>
<span data-ttu-id="b9121-128">Specifica il numero massimo di pool da restituire.</span><span class="sxs-lookup"><span data-stu-id="b9121-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="b9121-129">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="b9121-129">The default value is 10.</span></span>

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

### <span data-ttu-id="b9121-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="b9121-130">-Pool</span></span>
<span data-ttu-id="b9121-131">Specifica il **PSCloudPool** per cui ottenere i conteggi dei nodi.</span><span class="sxs-lookup"><span data-stu-id="b9121-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

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

### <span data-ttu-id="b9121-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b9121-132">-PoolId</span></span>
<span data-ttu-id="b9121-133">ID del pool per cui ottenere i conteggi dei nodi.</span><span class="sxs-lookup"><span data-stu-id="b9121-133">The id of the pool for which to get node counts.</span></span>

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

### <span data-ttu-id="b9121-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9121-134">CommonParameters</span></span>
<span data-ttu-id="b9121-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9121-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9121-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9121-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9121-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9121-137">INPUTS</span></span>

### <span data-ttu-id="b9121-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b9121-138">System.String</span></span>

### <span data-ttu-id="b9121-139">Microsoft.Azure.Commands.Batch. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="b9121-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>
<span data-ttu-id="b9121-140">Parametri: pool (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b9121-140">Parameters: Pool (ByValue)</span></span>

### <span data-ttu-id="b9121-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b9121-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="b9121-142">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b9121-142">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="b9121-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9121-143">OUTPUTS</span></span>

### <span data-ttu-id="b9121-144">Microsoft.Azure.Commands.Batch. Models. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="b9121-144">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="b9121-145">Note</span><span class="sxs-lookup"><span data-stu-id="b9121-145">NOTES</span></span>

## <span data-ttu-id="b9121-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9121-146">RELATED LINKS</span></span>

[<span data-ttu-id="b9121-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b9121-147">Get-AzureRmBatchAccountKeys</span></span>]()

[<span data-ttu-id="b9121-148">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b9121-148">Get-AzureBatchJob</span></span>]()

[<span data-ttu-id="b9121-149">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="b9121-149">Azure Batch Cmdlets</span></span>]()

