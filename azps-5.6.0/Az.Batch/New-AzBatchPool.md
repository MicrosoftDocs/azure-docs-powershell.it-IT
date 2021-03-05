---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 7fef035eda89d68d757658a512ca00369b69694a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992962"
---
# <span data-ttu-id="70803-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="70803-101">New-AzBatchPool</span></span>

## <span data-ttu-id="70803-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70803-102">SYNOPSIS</span></span>
<span data-ttu-id="70803-103">Crea un pool nel servizio batch.</span><span class="sxs-lookup"><span data-stu-id="70803-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="70803-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70803-104">SYNTAX</span></span>

### <span data-ttu-id="70803-105">CloudServiceAndTargetDedicated (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70803-105">CloudServiceAndTargetDedicated (Default)</span></span>
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

### <span data-ttu-id="70803-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="70803-106">VirtualMachineAndTargetDedicated</span></span>
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

### <span data-ttu-id="70803-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="70803-107">CloudServiceAndAutoScale</span></span>
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

### <span data-ttu-id="70803-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="70803-108">VirtualMachineAndAutoScale</span></span>
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

## <span data-ttu-id="70803-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="70803-109">DESCRIPTION</span></span>
<span data-ttu-id="70803-110">Il cmdlet **New-AzBatchPool** crea un pool nel servizio batch di Azure nell'account specificato dal *parametro BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="70803-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="70803-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70803-111">EXAMPLES</span></span>

### <span data-ttu-id="70803-112">Esempio 1: Creare un nuovo pool usando il parametro TargetDedicated impostato con CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="70803-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="70803-113">Il pool è configurato per l'uso STANDARD_D1_V2 macchine virtuali con la versione del sistema operativo della famiglia quattro.</span><span class="sxs-lookup"><span data-stu-id="70803-113">The pool is configured to use STANDARD_D1_V2 virtual machines with operating system version of family four.</span></span>

### <span data-ttu-id="70803-114">Esempio 2: Creare un nuovo pool usando il parametro TargetDedicated impostato con VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="70803-114">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="70803-115">Questo comando crea un nuovo pool con ID MyPool usando il set di parametri TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="70803-115">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="70803-116">L'allocazione di destinazione è tre nodi di calcolo.</span><span class="sxs-lookup"><span data-stu-id="70803-116">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="70803-117">Il pool è configurato per l'uso STANDARD_D1_V2 macchine virtuali con l'immagine del sistema operativo Windows-2016-Datacenter.</span><span class="sxs-lookup"><span data-stu-id="70803-117">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image.</span></span>

### <span data-ttu-id="70803-118">Esempio 3: Creare un nuovo pool usando il set di parametri di scala automatica</span><span class="sxs-lookup"><span data-stu-id="70803-118">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="70803-119">Questo comando crea un nuovo pool con ID AutoScalePool usando il set di parametri AutoScale.</span><span class="sxs-lookup"><span data-stu-id="70803-119">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="70803-120">Il pool è configurato per usare macchine virtuali STANDARD_D1_V2 con l'immagine del sistema operativo Windows-2016-Datacenter e il numero di nodi di elaborazione di destinazione è determinato dalla formula di gradazione automatica.</span><span class="sxs-lookup"><span data-stu-id="70803-120">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="70803-121">Esempio 4: Creare un pool con nodi in una subnet</span><span class="sxs-lookup"><span data-stu-id="70803-121">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="70803-122">Esempio 5: Creare un pool con account utente personalizzati</span><span class="sxs-lookup"><span data-stu-id="70803-122">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="70803-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70803-123">PARAMETERS</span></span>

### <span data-ttu-id="70803-124">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="70803-124">-ApplicationLicenses</span></span>
<span data-ttu-id="70803-125">L'elenco di licenze di applicazioni che il servizio batch rende disponibile in ogni nodo di calcolo nel pool.</span><span class="sxs-lookup"><span data-stu-id="70803-125">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="70803-126">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="70803-126">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="70803-127">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="70803-127">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="70803-128">Specifica la quantità di tempo, in minuti, che deve trascorrere prima che le dimensioni del pool vengono regolate automaticamente in base alla formula di scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="70803-128">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="70803-129">Il valore predefinito è 15 minuti e il valore minimo è 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="70803-129">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="70803-130">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="70803-130">-AutoScaleFormula</span></span>
<span data-ttu-id="70803-131">Specifica la formula per ridimensionare automaticamente il pool.</span><span class="sxs-lookup"><span data-stu-id="70803-131">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="70803-132">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="70803-132">-BatchContext</span></span>
<span data-ttu-id="70803-133">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="70803-133">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="70803-134">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="70803-134">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="70803-135">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="70803-135">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="70803-136">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="70803-136">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="70803-137">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="70803-137">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="70803-138">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="70803-138">-CertificateReferences</span></span>
<span data-ttu-id="70803-139">Specifica i certificati associati al pool.</span><span class="sxs-lookup"><span data-stu-id="70803-139">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="70803-140">Il servizio batch installa i certificati a cui si fa riferimento in ogni nodo di elaborazione del pool.</span><span class="sxs-lookup"><span data-stu-id="70803-140">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

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

