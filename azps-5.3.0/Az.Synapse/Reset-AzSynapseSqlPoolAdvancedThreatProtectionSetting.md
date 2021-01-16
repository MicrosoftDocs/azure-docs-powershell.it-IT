---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c5f1c3f2d1a23a06286cdbf7fb54915d33b1e3d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476600"
---
# <span data-ttu-id="4b25a-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="4b25a-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="4b25a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b25a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b25a-103">Rimuove le impostazioni avanzate di protezione dalle minacce da un pool SQL.</span><span class="sxs-lookup"><span data-stu-id="4b25a-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="4b25a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b25a-104">SYNTAX</span></span>

### <span data-ttu-id="4b25a-105">ClearByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4b25a-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b25a-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b25a-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b25a-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b25a-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b25a-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b25a-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b25a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b25a-109">DESCRIPTION</span></span>
<span data-ttu-id="4b25a-110">Il cmdlet **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** consente di rimuovere le impostazioni avanzate di protezione dalle minacce da un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b25a-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4b25a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b25a-111">EXAMPLES</span></span>

### <span data-ttu-id="4b25a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b25a-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="4b25a-113">Questo comando rimuove le impostazioni avanzate di protezione dalle minacce da un pool SQL denominato ContosoSqlPool sotto l'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4b25a-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="4b25a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b25a-114">PARAMETERS</span></span>

### <span data-ttu-id="4b25a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b25a-115">-AsJob</span></span>
<span data-ttu-id="4b25a-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4b25a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b25a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b25a-117">-DefaultProfile</span></span>
<span data-ttu-id="4b25a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b25a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b25a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b25a-119">-InputObject</span></span>
<span data-ttu-id="4b25a-120">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="4b25a-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b25a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b25a-121">-Name</span></span>
<span data-ttu-id="4b25a-122">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="4b25a-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet, ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b25a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b25a-123">-PassThru</span></span>
<span data-ttu-id="4b25a-124">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4b25a-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4b25a-125">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="4b25a-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4b25a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b25a-126">-ResourceGroupName</span></span>
<span data-ttu-id="4b25a-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b25a-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b25a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b25a-128">-ResourceId</span></span>
<span data-ttu-id="4b25a-129">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="4b25a-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b25a-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4b25a-130">-WorkspaceName</span></span>
<span data-ttu-id="4b25a-131">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="4b25a-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b25a-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4b25a-132">-WorkspaceObject</span></span>
<span data-ttu-id="4b25a-133">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="4b25a-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b25a-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b25a-134">-Confirm</span></span>
<span data-ttu-id="4b25a-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b25a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b25a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b25a-136">-WhatIf</span></span>
<span data-ttu-id="4b25a-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b25a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b25a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b25a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b25a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b25a-139">CommonParameters</span></span>
<span data-ttu-id="4b25a-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b25a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b25a-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b25a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b25a-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b25a-142">INPUTS</span></span>

### <span data-ttu-id="4b25a-143">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4b25a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4b25a-144">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4b25a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4b25a-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b25a-145">OUTPUTS</span></span>

### <span data-ttu-id="4b25a-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b25a-146">System.Boolean</span></span>

## <span data-ttu-id="4b25a-147">Note</span><span class="sxs-lookup"><span data-stu-id="4b25a-147">NOTES</span></span>

## <span data-ttu-id="4b25a-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b25a-148">RELATED LINKS</span></span>
