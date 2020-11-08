---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201376"
---
# <span data-ttu-id="2c501-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2c501-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="2c501-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c501-102">SYNOPSIS</span></span>
<span data-ttu-id="2c501-103">Rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2c501-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="2c501-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c501-104">SYNTAX</span></span>

### <span data-ttu-id="2c501-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2c501-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c501-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c501-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c501-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c501-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c501-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c501-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c501-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c501-109">DESCRIPTION</span></span>
<span data-ttu-id="2c501-110">Il cmdlet **Remove-AzSynapseIntegrationRuntime** rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2c501-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="2c501-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c501-111">EXAMPLES</span></span>

### <span data-ttu-id="2c501-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2c501-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="2c501-113">Questo comando rimuove il runtime di integrazione denominato "test-reserved-IR" dall'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2c501-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="2c501-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c501-114">PARAMETERS</span></span>

### <span data-ttu-id="2c501-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c501-115">-DefaultProfile</span></span>
<span data-ttu-id="2c501-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c501-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c501-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2c501-117">-Force</span></span>
<span data-ttu-id="2c501-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2c501-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2c501-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c501-119">-InputObject</span></span>
<span data-ttu-id="2c501-120">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="2c501-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="2c501-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c501-121">-Name</span></span>
<span data-ttu-id="2c501-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2c501-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="2c501-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c501-123">-ResourceGroupName</span></span>
<span data-ttu-id="2c501-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2c501-124">Resource group name.</span></span>

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

### <span data-ttu-id="2c501-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c501-125">-ResourceId</span></span>
<span data-ttu-id="2c501-126">Identificatore delle risorse del runtime di integrazione delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="2c501-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="2c501-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2c501-127">-WorkspaceName</span></span>
<span data-ttu-id="2c501-128">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="2c501-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2c501-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2c501-129">-WorkspaceObject</span></span>
<span data-ttu-id="2c501-130">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="2c501-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2c501-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2c501-131">-Confirm</span></span>
<span data-ttu-id="2c501-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c501-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c501-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c501-133">-WhatIf</span></span>
<span data-ttu-id="2c501-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c501-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c501-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c501-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c501-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c501-136">CommonParameters</span></span>
<span data-ttu-id="2c501-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c501-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c501-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c501-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c501-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c501-139">INPUTS</span></span>

### <span data-ttu-id="2c501-140">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2c501-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2c501-141">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2c501-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2c501-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c501-142">OUTPUTS</span></span>

### <span data-ttu-id="2c501-143">System. void</span><span class="sxs-lookup"><span data-stu-id="2c501-143">System.Void</span></span>

## <span data-ttu-id="2c501-144">Note</span><span class="sxs-lookup"><span data-stu-id="2c501-144">NOTES</span></span>

## <span data-ttu-id="2c501-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c501-145">RELATED LINKS</span></span>
