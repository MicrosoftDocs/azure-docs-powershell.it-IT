---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191142"
---
# <span data-ttu-id="d3e69-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d3e69-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="d3e69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3e69-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e69-103">Imposta le proprietà delle risorse del tipo di nodo o esegue azioni di reimage su specifici tipi di nodo con il parametro -Reimage.</span><span class="sxs-lookup"><span data-stu-id="d3e69-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="d3e69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3e69-104">SYNTAX</span></span>

### <span data-ttu-id="d3e69-105">ByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3e69-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e69-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="d3e69-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3e69-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="d3e69-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e69-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="d3e69-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e69-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="d3e69-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e69-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="d3e69-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3e69-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d3e69-111">DESCRIPTION</span></span>
<span data-ttu-id="d3e69-112">Imposta le proprietà delle risorse del tipo di nodo o esegue azioni di reimage su specifici tipi di nodo con il parametro -Reimage.</span><span class="sxs-lookup"><span data-stu-id="d3e69-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="d3e69-113">Durante l'operazione di ripristino, i nodi dell'infrastruttura del servizio verranno disabilitati prima di riprovare le macchine virtuali e averli ri abilitati nuovamente una volta tornati.</span><span class="sxs-lookup"><span data-stu-id="d3e69-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="d3e69-114">Se questa operazione viene eseguita nei tipi di nodo primario, l'operazione potrebbe richiedere del tempo perché potrebbe non essere possibile visualizzare nuovamente tutti i nodi contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="d3e69-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="d3e69-115">Usare -ForceReimage forzare l'operazione anche se l'infrastruttura del servizio non è in grado di disabilitare i nodi, ma usare con cautela perché ciò potrebbe causare la perdita di dati se nel nodo sono in esecuzione carichi di lavoro con stato.</span><span class="sxs-lookup"><span data-stu-id="d3e69-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="d3e69-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3e69-116">EXAMPLES</span></span>

### <span data-ttu-id="d3e69-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3e69-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="d3e69-118">Aggiornare il numero di istanze del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="d3e69-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="d3e69-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d3e69-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="d3e69-120">Aggiornare le properite della posizione del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="d3e69-120">Update placement properites of the node type.</span></span> <span data-ttu-id="d3e69-121">In questo modo verranno sovrascritte le precedenti properite del posizionamento, se presenti.</span><span class="sxs-lookup"><span data-stu-id="d3e69-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="d3e69-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d3e69-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="d3e69-123">Reimage node 0 and 3 on the node type.</span><span class="sxs-lookup"><span data-stu-id="d3e69-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="d3e69-124">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="d3e69-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="d3e69-125">Aggiornare il numero di istanze del tipo di nodo con piping.</span><span class="sxs-lookup"><span data-stu-id="d3e69-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="d3e69-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3e69-126">PARAMETERS</span></span>

