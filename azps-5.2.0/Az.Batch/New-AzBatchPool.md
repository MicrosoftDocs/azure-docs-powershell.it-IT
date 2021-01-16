---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 3c66893875dedd5e7298b9c6239c3da7ee86212e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336823"
---
# <span data-ttu-id="596ef-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="596ef-101">New-AzBatchPool</span></span>

## <span data-ttu-id="596ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="596ef-102">SYNOPSIS</span></span>
<span data-ttu-id="596ef-103">Crea un pool nel servizio batch.</span><span class="sxs-lookup"><span data-stu-id="596ef-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="596ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="596ef-104">SYNTAX</span></span>

### <span data-ttu-id="596ef-105">CloudServiceAndTargetDedicated (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="596ef-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="596ef-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="596ef-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="596ef-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="596ef-107">CloudServiceAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="596ef-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="596ef-108">VirtualMachineAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="596ef-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="596ef-109">DESCRIPTION</span></span>
<span data-ttu-id="596ef-110">Il cmdlet **New-AzBatchPool** crea un pool nel servizio batch di Azure sotto l'account specificato dal parametro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="596ef-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="596ef-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="596ef-111">EXAMPLES</span></span>

### <span data-ttu-id="596ef-112">Esempio 1: creare un nuovo pool usando il parametro TargetDedicated impostato con CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="596ef-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="596ef-113">Il pool è configurato per l'uso di STANDARD_D1_V2 macchine virtuali con la versione del sistema operativo della famiglia quattro.</span><span class="sxs-lookup"><span data-stu-id="596ef-113">The pool is configured to use STANDARD_D1_V2 virtual machines with operating system version of family four.</span></span>

### <span data-ttu-id="596ef-114">Esempio 2: creare un nuovo pool usando il parametro TargetDedicated impostato con VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="596ef-114">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="596ef-115">Questo comando crea un nuovo pool con ID pool con il set di parametri TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="596ef-115">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="596ef-116">L'allocazione di destinazione è tre nodi compute.</span><span class="sxs-lookup"><span data-stu-id="596ef-116">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="596ef-117">Il pool è configurato per l'uso di STANDARD_D1_V2 macchine virtuali con l'immagine del sistema operativo Windows-2016-datacenter.</span><span class="sxs-lookup"><span data-stu-id="596ef-117">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image.</span></span>

### <span data-ttu-id="596ef-118">Esempio 3: creare un nuovo pool usando il set di parametri di scalabilità verticale</span><span class="sxs-lookup"><span data-stu-id="596ef-118">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="596ef-119">Questo comando crea un nuovo pool con ID AutoScalePool con il set di parametri autoscale.</span><span class="sxs-lookup"><span data-stu-id="596ef-119">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="596ef-120">Il pool è configurato per l'uso di STANDARD_D1_V2 macchine virtuali con l'immagine del sistema operativo Windows-2016-datacenter e il numero di destinazione dei nodi di calcolo è determinato dalla formula di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="596ef-120">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="596ef-121">Esempio 4: creare un pool con nodi in una subnet</span><span class="sxs-lookup"><span data-stu-id="596ef-121">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="596ef-122">Esempio 5: creare un pool con account utente personalizzati</span><span class="sxs-lookup"><span data-stu-id="596ef-122">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="596ef-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="596ef-123">PARAMETERS</span></span>

### <span data-ttu-id="596ef-124">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="596ef-124">-ApplicationLicenses</span></span>
<span data-ttu-id="596ef-125">Elenco delle licenze per l'applicazione che il servizio batch rende disponibile su ogni nodo di calcolo nel pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-125">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="596ef-126">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="596ef-126">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="596ef-127">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="596ef-127">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="596ef-128">Specifica la quantità di tempo, in minuti, che trascorre prima che le dimensioni del pool vengano regolate automaticamente in base alla formula di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="596ef-128">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="596ef-129">Il valore predefinito è 15 minuti e il valore minimo è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="596ef-129">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="596ef-130">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="596ef-130">-AutoScaleFormula</span></span>
<span data-ttu-id="596ef-131">Specifica la formula per il ridimensionamento automatico del pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-131">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="596ef-132">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="596ef-132">-BatchContext</span></span>
<span data-ttu-id="596ef-133">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="596ef-133">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="596ef-134">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="596ef-134">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="596ef-135">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="596ef-135">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="596ef-136">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="596ef-136">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="596ef-137">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="596ef-137">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="596ef-138">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="596ef-138">-CertificateReferences</span></span>
<span data-ttu-id="596ef-139">Specifica i certificati associati al pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-139">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="596ef-140">Il servizio batch installa i certificati a cui si fa riferimento in ogni nodo di calcolo del pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-140">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="596ef-141">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="596ef-141">-CloudServiceConfiguration</span></span>
<span data-ttu-id="596ef-142">Specifica le impostazioni di configurazione per un pool in base alla piattaforma di servizi cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="596ef-142">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="596ef-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="596ef-143">-DefaultProfile</span></span>
<span data-ttu-id="596ef-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="596ef-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="596ef-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="596ef-145">-DisplayName</span></span>
<span data-ttu-id="596ef-146">Specifica il nome visualizzato del pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-146">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="596ef-147">-ID</span><span class="sxs-lookup"><span data-stu-id="596ef-147">-Id</span></span>
<span data-ttu-id="596ef-148">Specifica l'ID del pool da creare.</span><span class="sxs-lookup"><span data-stu-id="596ef-148">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="596ef-149">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="596ef-149">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="596ef-150">Indica che questo cmdlet configura il pool per la comunicazione diretta tra i nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="596ef-150">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="596ef-151">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="596ef-151">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="596ef-152">Specifica il numero massimo di attività che possono essere eseguite in un singolo nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="596ef-152">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="596ef-153">-Metadata</span><span class="sxs-lookup"><span data-stu-id="596ef-153">-Metadata</span></span>
<span data-ttu-id="596ef-154">Specifica i metadati, come coppie chiave/valore, da aggiungere al nuovo pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-154">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="596ef-155">La chiave è il nome dei metadati.</span><span class="sxs-lookup"><span data-stu-id="596ef-155">The key is the metadata name.</span></span>
<span data-ttu-id="596ef-156">Il valore è il valore Metadata.</span><span class="sxs-lookup"><span data-stu-id="596ef-156">The value is the metadata value.</span></span>

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

