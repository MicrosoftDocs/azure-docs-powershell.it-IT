---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183463"
---
# <span data-ttu-id="dd630-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="dd630-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="dd630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd630-102">SYNOPSIS</span></span>
<span data-ttu-id="dd630-103">Rimuovere il tipo di nodo o nodi specifici all'interno del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="dd630-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="dd630-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd630-104">SYNTAX</span></span>

### <span data-ttu-id="dd630-105">DeleteNodeTypeByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd630-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd630-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="dd630-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd630-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="dd630-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd630-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="dd630-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd630-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="dd630-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd630-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="dd630-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd630-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dd630-111">DESCRIPTION</span></span>
<span data-ttu-id="dd630-112">Rimuovere il tipo di nodo o nodi specifici all'interno del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="dd630-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="dd630-113">Se si usa il paremter -NodeName, verranno rimossi solo i nodi specificati.</span><span class="sxs-lookup"><span data-stu-id="dd630-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="dd630-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd630-114">EXAMPLES</span></span>

### <span data-ttu-id="dd630-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dd630-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="dd630-116">Rimuovere il tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="dd630-116">Remove node type.</span></span>

### <span data-ttu-id="dd630-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dd630-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="dd630-118">Rimuovi tipo di nodo, con piping.</span><span class="sxs-lookup"><span data-stu-id="dd630-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="dd630-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="dd630-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="dd630-120">Rimuovere 2 nodi dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="dd630-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="dd630-121">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="dd630-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="dd630-122">Rimuovere 2 nodi dal tipo di nodo, con piping.</span><span class="sxs-lookup"><span data-stu-id="dd630-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="dd630-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd630-123">PARAMETERS</span></span>

### <span data-ttu-id="dd630-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd630-124">-AsJob</span></span>
<span data-ttu-id="dd630-125">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="dd630-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="dd630-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dd630-126">-ClusterName</span></span>
<span data-ttu-id="dd630-127">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="dd630-127">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="dd630-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd630-128">-DefaultProfile</span></span>
<span data-ttu-id="dd630-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd630-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd630-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="dd630-130">-ForceRemoveNode</span></span>
<span data-ttu-id="dd630-131">L'uso di questo flag forza la rimozione anche se non è possibile disabilitare i nodi.</span><span class="sxs-lookup"><span data-stu-id="dd630-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="dd630-132">Usare con cautela perché ciò potrebbe causare la perdita di dati se nei nodi sono in esecuzione carichi di lavoro con stato oppure potrebbe causare il downing del cluster se dopo l'opearion non ci sono abbastanza nodi di proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd630-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

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

### <span data-ttu-id="dd630-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd630-133">-InputObject</span></span>
<span data-ttu-id="dd630-134">Risorsa tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="dd630-134">Node type resource</span></span>

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

### <span data-ttu-id="dd630-135">-Name</span><span class="sxs-lookup"><span data-stu-id="dd630-135">-Name</span></span>
<span data-ttu-id="dd630-136">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="dd630-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="dd630-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="dd630-137">-NodeName</span></span>
<span data-ttu-id="dd630-138">Elenco dei nomi dei nodi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="dd630-138">List of node names for the operation.</span></span>

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

### <span data-ttu-id="dd630-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd630-139">-PassThru</span></span>
<span data-ttu-id="dd630-140">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="dd630-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="dd630-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd630-141">-ResourceGroupName</span></span>
<span data-ttu-id="dd630-142">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd630-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="dd630-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd630-143">-ResourceId</span></span>
<span data-ttu-id="dd630-144">ID risorsa tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="dd630-144">Node type resource id</span></span>

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

### <span data-ttu-id="dd630-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd630-145">-Confirm</span></span>
<span data-ttu-id="dd630-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd630-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd630-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd630-147">-WhatIf</span></span>
<span data-ttu-id="dd630-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd630-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd630-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd630-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd630-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd630-150">CommonParameters</span></span>
<span data-ttu-id="dd630-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd630-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd630-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dd630-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd630-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="dd630-153">INPUTS</span></span>

### <span data-ttu-id="dd630-154">System.String</span><span class="sxs-lookup"><span data-stu-id="dd630-154">System.String</span></span>

## <span data-ttu-id="dd630-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd630-155">OUTPUTS</span></span>

### <span data-ttu-id="dd630-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd630-156">System.Boolean</span></span>

## <span data-ttu-id="dd630-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="dd630-157">NOTES</span></span>

## <span data-ttu-id="dd630-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd630-158">RELATED LINKS</span></span>
