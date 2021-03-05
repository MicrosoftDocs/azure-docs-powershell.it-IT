---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 065885f4ae8f6d2ac51cb87cb0e697f4f22245f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995888"
---
# <span data-ttu-id="e92e2-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e92e2-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="e92e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e92e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e92e2-103">Creare una nuova risorsa tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="e92e2-103">Create new node type resource.</span></span>

## <span data-ttu-id="e92e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e92e2-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e92e2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e92e2-105">DESCRIPTION</span></span>
<span data-ttu-id="e92e2-106">Creare una nuova risorsa tipo di nodo per un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="e92e2-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="e92e2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e92e2-107">EXAMPLES</span></span>

### <span data-ttu-id="e92e2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e92e2-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="e92e2-109">Creare un tipo di nodo primario con 3 nodi.</span><span class="sxs-lookup"><span data-stu-id="e92e2-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="e92e2-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e92e2-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="e92e2-111">Creare un tipo di nodo primario con 5 nodi e specificare le proprietà di posizionamento, i capacità, le porte dell'applicazione e dell'effimero.</span><span class="sxs-lookup"><span data-stu-id="e92e2-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="e92e2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e92e2-112">PARAMETERS</span></span>

### <span data-ttu-id="e92e2-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="e92e2-113">-ApplicationEndPort</span></span>
<span data-ttu-id="e92e2-114">Porta finale dell'applicazione per un intervallo di porte.</span><span class="sxs-lookup"><span data-stu-id="e92e2-114">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="e92e2-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="e92e2-115">-ApplicationStartPort</span></span>
<span data-ttu-id="e92e2-116">Porta di avvio dell'applicazione di un intervallo di porte.</span><span class="sxs-lookup"><span data-stu-id="e92e2-116">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="e92e2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e92e2-117">-AsJob</span></span>
<span data-ttu-id="e92e2-118">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="e92e2-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e92e2-119">-Capacità</span><span class="sxs-lookup"><span data-stu-id="e92e2-119">-Capacity</span></span>
<span data-ttu-id="e92e2-120">Tag di capacità applicati ai nodi nel tipo di nodo come coppie chiave/valore. Gestione risorse cluster usa questi tag per determinare la quantità di risorse di un nodo.</span><span class="sxs-lookup"><span data-stu-id="e92e2-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="e92e2-121">L'aggiornamento eseguirà l'override dei valori correnti.</span><span class="sxs-lookup"><span data-stu-id="e92e2-121">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e92e2-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e92e2-122">-ClusterName</span></span>
<span data-ttu-id="e92e2-123">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="e92e2-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e92e2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e92e2-124">-DefaultProfile</span></span>
<span data-ttu-id="e92e2-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e92e2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e92e2-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="e92e2-126">-DiskSize</span></span>
<span data-ttu-id="e92e2-127">Dimensioni del disco per ogni macchina virtuale nel tipo di nodo in BLOB.</span><span class="sxs-lookup"><span data-stu-id="e92e2-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="e92e2-128">Impostazione predefinita 100.</span><span class="sxs-lookup"><span data-stu-id="e92e2-128">Default 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e92e2-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="e92e2-129">-EphemeralEndPort</span></span>
<span data-ttu-id="e92e2-130">Porta finale effimera di una gamma di porte.</span><span class="sxs-lookup"><span data-stu-id="e92e2-130">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="e92e2-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="e92e2-131">-EphemeralStartPort</span></span>
<span data-ttu-id="e92e2-132">Porta iniziale effimera di un intervallo di porte.</span><span class="sxs-lookup"><span data-stu-id="e92e2-132">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="e92e2-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="e92e2-133">-InstanceCount</span></span>
<span data-ttu-id="e92e2-134">Numero di nodi nel tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="e92e2-134">The number of nodes in the node type.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e92e2-135">-Name</span><span class="sxs-lookup"><span data-stu-id="e92e2-135">-Name</span></span>
<span data-ttu-id="e92e2-136">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="e92e2-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e92e2-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="e92e2-137">-PlacementProperty</span></span>
<span data-ttu-id="e92e2-138">Tag di posizionamento applicati ai nodi nel tipo di nodo come coppie chiave/valore, che possono essere usati per indicare dove eseguire determinati servizi (carico di lavoro).</span><span class="sxs-lookup"><span data-stu-id="e92e2-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="e92e2-139">L'aggiornamento eseguirà l'override dei valori correnti.</span><span class="sxs-lookup"><span data-stu-id="e92e2-139">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e92e2-140">-Principale</span><span class="sxs-lookup"><span data-stu-id="e92e2-140">-Primary</span></span>
<span data-ttu-id="e92e2-141">Specificare se il tipo di nodo è primario.</span><span class="sxs-lookup"><span data-stu-id="e92e2-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="e92e2-142">In questo tipo di nodo verranno eseguiti i servizi di sistema.</span><span class="sxs-lookup"><span data-stu-id="e92e2-142">On this node type will run system services.</span></span>
<span data-ttu-id="e92e2-143">Solo un tipo di nodo deve essere contrassegnato come principale.</span><span class="sxs-lookup"><span data-stu-id="e92e2-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="e92e2-144">Il tipo di nodo primario non può essere eliminato né modificato per i cluster esistenti.</span><span class="sxs-lookup"><span data-stu-id="e92e2-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="e92e2-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e92e2-145">-ResourceGroupName</span></span>
<span data-ttu-id="e92e2-146">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e92e2-146">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e92e2-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="e92e2-147">-VmImageOffer</span></span>
<span data-ttu-id="e92e2-148">Tipo di offerta dell'immagine di Azure Virtual Machines Marketplace.</span><span class="sxs-lookup"><span data-stu-id="e92e2-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="e92e2-149">Impostazione predefinita: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="e92e2-149">Default: WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "WindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e92e2-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e92e2-150">-VmImagePublisher</span></span>
<span data-ttu-id="e92e2-151">Autore dell'immagine di Azure Virtual Machines Marketplace.</span><span class="sxs-lookup"><span data-stu-id="e92e2-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="e92e2-152">Impostazione predefinita: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="e92e2-152">Default: MicrosoftWindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "MicrosoftWindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e92e2-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="e92e2-153">-VmImageSku</span></span>
<span data-ttu-id="e92e2-154">SKU dell'immagine azure virtual machine marketplace.</span><span class="sxs-lookup"><span data-stu-id="e92e2-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="e92e2-155">Impostazione predefinita: Data center 2019.</span><span class="sxs-lookup"><span data-stu-id="e92e2-155">Default: 2019-Datacenter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "2019-Datacenter"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e92e2-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="e92e2-156">-VmImageVersion</span></span>
<span data-ttu-id="e92e2-157">Immagine della versione di Azure Virtual Machines Marketplace.</span><span class="sxs-lookup"><span data-stu-id="e92e2-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="e92e2-158">Impostazione predefinita: più recente.</span><span class="sxs-lookup"><span data-stu-id="e92e2-158">Default: latest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "latest"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e92e2-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="e92e2-159">-VmSize</span></span>
<span data-ttu-id="e92e2-160">Dimensioni delle macchine virtuali nel pool.</span><span class="sxs-lookup"><span data-stu-id="e92e2-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="e92e2-161">Tutte le macchine virtuali in un pool hanno le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e92e2-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="e92e2-162">Impostazione predefinita: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="e92e2-162">Default: Standard_D2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "Standard_D2"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e92e2-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e92e2-163">-Confirm</span></span>
<span data-ttu-id="e92e2-164">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e92e2-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e92e2-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e92e2-165">-WhatIf</span></span>
<span data-ttu-id="e92e2-166">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e92e2-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e92e2-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e92e2-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e92e2-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e92e2-168">CommonParameters</span></span>
<span data-ttu-id="e92e2-169">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e92e2-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e92e2-170">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e92e2-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e92e2-171">INPUT</span><span class="sxs-lookup"><span data-stu-id="e92e2-171">INPUTS</span></span>

### <span data-ttu-id="e92e2-172">System.String</span><span class="sxs-lookup"><span data-stu-id="e92e2-172">System.String</span></span>

## <span data-ttu-id="e92e2-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e92e2-173">OUTPUTS</span></span>

### <span data-ttu-id="e92e2-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e92e2-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="e92e2-175">NOTE</span><span class="sxs-lookup"><span data-stu-id="e92e2-175">NOTES</span></span>

## <span data-ttu-id="e92e2-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e92e2-176">RELATED LINKS</span></span>
