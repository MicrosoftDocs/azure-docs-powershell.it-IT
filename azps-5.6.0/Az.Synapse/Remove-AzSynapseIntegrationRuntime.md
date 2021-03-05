---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: bf15d0f533f54de589ef354d92c4cf2f600b12cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961085"
---
# <span data-ttu-id="ea102-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ea102-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="ea102-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea102-102">SYNOPSIS</span></span>
<span data-ttu-id="ea102-103">Rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ea102-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="ea102-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea102-104">SYNTAX</span></span>

### <span data-ttu-id="ea102-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea102-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea102-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea102-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea102-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea102-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea102-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea102-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea102-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ea102-109">DESCRIPTION</span></span>
<span data-ttu-id="ea102-110">Il cmdlet **Remove-AzSynapseIntegrationRuntime** rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ea102-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="ea102-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea102-111">EXAMPLES</span></span>

### <span data-ttu-id="ea102-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea102-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="ea102-113">Questo comando rimuove il runtime di integrazione denominato "test-reserved-ir" dall'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ea102-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="ea102-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea102-114">PARAMETERS</span></span>

### <span data-ttu-id="ea102-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea102-115">-DefaultProfile</span></span>
<span data-ttu-id="ea102-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea102-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea102-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ea102-117">-Force</span></span>
<span data-ttu-id="ea102-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ea102-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ea102-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea102-119">-InputObject</span></span>
<span data-ttu-id="ea102-120">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ea102-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="ea102-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ea102-121">-Name</span></span>
<span data-ttu-id="ea102-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ea102-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea102-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea102-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea102-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ea102-124">Resource group name.</span></span>

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

### <span data-ttu-id="ea102-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea102-125">-ResourceId</span></span>
<span data-ttu-id="ea102-126">Identificatore di risorsa del runtime di integrazione di Synapse.</span><span class="sxs-lookup"><span data-stu-id="ea102-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="ea102-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ea102-127">-WorkspaceName</span></span>
<span data-ttu-id="ea102-128">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="ea102-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ea102-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ea102-129">-WorkspaceObject</span></span>
<span data-ttu-id="ea102-130">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="ea102-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ea102-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea102-131">-Confirm</span></span>
<span data-ttu-id="ea102-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea102-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea102-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea102-133">-WhatIf</span></span>
<span data-ttu-id="ea102-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea102-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea102-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea102-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea102-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea102-136">CommonParameters</span></span>
<span data-ttu-id="ea102-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea102-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea102-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ea102-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea102-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="ea102-139">INPUTS</span></span>

### <span data-ttu-id="ea102-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea102-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ea102-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ea102-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ea102-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea102-142">OUTPUTS</span></span>

### <span data-ttu-id="ea102-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="ea102-143">System.Void</span></span>

## <span data-ttu-id="ea102-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="ea102-144">NOTES</span></span>

## <span data-ttu-id="ea102-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea102-145">RELATED LINKS</span></span>
