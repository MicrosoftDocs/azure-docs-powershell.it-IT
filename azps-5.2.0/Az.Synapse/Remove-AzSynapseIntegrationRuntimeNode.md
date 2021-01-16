---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362890"
---
# <span data-ttu-id="ebad3-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ebad3-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="ebad3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ebad3-102">SYNOPSIS</span></span>
<span data-ttu-id="ebad3-103">Rimuovere un nodo con il nome indicato in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ebad3-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="ebad3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ebad3-104">SYNTAX</span></span>

### <span data-ttu-id="ebad3-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ebad3-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebad3-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebad3-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebad3-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebad3-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebad3-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebad3-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebad3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebad3-109">DESCRIPTION</span></span>
<span data-ttu-id="ebad3-110">Il cmdlet **Remove-AzSynapseIntegrationRuntimeNode** rimuove un nodo in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ebad3-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="ebad3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ebad3-111">EXAMPLES</span></span>

### <span data-ttu-id="ebad3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ebad3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="ebad3-113">Rimuovere un nodo con il nome indicato in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ebad3-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="ebad3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ebad3-114">PARAMETERS</span></span>

### <span data-ttu-id="ebad3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebad3-115">-DefaultProfile</span></span>
<span data-ttu-id="ebad3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ebad3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebad3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ebad3-117">-Force</span></span>
<span data-ttu-id="ebad3-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ebad3-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ebad3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebad3-119">-InputObject</span></span>
<span data-ttu-id="ebad3-120">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="ebad3-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="ebad3-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ebad3-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ebad3-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ebad3-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="ebad3-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="ebad3-123">-NodeName</span></span>
<span data-ttu-id="ebad3-124">Nome del nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="ebad3-124">The integration runtime node name.</span></span>

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

### <span data-ttu-id="ebad3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebad3-125">-ResourceGroupName</span></span>
<span data-ttu-id="ebad3-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ebad3-126">Resource group name.</span></span>

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

### <span data-ttu-id="ebad3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebad3-127">-ResourceId</span></span>
<span data-ttu-id="ebad3-128">Identificatore delle risorse del runtime di integrazione delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="ebad3-128">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="ebad3-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ebad3-129">-WorkspaceName</span></span>
<span data-ttu-id="ebad3-130">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="ebad3-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ebad3-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ebad3-131">-WorkspaceObject</span></span>
<span data-ttu-id="ebad3-132">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="ebad3-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ebad3-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ebad3-133">-Confirm</span></span>
<span data-ttu-id="ebad3-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebad3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebad3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebad3-135">-WhatIf</span></span>
<span data-ttu-id="ebad3-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebad3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebad3-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebad3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebad3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebad3-138">CommonParameters</span></span>
<span data-ttu-id="ebad3-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebad3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebad3-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebad3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebad3-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ebad3-141">INPUTS</span></span>

### <span data-ttu-id="ebad3-142">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ebad3-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ebad3-143">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ebad3-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="ebad3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ebad3-144">System.String</span></span>

## <span data-ttu-id="ebad3-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ebad3-145">OUTPUTS</span></span>

### <span data-ttu-id="ebad3-146">System. void</span><span class="sxs-lookup"><span data-stu-id="ebad3-146">System.Void</span></span>

## <span data-ttu-id="ebad3-147">Note</span><span class="sxs-lookup"><span data-stu-id="ebad3-147">NOTES</span></span>

## <span data-ttu-id="ebad3-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ebad3-148">RELATED LINKS</span></span>
