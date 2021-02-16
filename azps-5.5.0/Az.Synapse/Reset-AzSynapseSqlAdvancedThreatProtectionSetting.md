---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209003"
---
# <span data-ttu-id="48e65-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="48e65-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="48e65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48e65-102">SYNOPSIS</span></span>
<span data-ttu-id="48e65-103">Rimuove le impostazioni di Protezione avanzata dalle minacce da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="48e65-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="48e65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48e65-104">SYNTAX</span></span>

### <span data-ttu-id="48e65-105">ClearByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48e65-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48e65-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48e65-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48e65-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48e65-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48e65-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="48e65-108">DESCRIPTION</span></span>
<span data-ttu-id="48e65-109">Il cmdlet **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** rimuove le impostazioni di Protezione avanzata dalle minacce da un'area di lavoro analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="48e65-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="48e65-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48e65-110">EXAMPLES</span></span>

### <span data-ttu-id="48e65-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48e65-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="48e65-112">Questo comando rimuove le impostazioni di protezione avanzata dalle minacce da un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="48e65-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="48e65-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48e65-113">PARAMETERS</span></span>

### <span data-ttu-id="48e65-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48e65-114">-AsJob</span></span>
<span data-ttu-id="48e65-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="48e65-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48e65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48e65-116">-DefaultProfile</span></span>
<span data-ttu-id="48e65-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48e65-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48e65-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48e65-118">-InputObject</span></span>
<span data-ttu-id="48e65-119">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="48e65-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48e65-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48e65-120">-PassThru</span></span>
<span data-ttu-id="48e65-121">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="48e65-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="48e65-122">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="48e65-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="48e65-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48e65-123">-ResourceGroupName</span></span>
<span data-ttu-id="48e65-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="48e65-124">Resource group name.</span></span>

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

### <span data-ttu-id="48e65-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48e65-125">-ResourceId</span></span>
<span data-ttu-id="48e65-126">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="48e65-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="48e65-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="48e65-127">-WorkspaceName</span></span>
<span data-ttu-id="48e65-128">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="48e65-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="48e65-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48e65-129">-Confirm</span></span>
<span data-ttu-id="48e65-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48e65-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48e65-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48e65-131">-WhatIf</span></span>
<span data-ttu-id="48e65-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48e65-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48e65-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48e65-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48e65-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e65-134">CommonParameters</span></span>
<span data-ttu-id="48e65-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48e65-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e65-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48e65-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e65-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="48e65-137">INPUTS</span></span>

### <span data-ttu-id="48e65-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="48e65-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="48e65-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48e65-139">OUTPUTS</span></span>

### <span data-ttu-id="48e65-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48e65-140">System.Boolean</span></span>

## <span data-ttu-id="48e65-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="48e65-141">NOTES</span></span>

## <span data-ttu-id="48e65-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48e65-142">RELATED LINKS</span></span>
