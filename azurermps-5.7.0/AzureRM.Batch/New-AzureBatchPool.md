---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 54a5d6dc737bc0bd6a7f1d236ce855b2a08dca6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521926"
---
# <span data-ttu-id="b99ef-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b99ef-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="b99ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b99ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b99ef-103">Crea un pool nel servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b99ef-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b99ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b99ef-104">SYNTAX</span></span>

### <span data-ttu-id="b99ef-105">CloudServiceAndTargetDedicated (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b99ef-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b99ef-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="b99ef-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b99ef-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="b99ef-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b99ef-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="b99ef-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b99ef-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b99ef-109">DESCRIPTION</span></span>
<span data-ttu-id="b99ef-110">Il cmdlet **New-AzureBatchPool** crea un pool nel servizio batch di Azure sotto l'account specificato dal parametro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="b99ef-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="b99ef-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b99ef-111">EXAMPLES</span></span>

### <span data-ttu-id="b99ef-112">Esempio 1: creare un nuovo pool usando il set di parametri TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="b99ef-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="b99ef-113">Questo comando crea un nuovo pool con ID pool con il set di parametri TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="b99ef-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="b99ef-114">L'allocazione di destinazione è tre nodi compute.</span><span class="sxs-lookup"><span data-stu-id="b99ef-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="b99ef-115">Il pool è configurato per l'uso di piccole macchine virtuali con la versione più recente del sistema operativo della famiglia quattro.</span><span class="sxs-lookup"><span data-stu-id="b99ef-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="b99ef-116">Esempio 2: creare un nuovo pool usando il set di parametri di scalabilità verticale</span><span class="sxs-lookup"><span data-stu-id="b99ef-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="b99ef-117">Questo comando crea un nuovo pool con ID AutoScalePool con il set di parametri autoscale.</span><span class="sxs-lookup"><span data-stu-id="b99ef-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="b99ef-118">Il pool è configurato per l'uso di piccole macchine virtuali con la versione più recente del sistema operativo della famiglia quattro e il numero di destinazione dei nodi di calcolo è determinato dalla formula di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="b99ef-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="b99ef-119">Esempio 3: creare un pool con nodi in una subnet</span><span class="sxs-lookup"><span data-stu-id="b99ef-119">Example 3: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="b99ef-120">Esempio 4: creare un pool con account utente personalizzati</span><span class="sxs-lookup"><span data-stu-id="b99ef-120">Example 4: Create a pool with custom user accounts</span></span>
```
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="b99ef-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b99ef-121">PARAMETERS</span></span>

### <span data-ttu-id="b99ef-122">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="b99ef-122">-ApplicationLicenses</span></span>
<span data-ttu-id="b99ef-123">Elenco delle licenze per l'applicazione che il servizio batch rende disponibile su ogni nodo di calcolo nel pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-123">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: ApplicationLicense

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-124">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="b99ef-124">-ApplicationPackageReferences</span></span>
```yaml
Type: PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-125">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="b99ef-125">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="b99ef-126">Specifica la quantità di tempo, in minuti, che trascorre prima che le dimensioni del pool vengano regolate automaticamente in base alla formula di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="b99ef-126">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="b99ef-127">Il valore predefinito è 15 minuti e il valore minimo è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="b99ef-127">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-128">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="b99ef-128">-AutoScaleFormula</span></span>
<span data-ttu-id="b99ef-129">Specifica la formula per il ridimensionamento automatico del pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-129">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-130">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b99ef-130">-BatchContext</span></span>
<span data-ttu-id="b99ef-131">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b99ef-131">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b99ef-132">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b99ef-132">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b99ef-133">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="b99ef-133">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b99ef-134">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b99ef-134">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b99ef-135">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b99ef-135">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-136">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="b99ef-136">-CertificateReferences</span></span>
<span data-ttu-id="b99ef-137">Specifica i certificati associati al pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-137">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="b99ef-138">Il servizio batch installa i certificati a cui si fa riferimento in ogni nodo di calcolo del pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-138">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-139">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b99ef-139">-CloudServiceConfiguration</span></span>
<span data-ttu-id="b99ef-140">Specifica le impostazioni di configurazione per un pool in base alla piattaforma di servizi cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="b99ef-140">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b99ef-141">-DefaultProfile</span></span>
<span data-ttu-id="b99ef-142">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b99ef-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-143">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b99ef-143">-DisplayName</span></span>
<span data-ttu-id="b99ef-144">Specifica il nome visualizzato del pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-144">Specifies the display name of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-145">-ID</span><span class="sxs-lookup"><span data-stu-id="b99ef-145">-Id</span></span>
<span data-ttu-id="b99ef-146">Specifica l'ID del pool da creare.</span><span class="sxs-lookup"><span data-stu-id="b99ef-146">Specifies the ID of the pool to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-147">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="b99ef-147">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="b99ef-148">Indica che questo cmdlet configura il pool per la comunicazione diretta tra i nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="b99ef-148">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-149">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="b99ef-149">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="b99ef-150">Specifica il numero massimo di attività che possono essere eseguite in un singolo nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="b99ef-150">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b99ef-151">-Metadata</span></span>
<span data-ttu-id="b99ef-152">Specifica i metadati, come coppie chiave/valore, da aggiungere al nuovo pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-152">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="b99ef-153">La chiave è il nome dei metadati.</span><span class="sxs-lookup"><span data-stu-id="b99ef-153">The key is the metadata name.</span></span>
<span data-ttu-id="b99ef-154">Il valore è il valore Metadata.</span><span class="sxs-lookup"><span data-stu-id="b99ef-154">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-155">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b99ef-155">-NetworkConfiguration</span></span>
<span data-ttu-id="b99ef-156">Configurazione di rete per il pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-156">The network configuration for the pool.</span></span>

