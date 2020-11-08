---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193818"
---
# <span data-ttu-id="236e4-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="236e4-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="236e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="236e4-102">SYNOPSIS</span></span>
<span data-ttu-id="236e4-103">Rimuovere il tipo di nodo o i nodi specifici all'interno del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="236e4-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="236e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="236e4-104">SYNTAX</span></span>

### <span data-ttu-id="236e4-105">DeleteNodeTypeByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="236e4-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="236e4-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="236e4-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="236e4-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="236e4-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="236e4-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="236e4-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="236e4-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="236e4-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="236e4-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="236e4-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="236e4-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="236e4-111">DESCRIPTION</span></span>
<span data-ttu-id="236e4-112">Rimuovere il tipo di nodo o i nodi specifici all'interno del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="236e4-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="236e4-113">Se paremter-nodeName viene usato, verranno rimossi solo i nodi specificati.</span><span class="sxs-lookup"><span data-stu-id="236e4-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="236e4-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="236e4-114">EXAMPLES</span></span>

### <span data-ttu-id="236e4-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="236e4-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="236e4-116">Rimuovi tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="236e4-116">Remove node type.</span></span>

### <span data-ttu-id="236e4-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="236e4-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="236e4-118">Rimuovi tipo di nodo con piping.</span><span class="sxs-lookup"><span data-stu-id="236e4-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="236e4-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="236e4-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="236e4-120">Rimuovere 2 nodi dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="236e4-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="236e4-121">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="236e4-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="236e4-122">Rimuovere 2 nodi dal tipo di nodo con piping.</span><span class="sxs-lookup"><span data-stu-id="236e4-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="236e4-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="236e4-123">PARAMETERS</span></span>

### <span data-ttu-id="236e4-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="236e4-124">-AsJob</span></span>
<span data-ttu-id="236e4-125">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="236e4-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="236e4-126">-Clustername</span><span class="sxs-lookup"><span data-stu-id="236e4-126">-ClusterName</span></span>
<span data-ttu-id="236e4-127">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="236e4-127">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="236e4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="236e4-128">-DefaultProfile</span></span>
<span data-ttu-id="236e4-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="236e4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="236e4-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="236e4-130">-ForceRemoveNode</span></span>
<span data-ttu-id="236e4-131">L'uso di questo contrassegno forza la rimozione anche se il tessuto di servizio non è in grado di disabilitare i nodi.</span><span class="sxs-lookup"><span data-stu-id="236e4-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="236e4-132">USA con cautela poiché questo può causare perdite di dati se i carichi di lavoro con stato sono in esecuzione nei nodi o se il cluster non contiene abbastanza nodi di inizializzazione dopo opearion.</span><span class="sxs-lookup"><span data-stu-id="236e4-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="236e4-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="236e4-133">-InputObject</span></span>
<span data-ttu-id="236e4-134">Risorsa tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="236e4-134">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: DeleteNodeTypeByObj, DeleteNodeByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="236e4-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="236e4-135">-Name</span></span>
<span data-ttu-id="236e4-136">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="236e4-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="236e4-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="236e4-137">-NodeName</span></span>
<span data-ttu-id="236e4-138">Elenco di nomi di nodo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="236e4-138">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="236e4-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="236e4-139">-PassThru</span></span>
<span data-ttu-id="236e4-140">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="236e4-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="236e4-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="236e4-141">-ResourceGroupName</span></span>
<span data-ttu-id="236e4-142">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="236e4-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="236e4-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="236e4-143">-ResourceId</span></span>
<span data-ttu-id="236e4-144">ID risorsa tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="236e4-144">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeById, DeleteNodeById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="236e4-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="236e4-145">-Confirm</span></span>
<span data-ttu-id="236e4-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="236e4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="236e4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="236e4-147">-WhatIf</span></span>
<span data-ttu-id="236e4-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="236e4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="236e4-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="236e4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="236e4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="236e4-150">CommonParameters</span></span>
<span data-ttu-id="236e4-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="236e4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="236e4-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="236e4-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="236e4-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="236e4-153">INPUTS</span></span>

### <span data-ttu-id="236e4-154">System. String</span><span class="sxs-lookup"><span data-stu-id="236e4-154">System.String</span></span>

## <span data-ttu-id="236e4-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="236e4-155">OUTPUTS</span></span>

### <span data-ttu-id="236e4-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="236e4-156">System.Boolean</span></span>

## <span data-ttu-id="236e4-157">Note</span><span class="sxs-lookup"><span data-stu-id="236e4-157">NOTES</span></span>

## <span data-ttu-id="236e4-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="236e4-158">RELATED LINKS</span></span>
