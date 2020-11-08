---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193816"
---
# <span data-ttu-id="aac77-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="aac77-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="aac77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aac77-102">SYNOPSIS</span></span>
<span data-ttu-id="aac77-103">Rimuovere l'estensione VM dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="aac77-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="aac77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aac77-104">SYNTAX</span></span>

### <span data-ttu-id="aac77-105">ByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aac77-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aac77-106">ByName</span><span class="sxs-lookup"><span data-stu-id="aac77-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aac77-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aac77-107">DESCRIPTION</span></span>
<span data-ttu-id="aac77-108">Rimuovere l'estensione VM dal tipo di nodo per nome.</span><span class="sxs-lookup"><span data-stu-id="aac77-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="aac77-109">USA [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) e osserva la proprietà VmExtensions per visualizzare l'estensione corrente nel tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="aac77-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="aac77-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aac77-110">EXAMPLES</span></span>

### <span data-ttu-id="aac77-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aac77-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="aac77-112">Rimuovi estensione dal tipo di nodo per nome.</span><span class="sxs-lookup"><span data-stu-id="aac77-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="aac77-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="aac77-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="aac77-114">Rimuovi estensione da tipo di nodo per nome, con piping.</span><span class="sxs-lookup"><span data-stu-id="aac77-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="aac77-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aac77-115">PARAMETERS</span></span>

### <span data-ttu-id="aac77-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aac77-116">-AsJob</span></span>
<span data-ttu-id="aac77-117">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="aac77-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="aac77-118">-Clustername</span><span class="sxs-lookup"><span data-stu-id="aac77-118">-ClusterName</span></span>
<span data-ttu-id="aac77-119">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="aac77-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="aac77-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac77-120">-DefaultProfile</span></span>
<span data-ttu-id="aac77-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aac77-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aac77-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aac77-122">-InputObject</span></span>
<span data-ttu-id="aac77-123">Risorsa tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="aac77-123">Node type resource</span></span>

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

### <span data-ttu-id="aac77-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="aac77-124">-Name</span></span>
<span data-ttu-id="aac77-125">nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="aac77-125">extension name.</span></span>

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

### <span data-ttu-id="aac77-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="aac77-126">-NodeTypeName</span></span>
<span data-ttu-id="aac77-127">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="aac77-127">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="aac77-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aac77-128">-PassThru</span></span>
<span data-ttu-id="aac77-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="aac77-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="aac77-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac77-130">-ResourceGroupName</span></span>
<span data-ttu-id="aac77-131">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aac77-131">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="aac77-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aac77-132">-Confirm</span></span>
<span data-ttu-id="aac77-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aac77-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aac77-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aac77-134">-WhatIf</span></span>
<span data-ttu-id="aac77-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aac77-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aac77-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aac77-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aac77-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac77-137">CommonParameters</span></span>
<span data-ttu-id="aac77-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aac77-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac77-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aac77-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac77-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aac77-140">INPUTS</span></span>

### <span data-ttu-id="aac77-141">System. String</span><span class="sxs-lookup"><span data-stu-id="aac77-141">System.String</span></span>

## <span data-ttu-id="aac77-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aac77-142">OUTPUTS</span></span>

### <span data-ttu-id="aac77-143">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="aac77-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="aac77-144">Note</span><span class="sxs-lookup"><span data-stu-id="aac77-144">NOTES</span></span>

## <span data-ttu-id="aac77-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aac77-145">RELATED LINKS</span></span>
