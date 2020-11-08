---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193122"
---
# <span data-ttu-id="78d13-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="78d13-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="78d13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78d13-102">SYNOPSIS</span></span>
<span data-ttu-id="78d13-103">Aggiorna il runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="78d13-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="78d13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78d13-104">SYNTAX</span></span>

### <span data-ttu-id="78d13-105">InvokeByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78d13-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d13-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78d13-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d13-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78d13-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d13-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78d13-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d13-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78d13-109">DESCRIPTION</span></span>
<span data-ttu-id="78d13-110">Il cmdlet **Invoke-AzSynapseIntegrationRuntimeUpgrade** aggiorna il runtime di integrazione ospitata autonomamente se la nuova versione è disponibile.</span><span class="sxs-lookup"><span data-stu-id="78d13-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="78d13-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78d13-111">EXAMPLES</span></span>

### <span data-ttu-id="78d13-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="78d13-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="78d13-113">Il cmdlet aggiorna il runtime di integrazione ospitale denominato "test-SelfHost-IR" nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="78d13-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="78d13-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78d13-114">PARAMETERS</span></span>

### <span data-ttu-id="78d13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d13-115">-DefaultProfile</span></span>
<span data-ttu-id="78d13-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78d13-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78d13-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78d13-117">-InputObject</span></span>
<span data-ttu-id="78d13-118">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="78d13-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="78d13-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="78d13-119">-Name</span></span>
<span data-ttu-id="78d13-120">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="78d13-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="78d13-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d13-121">-ResourceGroupName</span></span>
<span data-ttu-id="78d13-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="78d13-122">Resource group name.</span></span>

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

### <span data-ttu-id="78d13-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78d13-123">-ResourceId</span></span>
<span data-ttu-id="78d13-124">Identificatore delle risorse del runtime di integrazione delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="78d13-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="78d13-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="78d13-125">-WorkspaceName</span></span>
<span data-ttu-id="78d13-126">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="78d13-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="78d13-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="78d13-127">-WorkspaceObject</span></span>
<span data-ttu-id="78d13-128">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="78d13-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="78d13-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="78d13-129">-Confirm</span></span>
<span data-ttu-id="78d13-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d13-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d13-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d13-131">-WhatIf</span></span>
<span data-ttu-id="78d13-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78d13-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d13-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78d13-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d13-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d13-134">CommonParameters</span></span>
<span data-ttu-id="78d13-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d13-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d13-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78d13-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d13-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78d13-137">INPUTS</span></span>

### <span data-ttu-id="78d13-138">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="78d13-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="78d13-139">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="78d13-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="78d13-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78d13-140">OUTPUTS</span></span>

### <span data-ttu-id="78d13-141">System. void</span><span class="sxs-lookup"><span data-stu-id="78d13-141">System.Void</span></span>

## <span data-ttu-id="78d13-142">Note</span><span class="sxs-lookup"><span data-stu-id="78d13-142">NOTES</span></span>

## <span data-ttu-id="78d13-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78d13-143">RELATED LINKS</span></span>