### <span data-ttu-id="596ef-157">-MountConfiguration</span><span class="sxs-lookup"><span data-stu-id="596ef-157">-MountConfiguration</span></span>
<span data-ttu-id="596ef-158">Un elenco di file System da montare in ogni nodo del pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-158">A list of file systems to mount on each node in the pool.</span></span> <span data-ttu-id="596ef-159">Questo supporta i file di Azure, NFS, CIFS/SMB e Blobfuse.</span><span class="sxs-lookup"><span data-stu-id="596ef-159">This supports Azure Files, NFS, CIFS/SMB, and Blobfuse.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMountConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="596ef-160">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="596ef-160">-NetworkConfiguration</span></span>
<span data-ttu-id="596ef-161">Configurazione di rete per il pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-161">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="596ef-162">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="596ef-162">-ResizeTimeout</span></span>
<span data-ttu-id="596ef-163">Specifica il timeout per l'assegnazione di nodi di calcolo al pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-163">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="596ef-164">-StartTask</span><span class="sxs-lookup"><span data-stu-id="596ef-164">-StartTask</span></span>
<span data-ttu-id="596ef-165">Specifica la specifica dell'attività Start per il pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-165">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="596ef-166">L'attività avvia viene eseguita quando un nodo Compute si unisce al pool o quando il nodo COMPUTE viene riavviato o rielaborato.</span><span class="sxs-lookup"><span data-stu-id="596ef-166">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="596ef-167">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="596ef-167">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="596ef-168">Specifica il numero di nodi di calcolo dedicati da assegnare al pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-168">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="596ef-169">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="596ef-169">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="596ef-170">Specifica il numero di nodi di calcolo a priorità bassa da assegnare al pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-170">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="596ef-171">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="596ef-171">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="596ef-172">Specifica i criteri di pianificazione delle attività, ad esempio ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="596ef-172">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="596ef-173">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="596ef-173">-UserAccount</span></span>
<span data-ttu-id="596ef-174">Elenco di account utente da creare in ogni nodo del pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-174">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="596ef-175">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="596ef-175">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="596ef-176">Specifica le impostazioni di configurazione per un pool nell'infrastruttura delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="596ef-176">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="596ef-177">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="596ef-177">-VirtualMachineSize</span></span>
<span data-ttu-id="596ef-178">Specifica le dimensioni delle macchine virtuali nel pool.</span><span class="sxs-lookup"><span data-stu-id="596ef-178">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="596ef-179">Per altre informazioni sulle dimensioni della macchina virtuale, vedere dimensioni per le macchine virtuali https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) nel sito Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="596ef-179">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="596ef-180">-Confermare</span><span class="sxs-lookup"><span data-stu-id="596ef-180">-Confirm</span></span>
<span data-ttu-id="596ef-181">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="596ef-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="596ef-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="596ef-182">-WhatIf</span></span>
<span data-ttu-id="596ef-183">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="596ef-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="596ef-184">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="596ef-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="596ef-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="596ef-185">CommonParameters</span></span>
<span data-ttu-id="596ef-186">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="596ef-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="596ef-187">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="596ef-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="596ef-188">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="596ef-188">INPUTS</span></span>

### <span data-ttu-id="596ef-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="596ef-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="596ef-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="596ef-190">OUTPUTS</span></span>

### <span data-ttu-id="596ef-191">System. void</span><span class="sxs-lookup"><span data-stu-id="596ef-191">System.Void</span></span>

## <span data-ttu-id="596ef-192">Note</span><span class="sxs-lookup"><span data-stu-id="596ef-192">NOTES</span></span>

## <span data-ttu-id="596ef-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="596ef-193">RELATED LINKS</span></span>

[<span data-ttu-id="596ef-194">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="596ef-194">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="596ef-195">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="596ef-195">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="596ef-196">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="596ef-196">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="596ef-197">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="596ef-197">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