### <span data-ttu-id="d3e69-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="d3e69-127">-ApplicationEndPort</span></span>
<span data-ttu-id="d3e69-128">Porta finale dell'applicazione per un intervallo di porte.</span><span class="sxs-lookup"><span data-stu-id="d3e69-128">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="d3e69-129">-ApplicationStartPort</span></span>
<span data-ttu-id="d3e69-130">Porta di avvio dell'applicazione di un intervallo di porte.</span><span class="sxs-lookup"><span data-stu-id="d3e69-130">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3e69-131">-AsJob</span></span>
<span data-ttu-id="d3e69-132">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="d3e69-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d3e69-133">-Capacità</span><span class="sxs-lookup"><span data-stu-id="d3e69-133">-Capacity</span></span>
<span data-ttu-id="d3e69-134">Tag di capacità applicati ai nodi nel tipo di nodo come coppie chiave/valore. Gestione risorse cluster usa questi tag per determinare la quantità di risorse di un nodo.</span><span class="sxs-lookup"><span data-stu-id="d3e69-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="d3e69-135">L'aggiornamento eseguirà l'override dei valori correnti.</span><span class="sxs-lookup"><span data-stu-id="d3e69-135">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-136">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d3e69-136">-ClusterName</span></span>
<span data-ttu-id="d3e69-137">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="d3e69-137">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e69-138">-DefaultProfile</span></span>
<span data-ttu-id="d3e69-139">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3e69-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3e69-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="d3e69-140">-EphemeralEndPort</span></span>
<span data-ttu-id="d3e69-141">Porta finale effimera di una gamma di porte.</span><span class="sxs-lookup"><span data-stu-id="d3e69-141">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="d3e69-142">-EphemeralStartPort</span></span>
<span data-ttu-id="d3e69-143">Porta iniziale effimera di un intervallo di porte.</span><span class="sxs-lookup"><span data-stu-id="d3e69-143">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="d3e69-144">-ForceReimage</span></span>
<span data-ttu-id="d3e69-145">L'uso di questo flag forza la rimozione anche se non è possibile disabilitare i nodi.</span><span class="sxs-lookup"><span data-stu-id="d3e69-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="d3e69-146">Usare con cautela perché ciò potrebbe causare la perdita di dati se nel nodo sono in esecuzione carichi di lavoro con stato.</span><span class="sxs-lookup"><span data-stu-id="d3e69-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3e69-147">-InputObject</span></span>
<span data-ttu-id="d3e69-148">Risorsa tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="d3e69-148">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj, ReimageByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="d3e69-149">-InstanceCount</span></span>
<span data-ttu-id="d3e69-150">Numero di nodi nel tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="d3e69-150">The number of nodes in the node type.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-151">-Name</span><span class="sxs-lookup"><span data-stu-id="d3e69-151">-Name</span></span>
<span data-ttu-id="d3e69-152">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="d3e69-152">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-153">-NodeName</span><span class="sxs-lookup"><span data-stu-id="d3e69-153">-NodeName</span></span>
<span data-ttu-id="d3e69-154">Elenco dei nomi dei nodi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d3e69-154">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3e69-155">-PassThru</span></span>
<span data-ttu-id="d3e69-156">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="d3e69-156">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="d3e69-157">-PlacementProperty</span></span>
<span data-ttu-id="d3e69-158">Tag di posizionamento applicati ai nodi nel tipo di nodo come coppie chiave/valore, che possono essere usati per indicare dove eseguire determinati servizi (carico di lavoro).</span><span class="sxs-lookup"><span data-stu-id="d3e69-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="d3e69-159">L'aggiornamento eseguirà l'override dei valori correnti.</span><span class="sxs-lookup"><span data-stu-id="d3e69-159">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-160">-Reimage</span><span class="sxs-lookup"><span data-stu-id="d3e69-160">-Reimage</span></span>
<span data-ttu-id="d3e69-161">Specificare per visualizzare nuovamente i nodi dell'immagine nel tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="d3e69-161">Specify to reimage nodes on the node type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e69-162">-ResourceGroupName</span></span>
<span data-ttu-id="d3e69-163">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3e69-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e69-164">-ResourceId</span></span>
<span data-ttu-id="d3e69-165">ID risorsa tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="d3e69-165">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsById, ReimageById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e69-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3e69-166">-Confirm</span></span>
<span data-ttu-id="d3e69-167">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3e69-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e69-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e69-168">-WhatIf</span></span>
<span data-ttu-id="d3e69-169">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3e69-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3e69-170">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3e69-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3e69-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e69-171">CommonParameters</span></span>
<span data-ttu-id="d3e69-172">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e69-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e69-173">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3e69-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e69-174">INPUT</span><span class="sxs-lookup"><span data-stu-id="d3e69-174">INPUTS</span></span>

### <span data-ttu-id="d3e69-175">System.String</span><span class="sxs-lookup"><span data-stu-id="d3e69-175">System.String</span></span>

## <span data-ttu-id="d3e69-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3e69-176">OUTPUTS</span></span>

### <span data-ttu-id="d3e69-177">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d3e69-177">System.Boolean</span></span>

## <span data-ttu-id="d3e69-178">NOTE</span><span class="sxs-lookup"><span data-stu-id="d3e69-178">NOTES</span></span>

## <span data-ttu-id="d3e69-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3e69-179">RELATED LINKS</span></span>
