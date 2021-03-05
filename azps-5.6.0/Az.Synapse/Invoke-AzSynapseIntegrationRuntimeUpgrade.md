---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: ad5b23e29eb2d13fcad6aaf2659940dace83f4eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984045"
---
# <span data-ttu-id="20c41-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="20c41-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="20c41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20c41-102">SYNOPSIS</span></span>
<span data-ttu-id="20c41-103">Aggiorna il runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="20c41-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="20c41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20c41-104">SYNTAX</span></span>

### <span data-ttu-id="20c41-105">InvokeByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20c41-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20c41-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20c41-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20c41-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20c41-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20c41-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20c41-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20c41-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="20c41-109">DESCRIPTION</span></span>
<span data-ttu-id="20c41-110">Il cmdlet **Invoke-AzSynapseIntegrationRuntimeUpgrade** aggiorna il runtime di integrazione self-hosted, se la nuova versione è disponibile.</span><span class="sxs-lookup"><span data-stu-id="20c41-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="20c41-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20c41-111">EXAMPLES</span></span>

### <span data-ttu-id="20c41-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="20c41-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="20c41-113">Il cmdlet aggiorna il runtime di integrazione self-hosted denominato "test-selfhost-ir" nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="20c41-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="20c41-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20c41-114">PARAMETERS</span></span>

### <span data-ttu-id="20c41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c41-115">-DefaultProfile</span></span>
<span data-ttu-id="20c41-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20c41-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20c41-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20c41-117">-InputObject</span></span>
<span data-ttu-id="20c41-118">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="20c41-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20c41-119">-Name</span><span class="sxs-lookup"><span data-stu-id="20c41-119">-Name</span></span>
<span data-ttu-id="20c41-120">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="20c41-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c41-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c41-121">-ResourceGroupName</span></span>
<span data-ttu-id="20c41-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="20c41-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c41-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20c41-123">-ResourceId</span></span>
<span data-ttu-id="20c41-124">Identificatore di risorsa del runtime di integrazione di Synapse.</span><span class="sxs-lookup"><span data-stu-id="20c41-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c41-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="20c41-125">-WorkspaceName</span></span>
<span data-ttu-id="20c41-126">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="20c41-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c41-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="20c41-127">-WorkspaceObject</span></span>
<span data-ttu-id="20c41-128">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="20c41-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20c41-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20c41-129">-Confirm</span></span>
<span data-ttu-id="20c41-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20c41-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20c41-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20c41-131">-WhatIf</span></span>
<span data-ttu-id="20c41-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20c41-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20c41-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20c41-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20c41-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c41-134">CommonParameters</span></span>
<span data-ttu-id="20c41-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c41-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c41-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="20c41-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c41-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="20c41-137">INPUTS</span></span>

### <span data-ttu-id="20c41-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="20c41-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="20c41-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="20c41-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="20c41-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20c41-140">OUTPUTS</span></span>

### <span data-ttu-id="20c41-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="20c41-141">System.Void</span></span>

## <span data-ttu-id="20c41-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="20c41-142">NOTES</span></span>

## <span data-ttu-id="20c41-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20c41-143">RELATED LINKS</span></span>
