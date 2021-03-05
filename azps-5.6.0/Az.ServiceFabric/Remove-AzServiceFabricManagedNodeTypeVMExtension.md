---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: 410509f59cc34dd139761a3e4ddb5de9907ef720
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005454"
---
# <span data-ttu-id="e4be1-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="e4be1-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="e4be1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4be1-102">SYNOPSIS</span></span>
<span data-ttu-id="e4be1-103">Rimuovere l'estensione della macchina virtuale dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="e4be1-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="e4be1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4be1-104">SYNTAX</span></span>

### <span data-ttu-id="e4be1-105">ByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4be1-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4be1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e4be1-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4be1-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e4be1-107">DESCRIPTION</span></span>
<span data-ttu-id="e4be1-108">Rimuovere l'estensione della macchina virtuale dal tipo di nodo in base al nome.</span><span class="sxs-lookup"><span data-stu-id="e4be1-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="e4be1-109">Usare [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) ed esaminare la proprietà VmExtensions per vedere l'estensione corrente nel tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="e4be1-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="e4be1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4be1-110">EXAMPLES</span></span>

### <span data-ttu-id="e4be1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e4be1-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="e4be1-112">Rimuovere l'estensione dal tipo di nodo in base al nome.</span><span class="sxs-lookup"><span data-stu-id="e4be1-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="e4be1-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e4be1-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="e4be1-114">Rimuovere l'estensione dal tipo di nodo in base al nome, con piping.</span><span class="sxs-lookup"><span data-stu-id="e4be1-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="e4be1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4be1-115">PARAMETERS</span></span>

### <span data-ttu-id="e4be1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4be1-116">-AsJob</span></span>
<span data-ttu-id="e4be1-117">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="e4be1-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e4be1-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e4be1-118">-ClusterName</span></span>
<span data-ttu-id="e4be1-119">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="e4be1-119">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4be1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4be1-120">-DefaultProfile</span></span>
<span data-ttu-id="e4be1-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4be1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4be1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4be1-122">-InputObject</span></span>
<span data-ttu-id="e4be1-123">Risorsa tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="e4be1-123">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4be1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e4be1-124">-Name</span></span>
<span data-ttu-id="e4be1-125">nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="e4be1-125">extension name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4be1-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="e4be1-126">-NodeTypeName</span></span>
<span data-ttu-id="e4be1-127">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="e4be1-127">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4be1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4be1-128">-PassThru</span></span>
<span data-ttu-id="e4be1-129">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="e4be1-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e4be1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4be1-130">-ResourceGroupName</span></span>
<span data-ttu-id="e4be1-131">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4be1-131">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4be1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4be1-132">-Confirm</span></span>
<span data-ttu-id="e4be1-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4be1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4be1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4be1-134">-WhatIf</span></span>
<span data-ttu-id="e4be1-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4be1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4be1-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4be1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4be1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4be1-137">CommonParameters</span></span>
<span data-ttu-id="e4be1-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4be1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4be1-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e4be1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4be1-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="e4be1-140">INPUTS</span></span>

### <span data-ttu-id="e4be1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e4be1-141">System.String</span></span>

## <span data-ttu-id="e4be1-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4be1-142">OUTPUTS</span></span>

### <span data-ttu-id="e4be1-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e4be1-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="e4be1-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="e4be1-144">NOTES</span></span>

## <span data-ttu-id="e4be1-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4be1-145">RELATED LINKS</span></span>
