---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199999"
---
# <span data-ttu-id="16994-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="16994-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="16994-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16994-102">SYNOPSIS</span></span>
<span data-ttu-id="16994-103">Creare una nuova risorsa tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="16994-103">Create new node type resource.</span></span>

## <span data-ttu-id="16994-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16994-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16994-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16994-105">DESCRIPTION</span></span>
<span data-ttu-id="16994-106">Creare una nuova risorsa tipo di nodo per un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="16994-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="16994-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16994-107">EXAMPLES</span></span>

### <span data-ttu-id="16994-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16994-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="16994-109">Creare un tipo di nodo primario con 3 nodi.</span><span class="sxs-lookup"><span data-stu-id="16994-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="16994-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="16994-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="16994-111">Crea il tipo di nodo primario con 5 nodi e specificando le proprietà di posizionamento, le capacità, l'applicazione e le porte effimere.</span><span class="sxs-lookup"><span data-stu-id="16994-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="16994-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16994-112">PARAMETERS</span></span>

### <span data-ttu-id="16994-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="16994-113">-ApplicationEndPort</span></span>
<span data-ttu-id="16994-114">Porta di fine applicazione di un intervallo di porte.</span><span class="sxs-lookup"><span data-stu-id="16994-114">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="16994-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="16994-115">-ApplicationStartPort</span></span>
<span data-ttu-id="16994-116">Porta di avvio dell'applicazione di un intervallo di porte.</span><span class="sxs-lookup"><span data-stu-id="16994-116">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="16994-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16994-117">-AsJob</span></span>
<span data-ttu-id="16994-118">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="16994-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="16994-119">-Capacità</span><span class="sxs-lookup"><span data-stu-id="16994-119">-Capacity</span></span>
<span data-ttu-id="16994-120">I tag di capacità applicati ai nodi del tipo di nodo come coppie chiave/valore, il gestore di risorse del cluster usa questi tag per comprendere la quantità di risorse di un nodo.</span><span class="sxs-lookup"><span data-stu-id="16994-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="16994-121">L'aggiornamento di questa operazione sostituirà i valori correnti.</span><span class="sxs-lookup"><span data-stu-id="16994-121">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="16994-122">-Clustername</span><span class="sxs-lookup"><span data-stu-id="16994-122">-ClusterName</span></span>
<span data-ttu-id="16994-123">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="16994-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="16994-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16994-124">-DefaultProfile</span></span>
<span data-ttu-id="16994-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16994-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16994-126">-FissoDimensione</span><span class="sxs-lookup"><span data-stu-id="16994-126">-DiskSize</span></span>
<span data-ttu-id="16994-127">Dimensioni del disco per ogni VM nel tipo di nodo in GBs.</span><span class="sxs-lookup"><span data-stu-id="16994-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="16994-128">Impostazione predefinita 100.</span><span class="sxs-lookup"><span data-stu-id="16994-128">Default 100.</span></span>

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

