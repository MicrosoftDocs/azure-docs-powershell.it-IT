---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193118"
---
# <span data-ttu-id="8a046-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="8a046-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="8a046-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a046-102">SYNOPSIS</span></span>
<span data-ttu-id="8a046-103">Sincronizza le credenziali tra i nodi di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="8a046-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="8a046-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a046-104">SYNTAX</span></span>

### <span data-ttu-id="8a046-105">StopByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a046-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a046-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a046-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a046-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a046-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a046-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a046-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a046-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a046-109">DESCRIPTION</span></span>
<span data-ttu-id="8a046-110">Il cmdlet **Sync-AzSynapseIntegrationRuntimeCredential** sincronizza le credenziali locali tra i nodi di Integration Runtime, che obbligano le credenziali a essere identiche in tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="8a046-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="8a046-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a046-111">EXAMPLES</span></span>

### <span data-ttu-id="8a046-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8a046-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="8a046-113">Sincronizza le credenziali tra i nodi di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="8a046-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="8a046-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a046-114">PARAMETERS</span></span>

### <span data-ttu-id="8a046-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a046-115">-DefaultProfile</span></span>
<span data-ttu-id="8a046-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a046-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a046-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8a046-117">-Force</span></span>
<span data-ttu-id="8a046-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8a046-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8a046-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a046-119">-InputObject</span></span>
<span data-ttu-id="8a046-120">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="8a046-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="8a046-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="8a046-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="8a046-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8a046-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="8a046-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a046-123">-ResourceGroupName</span></span>
<span data-ttu-id="8a046-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8a046-124">Resource group name.</span></span>

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

### <span data-ttu-id="8a046-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a046-125">-ResourceId</span></span>
<span data-ttu-id="8a046-126">Identificatore delle risorse del runtime di integrazione delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="8a046-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="8a046-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8a046-127">-WorkspaceName</span></span>
<span data-ttu-id="8a046-128">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="8a046-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8a046-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8a046-129">-WorkspaceObject</span></span>
<span data-ttu-id="8a046-130">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="8a046-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8a046-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a046-131">-Confirm</span></span>
<span data-ttu-id="8a046-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a046-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a046-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a046-133">-WhatIf</span></span>
<span data-ttu-id="8a046-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a046-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a046-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a046-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a046-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a046-136">CommonParameters</span></span>
<span data-ttu-id="8a046-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a046-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a046-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a046-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a046-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a046-139">INPUTS</span></span>

### <span data-ttu-id="8a046-140">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8a046-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8a046-141">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8a046-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8a046-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a046-142">OUTPUTS</span></span>

### <span data-ttu-id="8a046-143">System. void</span><span class="sxs-lookup"><span data-stu-id="8a046-143">System.Void</span></span>

## <span data-ttu-id="8a046-144">Note</span><span class="sxs-lookup"><span data-stu-id="8a046-144">NOTES</span></span>

## <span data-ttu-id="8a046-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a046-145">RELATED LINKS</span></span>