### <span data-ttu-id="70803-141">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="70803-141">-CloudServiceConfiguration</span></span>
<span data-ttu-id="70803-142">Specifica le impostazioni di configurazione per un pool in base alla piattaforma del servizio cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="70803-142">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="70803-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70803-143">-DefaultProfile</span></span>
<span data-ttu-id="70803-144">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70803-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70803-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="70803-145">-DisplayName</span></span>
<span data-ttu-id="70803-146">Specifica il nome visualizzato del pool.</span><span class="sxs-lookup"><span data-stu-id="70803-146">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="70803-147">-Id</span><span class="sxs-lookup"><span data-stu-id="70803-147">-Id</span></span>
<span data-ttu-id="70803-148">Specifica l'ID del pool da creare.</span><span class="sxs-lookup"><span data-stu-id="70803-148">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="70803-149">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="70803-149">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="70803-150">Indica che questo cmdlet configura il pool per la comunicazione diretta tra i nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="70803-150">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="70803-151">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="70803-151">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="70803-152">Specifica il numero massimo di attività che è possibile eseguire in un singolo nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="70803-152">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="70803-153">-Metadata</span><span class="sxs-lookup"><span data-stu-id="70803-153">-Metadata</span></span>
<span data-ttu-id="70803-154">Specifica i metadati, come coppie chiave/valore, da aggiungere al nuovo pool.</span><span class="sxs-lookup"><span data-stu-id="70803-154">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="70803-155">La chiave è il nome dei metadati.</span><span class="sxs-lookup"><span data-stu-id="70803-155">The key is the metadata name.</span></span>
<span data-ttu-id="70803-156">Il valore è il valore dei metadati.</span><span class="sxs-lookup"><span data-stu-id="70803-156">The value is the metadata value.</span></span>

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

### <span data-ttu-id="70803-157">-MountConfiguration</span><span class="sxs-lookup"><span data-stu-id="70803-157">-MountConfiguration</span></span>
<span data-ttu-id="70803-158">Elenco di file system da installare in ogni nodo del pool.</span><span class="sxs-lookup"><span data-stu-id="70803-158">A list of file systems to mount on each node in the pool.</span></span> <span data-ttu-id="70803-159">Supporta File di Azure, NFS, CIFS/SMB e BLOBfuse.</span><span class="sxs-lookup"><span data-stu-id="70803-159">This supports Azure Files, NFS, CIFS/SMB, and Blobfuse.</span></span>

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

### <span data-ttu-id="70803-160">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="70803-160">-NetworkConfiguration</span></span>
<span data-ttu-id="70803-161">Configurazione di rete per il pool.</span><span class="sxs-lookup"><span data-stu-id="70803-161">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="70803-162">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="70803-162">-ResizeTimeout</span></span>
<span data-ttu-id="70803-163">Specifica il timeout per l'allocazione dei nodi di calcolo al pool.</span><span class="sxs-lookup"><span data-stu-id="70803-163">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="70803-164">-StartTask</span><span class="sxs-lookup"><span data-stu-id="70803-164">-StartTask</span></span>
<span data-ttu-id="70803-165">Specifica la specifica dell'attività di avvio per il pool.</span><span class="sxs-lookup"><span data-stu-id="70803-165">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="70803-166">L'attività di avvio viene eseguita quando un nodo di calcolo si unisce al pool o quando il nodo di calcolo viene riavviato o visualizzato di nuovo.</span><span class="sxs-lookup"><span data-stu-id="70803-166">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="70803-167">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="70803-167">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="70803-168">Specifica il numero di destinazione di nodi di elaborazione dedicati da allocare al pool.</span><span class="sxs-lookup"><span data-stu-id="70803-168">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="70803-169">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="70803-169">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="70803-170">Specifica il numero di destinazione di nodi di elaborazione con priorità bassa da allocare al pool.</span><span class="sxs-lookup"><span data-stu-id="70803-170">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="70803-171">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="70803-171">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="70803-172">Specifica i criteri di programmazione delle attività, ad esempio ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="70803-172">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="70803-173">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="70803-173">-UserAccount</span></span>
<span data-ttu-id="70803-174">Elenco degli account utente da creare in ogni nodo del pool.</span><span class="sxs-lookup"><span data-stu-id="70803-174">The list of user accounts to be created on each node in the pool.</span></span>

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

### <span data-ttu-id="70803-175">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="70803-175">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="70803-176">Specifica le impostazioni di configurazione per un pool nell'infrastruttura delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="70803-176">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="70803-177">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="70803-177">-VirtualMachineSize</span></span>
<span data-ttu-id="70803-178">Specifica le dimensioni delle macchine virtuali nel pool.</span><span class="sxs-lookup"><span data-stu-id="70803-178">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="70803-179">Per altre informazioni sulle dimensioni delle macchine virtuali, vedere Dimensioni per le macchine virtuali https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) (nel sito di Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="70803-179">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="70803-180">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70803-180">-Confirm</span></span>
<span data-ttu-id="70803-181">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70803-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70803-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70803-182">-WhatIf</span></span>
<span data-ttu-id="70803-183">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70803-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70803-184">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70803-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70803-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70803-185">CommonParameters</span></span>
<span data-ttu-id="70803-186">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70803-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70803-187">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="70803-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70803-188">INPUT</span><span class="sxs-lookup"><span data-stu-id="70803-188">INPUTS</span></span>

### <span data-ttu-id="70803-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="70803-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="70803-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70803-190">OUTPUTS</span></span>

### <span data-ttu-id="70803-191">System.Void</span><span class="sxs-lookup"><span data-stu-id="70803-191">System.Void</span></span>

## <span data-ttu-id="70803-192">NOTE</span><span class="sxs-lookup"><span data-stu-id="70803-192">NOTES</span></span>

## <span data-ttu-id="70803-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70803-193">RELATED LINKS</span></span>

[<span data-ttu-id="70803-194">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="70803-194">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="70803-195">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="70803-195">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="70803-196">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="70803-196">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="70803-197">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="70803-197">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
