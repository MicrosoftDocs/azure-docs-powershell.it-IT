---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183455"
---
# <span data-ttu-id="39144-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="39144-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="39144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39144-102">SYNOPSIS</span></span>
<span data-ttu-id="39144-103">Rimuovere l'estensione della macchina virtuale dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="39144-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="39144-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39144-104">SYNTAX</span></span>

### <span data-ttu-id="39144-105">ByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39144-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39144-106">ByName</span><span class="sxs-lookup"><span data-stu-id="39144-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39144-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39144-107">DESCRIPTION</span></span>
<span data-ttu-id="39144-108">Rimuovere l'estensione della macchina virtuale dal tipo di nodo in base al nome.</span><span class="sxs-lookup"><span data-stu-id="39144-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="39144-109">Usare [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) ed esaminare la proprietà VmExtensions per vedere l'estensione corrente nel tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="39144-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="39144-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39144-110">EXAMPLES</span></span>

### <span data-ttu-id="39144-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="39144-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="39144-112">Rimuovere l'estensione dal tipo di nodo in base al nome.</span><span class="sxs-lookup"><span data-stu-id="39144-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="39144-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="39144-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="39144-114">Rimuovere l'estensione dal tipo di nodo in base al nome, con piping.</span><span class="sxs-lookup"><span data-stu-id="39144-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="39144-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39144-115">PARAMETERS</span></span>

### <span data-ttu-id="39144-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39144-116">-AsJob</span></span>
<span data-ttu-id="39144-117">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="39144-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="39144-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="39144-118">-ClusterName</span></span>
<span data-ttu-id="39144-119">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="39144-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="39144-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39144-120">-DefaultProfile</span></span>
<span data-ttu-id="39144-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39144-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39144-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39144-122">-InputObject</span></span>
<span data-ttu-id="39144-123">Risorsa tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="39144-123">Node type resource</span></span>

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

### <span data-ttu-id="39144-124">-Name</span><span class="sxs-lookup"><span data-stu-id="39144-124">-Name</span></span>
<span data-ttu-id="39144-125">nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="39144-125">extension name.</span></span>

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

### <span data-ttu-id="39144-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="39144-126">-NodeTypeName</span></span>
<span data-ttu-id="39144-127">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="39144-127">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="39144-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39144-128">-PassThru</span></span>
<span data-ttu-id="39144-129">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="39144-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="39144-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39144-130">-ResourceGroupName</span></span>
<span data-ttu-id="39144-131">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39144-131">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="39144-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39144-132">-Confirm</span></span>
<span data-ttu-id="39144-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39144-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39144-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39144-134">-WhatIf</span></span>
<span data-ttu-id="39144-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39144-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39144-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39144-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39144-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39144-137">CommonParameters</span></span>
<span data-ttu-id="39144-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39144-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39144-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39144-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39144-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="39144-140">INPUTS</span></span>

### <span data-ttu-id="39144-141">System.String</span><span class="sxs-lookup"><span data-stu-id="39144-141">System.String</span></span>

## <span data-ttu-id="39144-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39144-142">OUTPUTS</span></span>

### <span data-ttu-id="39144-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="39144-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="39144-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="39144-144">NOTES</span></span>

## <span data-ttu-id="39144-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39144-145">RELATED LINKS</span></span>
