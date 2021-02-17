---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198351"
---
# <span data-ttu-id="14d85-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="14d85-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="14d85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14d85-102">SYNOPSIS</span></span>
<span data-ttu-id="14d85-103">Rimuovere un nodo con il nome specificato in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="14d85-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="14d85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14d85-104">SYNTAX</span></span>

### <span data-ttu-id="14d85-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14d85-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14d85-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14d85-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14d85-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14d85-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14d85-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14d85-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14d85-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14d85-109">DESCRIPTION</span></span>
<span data-ttu-id="14d85-110">Il cmdlet **Remove-AzSynapseIntegrationRuntimeNode** rimuove un nodo in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="14d85-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="14d85-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14d85-111">EXAMPLES</span></span>

### <span data-ttu-id="14d85-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14d85-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="14d85-113">Rimuovere un nodo con il nome specificato in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="14d85-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="14d85-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14d85-114">PARAMETERS</span></span>

### <span data-ttu-id="14d85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d85-115">-DefaultProfile</span></span>
<span data-ttu-id="14d85-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14d85-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14d85-117">-Force</span><span class="sxs-lookup"><span data-stu-id="14d85-117">-Force</span></span>
<span data-ttu-id="14d85-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="14d85-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="14d85-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14d85-119">-InputObject</span></span>
<span data-ttu-id="14d85-120">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="14d85-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14d85-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="14d85-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="14d85-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="14d85-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d85-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="14d85-123">-NodeName</span></span>
<span data-ttu-id="14d85-124">Nome del nodo di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="14d85-124">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14d85-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14d85-125">-ResourceGroupName</span></span>
<span data-ttu-id="14d85-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14d85-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d85-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14d85-127">-ResourceId</span></span>
<span data-ttu-id="14d85-128">Identificatore di risorsa del runtime di integrazione synapse.</span><span class="sxs-lookup"><span data-stu-id="14d85-128">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d85-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="14d85-129">-WorkspaceName</span></span>
<span data-ttu-id="14d85-130">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="14d85-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d85-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="14d85-131">-WorkspaceObject</span></span>
<span data-ttu-id="14d85-132">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="14d85-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14d85-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14d85-133">-Confirm</span></span>
<span data-ttu-id="14d85-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14d85-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14d85-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14d85-135">-WhatIf</span></span>
<span data-ttu-id="14d85-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14d85-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14d85-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14d85-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14d85-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d85-138">CommonParameters</span></span>
<span data-ttu-id="14d85-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d85-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d85-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14d85-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d85-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="14d85-141">INPUTS</span></span>

### <span data-ttu-id="14d85-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="14d85-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="14d85-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="14d85-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="14d85-144">System.String</span><span class="sxs-lookup"><span data-stu-id="14d85-144">System.String</span></span>

## <span data-ttu-id="14d85-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14d85-145">OUTPUTS</span></span>

### <span data-ttu-id="14d85-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="14d85-146">System.Void</span></span>

## <span data-ttu-id="14d85-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="14d85-147">NOTES</span></span>

## <span data-ttu-id="14d85-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14d85-148">RELATED LINKS</span></span>
