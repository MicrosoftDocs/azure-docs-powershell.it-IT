---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 3a9534ea2fd0f1bcfc17f9eb5df63b25f7760f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517051"
---
# <span data-ttu-id="db79d-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="db79d-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="db79d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db79d-102">SYNOPSIS</span></span>
<span data-ttu-id="db79d-103">Crea un pool nel servizio batch.</span><span class="sxs-lookup"><span data-stu-id="db79d-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db79d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db79d-104">SYNTAX</span></span>

### <span data-ttu-id="db79d-105">CloudServiceAndTargetDedicated (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db79d-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db79d-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="db79d-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db79d-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="db79d-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db79d-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="db79d-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db79d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db79d-109">DESCRIPTION</span></span>
<span data-ttu-id="db79d-110">Il cmdlet **New-AzureBatchPool** crea un pool nel servizio batch di Azure sotto l'account specificato dal parametro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="db79d-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="db79d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db79d-111">EXAMPLES</span></span>

### <span data-ttu-id="db79d-112">Esempio 1: creare un nuovo pool usando il set di parametri TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="db79d-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicated 3 -BatchContext $Context
```

<span data-ttu-id="db79d-113">Questo comando crea un nuovo pool con ID pool con il set di parametri TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="db79d-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="db79d-114">L'allocazione di destinazione è tre nodi compute.</span><span class="sxs-lookup"><span data-stu-id="db79d-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="db79d-115">Il pool è configurato per l'uso di piccole macchine virtuali con la versione più recente del sistema operativo della famiglia quattro.</span><span class="sxs-lookup"><span data-stu-id="db79d-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="db79d-116">Esempio 2: creare un nuovo pool usando il set di parametri di scalabilità verticale</span><span class="sxs-lookup"><span data-stu-id="db79d-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="db79d-117">Questo comando crea un nuovo pool con ID AutoScalePool con il set di parametri autoscale.</span><span class="sxs-lookup"><span data-stu-id="db79d-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="db79d-118">Il pool è configurato per l'uso di piccole macchine virtuali con la versione più recente del sistema operativo della famiglia quattro e il numero di destinazione dei nodi di calcolo è determinato dalla formula di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="db79d-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

## <span data-ttu-id="db79d-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db79d-119">PARAMETERS</span></span>

### <span data-ttu-id="db79d-120">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="db79d-120">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-121">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="db79d-121">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="db79d-122">Specifica la quantità di tempo, in minuti, che trascorre prima che le dimensioni del pool vengano regolate automaticamente in base alla formula di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="db79d-122">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="db79d-123">Il valore predefinito è 15 minuti e il valore minimo è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="db79d-123">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-124">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="db79d-124">-AutoScaleFormula</span></span>
<span data-ttu-id="db79d-125">Specifica la formula per il ridimensionamento automatico del pool.</span><span class="sxs-lookup"><span data-stu-id="db79d-125">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-126">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="db79d-126">-BatchContext</span></span>
<span data-ttu-id="db79d-127">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="db79d-127">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="db79d-128">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="db79d-128">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="db79d-129">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="db79d-129">-CertificateReferences</span></span>
<span data-ttu-id="db79d-130">Specifica i certificati associati al pool.</span><span class="sxs-lookup"><span data-stu-id="db79d-130">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="db79d-131">Il servizio batch installa i certificati a cui si fa riferimento in ogni nodo di calcolo del pool.</span><span class="sxs-lookup"><span data-stu-id="db79d-131">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-132">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="db79d-132">-CloudServiceConfiguration</span></span>
<span data-ttu-id="db79d-133">Specifica le impostazioni di configurazione per un pool in base alla piattaforma di servizi cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="db79d-133">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-134">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db79d-134">-DisplayName</span></span>
<span data-ttu-id="db79d-135">Specifica il nome visualizzato del pool.</span><span class="sxs-lookup"><span data-stu-id="db79d-135">Specifies the display name of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-136">-ID</span><span class="sxs-lookup"><span data-stu-id="db79d-136">-Id</span></span>
<span data-ttu-id="db79d-137">Specifica l'ID del pool da creare.</span><span class="sxs-lookup"><span data-stu-id="db79d-137">Specifies the ID of the pool to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-138">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="db79d-138">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="db79d-139">Indica che questo cmdlet configura il pool per la comunicazione diretta tra i nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="db79d-139">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-140">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="db79d-140">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="db79d-141">Specifica il numero massimo di attività che possono essere eseguite in un singolo nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="db79d-141">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-142">-Metadata</span><span class="sxs-lookup"><span data-stu-id="db79d-142">-Metadata</span></span>
<span data-ttu-id="db79d-143">Specifica i metadati, come coppie chiave/valore, da aggiungere al nuovo pool.</span><span class="sxs-lookup"><span data-stu-id="db79d-143">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="db79d-144">La chiave è il nome dei metadati.</span><span class="sxs-lookup"><span data-stu-id="db79d-144">The key is the metadata name.</span></span>
<span data-ttu-id="db79d-145">Il valore è il valore Metadata.</span><span class="sxs-lookup"><span data-stu-id="db79d-145">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-146">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="db79d-146">-NetworkConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-147">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="db79d-147">-ResizeTimeout</span></span>
<span data-ttu-id="db79d-148">Specifica il timeout per l'assegnazione di nodi di calcolo al pool.</span><span class="sxs-lookup"><span data-stu-id="db79d-148">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-149">-StartTask</span><span class="sxs-lookup"><span data-stu-id="db79d-149">-StartTask</span></span>
<span data-ttu-id="db79d-150">Specifica la specifica dell'attività Start per il pool.</span><span class="sxs-lookup"><span data-stu-id="db79d-150">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="db79d-151">L'attività avvia viene eseguita quando un nodo Compute si unisce al pool o quando il nodo COMPUTE viene riavviato o rielaborato.</span><span class="sxs-lookup"><span data-stu-id="db79d-151">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-152">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="db79d-152">-TargetDedicated</span></span>
<span data-ttu-id="db79d-153">Specifica il numero di destinazione dei nodi compute da allocare al pool.</span><span class="sxs-lookup"><span data-stu-id="db79d-153">Specifies the target number of compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-154">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="db79d-154">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="db79d-155">Specifica i criteri di pianificazione delle attività, ad esempio ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="db79d-155">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-156">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="db79d-156">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="db79d-157">Specifica le impostazioni di configurazione per un pool nell'infrastruttura delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="db79d-157">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-158">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="db79d-158">-VirtualMachineSize</span></span>
<span data-ttu-id="db79d-159">Specifica le dimensioni delle macchine virtuali nel pool.</span><span class="sxs-lookup"><span data-stu-id="db79d-159">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="db79d-160">Per altre informazioni sulle dimensioni della macchina virtuale, vedere dimensioni per le macchine virtuali https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) nel sito Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="db79d-160">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db79d-161">-Confirm</span></span>
<span data-ttu-id="db79d-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db79d-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db79d-163">-WhatIf</span></span>
<span data-ttu-id="db79d-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db79d-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db79d-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db79d-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db79d-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db79d-166">-DefaultProfile</span></span>
<span data-ttu-id="db79d-167">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db79d-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db79d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db79d-168">CommonParameters</span></span>
<span data-ttu-id="db79d-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db79d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db79d-170">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db79d-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db79d-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db79d-171">INPUTS</span></span>

### <span data-ttu-id="db79d-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="db79d-172">BatchAccountContext</span></span>
<span data-ttu-id="db79d-173">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="db79d-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="db79d-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db79d-174">OUTPUTS</span></span>

## <span data-ttu-id="db79d-175">Note</span><span class="sxs-lookup"><span data-stu-id="db79d-175">NOTES</span></span>

## <span data-ttu-id="db79d-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db79d-176">RELATED LINKS</span></span>

[<span data-ttu-id="db79d-177">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="db79d-177">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="db79d-178">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="db79d-178">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="db79d-179">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="db79d-179">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="db79d-180">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="db79d-180">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