```yaml
Type: PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-157">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="b99ef-157">-ResizeTimeout</span></span>
<span data-ttu-id="b99ef-158">Specifica il timeout per l'assegnazione di nodi di calcolo al pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-158">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-159">-StartTask</span><span class="sxs-lookup"><span data-stu-id="b99ef-159">-StartTask</span></span>
<span data-ttu-id="b99ef-160">Specifica la specifica dell'attività Start per il pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-160">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="b99ef-161">L'attività avvia viene eseguita quando un nodo Compute si unisce al pool o quando il nodo COMPUTE viene riavviato o rielaborato.</span><span class="sxs-lookup"><span data-stu-id="b99ef-161">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-162">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="b99ef-162">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="b99ef-163">Specifica il numero di nodi di calcolo dedicati da assegnare al pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-163">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-164">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="b99ef-164">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="b99ef-165">Specifica il numero di nodi di calcolo a priorità bassa da assegnare al pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-165">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-166">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="b99ef-166">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="b99ef-167">Specifica i criteri di pianificazione delle attività, ad esempio ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="b99ef-167">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-168">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="b99ef-168">-UserAccount</span></span>
<span data-ttu-id="b99ef-169">Elenco di account utente da creare in ogni nodo del pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-169">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: PSUserAccount[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-170">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="b99ef-170">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="b99ef-171">Specifica le impostazioni di configurazione per un pool nell'infrastruttura delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b99ef-171">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-172">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="b99ef-172">-VirtualMachineSize</span></span>
<span data-ttu-id="b99ef-173">Specifica le dimensioni delle macchine virtuali nel pool.</span><span class="sxs-lookup"><span data-stu-id="b99ef-173">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="b99ef-174">Per altre informazioni sulle dimensioni della macchina virtuale, vedere dimensioni per le macchine virtuali https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) nel sito Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b99ef-174">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-175">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b99ef-175">-Confirm</span></span>
<span data-ttu-id="b99ef-176">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b99ef-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b99ef-177">-WhatIf</span></span>
<span data-ttu-id="b99ef-178">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b99ef-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b99ef-179">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b99ef-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99ef-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b99ef-180">CommonParameters</span></span>
<span data-ttu-id="b99ef-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b99ef-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b99ef-182">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b99ef-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b99ef-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b99ef-183">INPUTS</span></span>

### <span data-ttu-id="b99ef-184">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b99ef-184">BatchAccountContext</span></span>
<span data-ttu-id="b99ef-185">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b99ef-185">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="b99ef-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b99ef-186">OUTPUTS</span></span>

## <span data-ttu-id="b99ef-187">Note</span><span class="sxs-lookup"><span data-stu-id="b99ef-187">NOTES</span></span>

## <span data-ttu-id="b99ef-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b99ef-188">RELATED LINKS</span></span>

[<span data-ttu-id="b99ef-189">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b99ef-189">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b99ef-190">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b99ef-190">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="b99ef-191">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b99ef-191">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="b99ef-192">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="b99ef-192">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


