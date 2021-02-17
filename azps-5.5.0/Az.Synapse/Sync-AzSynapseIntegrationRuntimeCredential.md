---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207595"
---
# <span data-ttu-id="cc7c7-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="cc7c7-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="cc7c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc7c7-102">SYNOPSIS</span></span>
<span data-ttu-id="cc7c7-103">Sincronizza le credenziali tra i nodi di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="cc7c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc7c7-104">SYNTAX</span></span>

### <span data-ttu-id="cc7c7-105">StopByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cc7c7-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc7c7-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc7c7-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc7c7-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc7c7-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc7c7-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc7c7-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc7c7-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cc7c7-109">DESCRIPTION</span></span>
<span data-ttu-id="cc7c7-110">Il cmdlet **Sync-AzSynapseIntegrationRuntimeCredential** sincronizza le credenziali locali tra i nodi di runtime di integrazione, che forzano le credenziali a essere identiche in tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="cc7c7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc7c7-111">EXAMPLES</span></span>

### <span data-ttu-id="cc7c7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cc7c7-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="cc7c7-113">Sincronizza le credenziali tra i nodi di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="cc7c7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc7c7-114">PARAMETERS</span></span>

### <span data-ttu-id="cc7c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc7c7-115">-DefaultProfile</span></span>
<span data-ttu-id="cc7c7-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc7c7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cc7c7-117">-Force</span></span>
<span data-ttu-id="cc7c7-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cc7c7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc7c7-119">-InputObject</span></span>
<span data-ttu-id="cc7c7-120">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7c7-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="cc7c7-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="cc7c7-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc7c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc7c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="cc7c7-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc7c7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc7c7-125">-ResourceId</span></span>
<span data-ttu-id="cc7c7-126">Identificatore di risorsa del runtime di integrazione synapse.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc7c7-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cc7c7-127">-WorkspaceName</span></span>
<span data-ttu-id="cc7c7-128">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc7c7-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cc7c7-129">-WorkspaceObject</span></span>
<span data-ttu-id="cc7c7-130">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7c7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc7c7-131">-Confirm</span></span>
<span data-ttu-id="cc7c7-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc7c7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc7c7-133">-WhatIf</span></span>
<span data-ttu-id="cc7c7-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc7c7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc7c7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc7c7-136">CommonParameters</span></span>
<span data-ttu-id="cc7c7-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc7c7-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc7c7-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="cc7c7-139">INPUTS</span></span>

### <span data-ttu-id="cc7c7-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc7c7-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cc7c7-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cc7c7-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cc7c7-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc7c7-142">OUTPUTS</span></span>

### <span data-ttu-id="cc7c7-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="cc7c7-143">System.Void</span></span>

## <span data-ttu-id="cc7c7-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="cc7c7-144">NOTES</span></span>

## <span data-ttu-id="cc7c7-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc7c7-145">RELATED LINKS</span></span>
