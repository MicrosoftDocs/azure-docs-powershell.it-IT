---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193104"
---
# <span data-ttu-id="909ef-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="909ef-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="909ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="909ef-102">SYNOPSIS</span></span>
<span data-ttu-id="909ef-103">Aggiorna un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="909ef-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="909ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="909ef-104">SYNTAX</span></span>

### <span data-ttu-id="909ef-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="909ef-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="909ef-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="909ef-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="909ef-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="909ef-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="909ef-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="909ef-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="909ef-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="909ef-109">DESCRIPTION</span></span>
<span data-ttu-id="909ef-110">Il cmdlet **Update-AzSynapseIntegrationRuntime** aggiorna le proprietà di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="909ef-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="909ef-111">Attualmente il cmdlet supporta solo l'aggiornamento di "AutoUpdate" e "AutoUpdateDelayOffset" per l'integrazione autonoma di Runtime.</span><span class="sxs-lookup"><span data-stu-id="909ef-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="909ef-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="909ef-112">EXAMPLES</span></span>

### <span data-ttu-id="909ef-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="909ef-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="909ef-114">Il cmdlet aggiorna l'integrazione di runtime indipendente denominata "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="909ef-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="909ef-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="909ef-115">PARAMETERS</span></span>

### <span data-ttu-id="909ef-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="909ef-116">-AutoUpdate</span></span>
<span data-ttu-id="909ef-117">Abilitare o disabilitare l'aggiornamento automatico di runtime self-hosted Integration.</span><span class="sxs-lookup"><span data-stu-id="909ef-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909ef-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="909ef-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="909ef-119">L'ora del giorno per l'aggiornamento automatico di runtime self-hosted Integration.</span><span class="sxs-lookup"><span data-stu-id="909ef-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909ef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="909ef-120">-DefaultProfile</span></span>
<span data-ttu-id="909ef-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="909ef-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="909ef-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="909ef-122">-InputObject</span></span>
<span data-ttu-id="909ef-123">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="909ef-123">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="909ef-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="909ef-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="909ef-125">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="909ef-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909ef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="909ef-126">-ResourceGroupName</span></span>
<span data-ttu-id="909ef-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="909ef-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909ef-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="909ef-128">-ResourceId</span></span>
<span data-ttu-id="909ef-129">Identificatore delle risorse del runtime di integrazione delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="909ef-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909ef-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="909ef-130">-WorkspaceName</span></span>
<span data-ttu-id="909ef-131">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="909ef-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909ef-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="909ef-132">-WorkspaceObject</span></span>
<span data-ttu-id="909ef-133">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="909ef-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="909ef-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="909ef-134">-Confirm</span></span>
<span data-ttu-id="909ef-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="909ef-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="909ef-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="909ef-136">-WhatIf</span></span>
<span data-ttu-id="909ef-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="909ef-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="909ef-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="909ef-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="909ef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="909ef-139">CommonParameters</span></span>
<span data-ttu-id="909ef-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="909ef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="909ef-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="909ef-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="909ef-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="909ef-142">INPUTS</span></span>

### <span data-ttu-id="909ef-143">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="909ef-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="909ef-144">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="909ef-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="909ef-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="909ef-145">OUTPUTS</span></span>

### <span data-ttu-id="909ef-146">Microsoft. Azure. Commands. sinapsi. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="909ef-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="909ef-147">Note</span><span class="sxs-lookup"><span data-stu-id="909ef-147">NOTES</span></span>

## <span data-ttu-id="909ef-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="909ef-148">RELATED LINKS</span></span>
