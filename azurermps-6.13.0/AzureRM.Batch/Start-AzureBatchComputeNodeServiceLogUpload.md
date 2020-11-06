---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/Start-AzureBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 8f171b42e3f1e1f087890ec451d5a3ff13cb8c57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517559"
---
# <span data-ttu-id="75914-101">Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="75914-101">Start-AzureBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="75914-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75914-102">SYNOPSIS</span></span>
<span data-ttu-id="75914-103">Caricare i file di log del servizio compute node in un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="75914-103">Upload compute node service log files to an Azure Storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75914-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75914-104">SYNTAX</span></span>

### <span data-ttu-id="75914-105">AzureBatchComputeNodeServiceLogUpload (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75914-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime>
 [-EndTime <DateTime>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75914-106">ID</span><span class="sxs-lookup"><span data-stu-id="75914-106">Id</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String>
 [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75914-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="75914-107">ParentObject</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75914-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75914-108">DESCRIPTION</span></span>
<span data-ttu-id="75914-109">Questo cmdlet raccoglie i file di log del servizio batch di Azure dai nodi compute se si verifica un errore e si vuole eseguire l'escalation del supporto di Azure.</span><span class="sxs-lookup"><span data-stu-id="75914-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="75914-110">I file di log del servizio batch di Azure devono essere condivisi con il supporto di Azure per facilitare i problemi di debug con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="75914-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="75914-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75914-111">EXAMPLES</span></span>

### <span data-ttu-id="75914-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75914-112">Example 1</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="75914-113">Caricare i registri dei servizi compute node scritti o dopo il 1 ° gennaio 2018 a mezzanotte, ottenuti dal nodo COMPUTE, in base all'ID pool del pool in cui si trova il nodo COMPUTE e all'ID del nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="75914-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="75914-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="75914-114">Example 2</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="75914-115">Caricare i registri dei servizi compute node scritti in o dopo il 1 ° gennaio 2018 mezzanotte e prima del 10 gennaio 2018 mezzanotte, ottenuti dal nodo COMPUTE, con ID pool del pool in cui si trova il nodo COMPUTE e l'ID del nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="75914-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="75914-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="75914-116">Example 3</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzureBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="75914-117">Caricare i registri dei servizi compute node scritti in o dopo il 1 ° gennaio 2018 a mezzanotte e prima del 10 gennaio 2018 a mezzanotte, ottenuti dall'oggetto compute node.</span><span class="sxs-lookup"><span data-stu-id="75914-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="75914-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75914-118">PARAMETERS</span></span>

### <span data-ttu-id="75914-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="75914-119">-BatchContext</span></span>
<span data-ttu-id="75914-120">Istanza di BatchAccountContext da usare per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="75914-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="75914-121">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="75914-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="75914-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="75914-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="75914-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="75914-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="75914-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="75914-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="75914-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="75914-125">-ComputeNode</span></span>
<span data-ttu-id="75914-126">Specifica l'oggetto **PSComputeNode** da cui vengono recuperati i registri dei servizi.</span><span class="sxs-lookup"><span data-stu-id="75914-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75914-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="75914-127">-ComputeNodeId</span></span>
<span data-ttu-id="75914-128">ID del nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="75914-128">The id of the compute node.</span></span>

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

### <span data-ttu-id="75914-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="75914-129">-ContainerUrl</span></span>
<span data-ttu-id="75914-130">URL del contenitore per l'archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="75914-130">The container url to Azure Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75914-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75914-131">-DefaultProfile</span></span>
<span data-ttu-id="75914-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75914-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75914-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="75914-133">-EndTime</span></span>
<span data-ttu-id="75914-134">Ora di fine del log del servizio da caricare (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="75914-134">The end time of service log to be uploaded (optional).</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75914-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="75914-135">-PoolId</span></span>
<span data-ttu-id="75914-136">ID del pool che contiene il nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="75914-136">The id of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="75914-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="75914-137">-StartTime</span></span>
<span data-ttu-id="75914-138">Ora di inizio del log del servizio da caricare.</span><span class="sxs-lookup"><span data-stu-id="75914-138">The start time of service log to be uploaded.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75914-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="75914-139">-Confirm</span></span>
<span data-ttu-id="75914-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75914-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75914-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75914-141">-WhatIf</span></span>
<span data-ttu-id="75914-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75914-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75914-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75914-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75914-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75914-144">CommonParameters</span></span>
<span data-ttu-id="75914-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75914-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75914-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75914-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75914-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75914-147">INPUTS</span></span>

### <span data-ttu-id="75914-148">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="75914-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="75914-149">Parametri: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="75914-149">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="75914-150">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="75914-150">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="75914-151">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="75914-151">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="75914-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75914-152">OUTPUTS</span></span>

### <span data-ttu-id="75914-153">Microsoft.Azure.Commands.Batch. Models. PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="75914-153">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="75914-154">Note</span><span class="sxs-lookup"><span data-stu-id="75914-154">NOTES</span></span>

## <span data-ttu-id="75914-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75914-155">RELATED LINKS</span></span>