### <span data-ttu-id="16994-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="16994-129">-EphemeralEndPort</span></span>
<span data-ttu-id="16994-130">Porta finale effimera di un intervallo di porte.</span><span class="sxs-lookup"><span data-stu-id="16994-130">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="16994-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="16994-131">-EphemeralStartPort</span></span>
<span data-ttu-id="16994-132">Porta di inizio effimera di un intervallo di porte.</span><span class="sxs-lookup"><span data-stu-id="16994-132">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="16994-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="16994-133">-InstanceCount</span></span>
<span data-ttu-id="16994-134">Numero di nodi nel tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="16994-134">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="16994-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="16994-135">-Name</span></span>
<span data-ttu-id="16994-136">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="16994-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="16994-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="16994-137">-PlacementProperty</span></span>
<span data-ttu-id="16994-138">I tag di posizionamento applicati ai nodi del tipo di nodo come coppie chiave/valore, che possono essere usati per indicare la posizione in cui devono essere eseguiti determinati servizi (carico di lavoro).</span><span class="sxs-lookup"><span data-stu-id="16994-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="16994-139">L'aggiornamento di questa operazione sostituirà i valori correnti.</span><span class="sxs-lookup"><span data-stu-id="16994-139">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="16994-140">-Primaria</span><span class="sxs-lookup"><span data-stu-id="16994-140">-Primary</span></span>
<span data-ttu-id="16994-141">Specifica se il tipo di nodo è primario.</span><span class="sxs-lookup"><span data-stu-id="16994-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="16994-142">In questo tipo di nodo verranno eseguiti i servizi di sistema.</span><span class="sxs-lookup"><span data-stu-id="16994-142">On this node type will run system services.</span></span>
<span data-ttu-id="16994-143">Un solo tipo di nodo deve essere contrassegnato come primario.</span><span class="sxs-lookup"><span data-stu-id="16994-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="16994-144">Il tipo di nodo primario non può essere eliminato o modificato per i cluster esistenti.</span><span class="sxs-lookup"><span data-stu-id="16994-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="16994-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16994-145">-ResourceGroupName</span></span>
<span data-ttu-id="16994-146">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="16994-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="16994-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="16994-147">-VmImageOffer</span></span>
<span data-ttu-id="16994-148">Tipo di offerta dell'immagine di Azure Virtual Machines Marketplace.</span><span class="sxs-lookup"><span data-stu-id="16994-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="16994-149">Impostazione predefinita: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="16994-149">Default: WindowsServer.</span></span>

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

### <span data-ttu-id="16994-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="16994-150">-VmImagePublisher</span></span>
<span data-ttu-id="16994-151">L'editore dell'immagine di Azure Virtual Machines Marketplace.</span><span class="sxs-lookup"><span data-stu-id="16994-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="16994-152">Impostazione predefinita: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="16994-152">Default: MicrosoftWindowsServer.</span></span>

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

### <span data-ttu-id="16994-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="16994-153">-VmImageSku</span></span>
<span data-ttu-id="16994-154">SKU dell'immagine di Azure Virtual Machines Marketplace.</span><span class="sxs-lookup"><span data-stu-id="16994-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="16994-155">Impostazione predefinita: 2019-datacenter.</span><span class="sxs-lookup"><span data-stu-id="16994-155">Default: 2019-Datacenter.</span></span>

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

### <span data-ttu-id="16994-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="16994-156">-VmImageVersion</span></span>
<span data-ttu-id="16994-157">La versione dell'immagine di Azure Virtual Machines Marketplace.</span><span class="sxs-lookup"><span data-stu-id="16994-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="16994-158">Impostazione predefinita: ultima.</span><span class="sxs-lookup"><span data-stu-id="16994-158">Default: latest.</span></span>

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

### <span data-ttu-id="16994-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="16994-159">-VmSize</span></span>
<span data-ttu-id="16994-160">Le dimensioni delle macchine virtuali nel pool.</span><span class="sxs-lookup"><span data-stu-id="16994-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="16994-161">Tutte le macchine virtuali in un pool hanno le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="16994-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="16994-162">Impostazione predefinita: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="16994-162">Default: Standard_D2.</span></span>

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

### <span data-ttu-id="16994-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="16994-163">-Confirm</span></span>
<span data-ttu-id="16994-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16994-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16994-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16994-165">-WhatIf</span></span>
<span data-ttu-id="16994-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16994-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16994-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16994-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16994-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16994-168">CommonParameters</span></span>
<span data-ttu-id="16994-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16994-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16994-170">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16994-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16994-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16994-171">INPUTS</span></span>

### <span data-ttu-id="16994-172">System. String</span><span class="sxs-lookup"><span data-stu-id="16994-172">System.String</span></span>

## <span data-ttu-id="16994-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16994-173">OUTPUTS</span></span>

### <span data-ttu-id="16994-174">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="16994-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="16994-175">Note</span><span class="sxs-lookup"><span data-stu-id="16994-175">NOTES</span></span>

## <span data-ttu-id="16994-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16994-176">RELATED LINKS</span></span>