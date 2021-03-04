---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/Start-AzBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 84d0d1711c9ed29aa48c4845787529a46686da0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975950"
---
# <span data-ttu-id="062f3-101">Start-AzBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="062f3-101">Start-AzBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="062f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="062f3-102">SYNOPSIS</span></span>
<span data-ttu-id="062f3-103">Caricare i file di log del servizio nodo di elaborazione in un contenitore Di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="062f3-103">Upload compute node service log files to an Azure Storage container.</span></span>

## <span data-ttu-id="062f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="062f3-104">SYNTAX</span></span>

### <span data-ttu-id="062f3-105">AzureBatchComputeNodeServiceLogUpload (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="062f3-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="062f3-106">ID</span><span class="sxs-lookup"><span data-stu-id="062f3-106">Id</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="062f3-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="062f3-107">ParentObject</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="062f3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="062f3-108">DESCRIPTION</span></span>
<span data-ttu-id="062f3-109">Questo cmdlet raccoglie i file di log del servizio batch di Azure dai nodi di calcolo se si verifica un errore e si vuole eseguire l'escalation al supporto di Azure.</span><span class="sxs-lookup"><span data-stu-id="062f3-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="062f3-110">I file di log del servizio batch di Azure devono essere condivisi con il supporto di Azure per facilitare i problemi di debug con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="062f3-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="062f3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="062f3-111">EXAMPLES</span></span>

### <span data-ttu-id="062f3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="062f3-112">Example 1</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="062f3-113">Caricare i log dei servizi nodo di elaborazione scritti a mezzanotte del 1° gennaio 2018 o dopo la mezzanotte del 1° gennaio 2018, ottenute dal nodo di elaborazione, in base all'ID pool del pool in cui si trova il nodo di elaborazione e all'ID nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="062f3-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="062f3-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="062f3-114">Example 2</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="062f3-115">Caricare i log dei servizi nodo di elaborazione scritti a mezzanotte o dopo il 1° gennaio 2018 e prima della mezzanotte del 10 gennaio 2018, ottenute dal nodo di elaborazione, in base all'ID pool del pool in cui si trova il nodo di elaborazione e all'ID nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="062f3-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="062f3-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="062f3-116">Example 3</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="062f3-117">Caricare i log dei servizi nodo di elaborazione scritti in o dopo la mezzanotte del 1° gennaio 2018 e prima della mezzanotte del 10 gennaio 2018, ottenute dall'oggetto nodo di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="062f3-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="062f3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="062f3-118">PARAMETERS</span></span>

### <span data-ttu-id="062f3-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="062f3-119">-BatchContext</span></span>
<span data-ttu-id="062f3-120">Istanza BatchAccountContext da usare quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="062f3-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="062f3-121">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="062f3-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="062f3-122">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="062f3-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="062f3-123">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="062f3-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="062f3-124">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="062f3-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="062f3-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="062f3-125">-ComputeNode</span></span>
<span data-ttu-id="062f3-126">Specifica **l'oggetto PSComputeNode** da cui vengono recuperati i log del servizio.</span><span class="sxs-lookup"><span data-stu-id="062f3-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

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

### <span data-ttu-id="062f3-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="062f3-127">-ComputeNodeId</span></span>
<span data-ttu-id="062f3-128">ID del nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="062f3-128">The id of the compute node.</span></span>

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

### <span data-ttu-id="062f3-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="062f3-129">-ContainerUrl</span></span>
<span data-ttu-id="062f3-130">L'URL del contenitore per Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="062f3-130">The container url to Azure Storage.</span></span>

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

### <span data-ttu-id="062f3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="062f3-131">-DefaultProfile</span></span>
<span data-ttu-id="062f3-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="062f3-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="062f3-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="062f3-133">-EndTime</span></span>
<span data-ttu-id="062f3-134">Ora di fine del log del servizio da caricare (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="062f3-134">The end time of service log to be uploaded (optional).</span></span>

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

### <span data-ttu-id="062f3-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="062f3-135">-PoolId</span></span>
<span data-ttu-id="062f3-136">ID del pool che contiene il nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="062f3-136">The id of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="062f3-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="062f3-137">-StartTime</span></span>
<span data-ttu-id="062f3-138">Ora di inizio del log del servizio da caricare.</span><span class="sxs-lookup"><span data-stu-id="062f3-138">The start time of service log to be uploaded.</span></span>

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

### <span data-ttu-id="062f3-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="062f3-139">-Confirm</span></span>
<span data-ttu-id="062f3-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="062f3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="062f3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="062f3-141">-WhatIf</span></span>
<span data-ttu-id="062f3-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="062f3-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="062f3-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="062f3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="062f3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="062f3-144">CommonParameters</span></span>
<span data-ttu-id="062f3-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="062f3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="062f3-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="062f3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="062f3-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="062f3-147">INPUTS</span></span>

### <span data-ttu-id="062f3-148">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="062f3-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="062f3-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="062f3-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="062f3-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="062f3-150">OUTPUTS</span></span>

### <span data-ttu-id="062f3-151">Microsoft.Azure.Commands.Batch. Models.PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="062f3-151">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="062f3-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="062f3-152">NOTES</span></span>

## <span data-ttu-id="062f3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="062f3-153">RELATED LINKS</span></span>
