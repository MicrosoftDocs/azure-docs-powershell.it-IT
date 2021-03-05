---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9b4e55f701b956fc653cf08cddb87997a998315e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987473"
---
# <span data-ttu-id="07155-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="07155-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="07155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07155-102">SYNOPSIS</span></span>
<span data-ttu-id="07155-103">Rimuove le impostazioni di Protezione avanzata dalle minacce da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="07155-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="07155-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07155-104">SYNTAX</span></span>

### <span data-ttu-id="07155-105">ClearByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07155-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07155-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07155-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07155-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07155-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07155-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="07155-108">DESCRIPTION</span></span>
<span data-ttu-id="07155-109">Il cmdlet **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** rimuove le impostazioni di Protezione avanzata dalle minacce da un'area di lavoro analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="07155-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="07155-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07155-110">EXAMPLES</span></span>

### <span data-ttu-id="07155-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07155-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="07155-112">Questo comando rimuove le impostazioni di protezione avanzata dalle minacce da un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="07155-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="07155-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07155-113">PARAMETERS</span></span>

### <span data-ttu-id="07155-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07155-114">-AsJob</span></span>
<span data-ttu-id="07155-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="07155-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07155-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07155-116">-DefaultProfile</span></span>
<span data-ttu-id="07155-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07155-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07155-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07155-118">-InputObject</span></span>
<span data-ttu-id="07155-119">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="07155-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="07155-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07155-120">-PassThru</span></span>
<span data-ttu-id="07155-121">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="07155-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="07155-122">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="07155-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="07155-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07155-123">-ResourceGroupName</span></span>
<span data-ttu-id="07155-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="07155-124">Resource group name.</span></span>

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

### <span data-ttu-id="07155-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07155-125">-ResourceId</span></span>
<span data-ttu-id="07155-126">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="07155-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="07155-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="07155-127">-WorkspaceName</span></span>
<span data-ttu-id="07155-128">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="07155-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="07155-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07155-129">-Confirm</span></span>
<span data-ttu-id="07155-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07155-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07155-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07155-131">-WhatIf</span></span>
<span data-ttu-id="07155-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07155-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07155-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07155-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07155-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07155-134">CommonParameters</span></span>
<span data-ttu-id="07155-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07155-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07155-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="07155-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07155-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="07155-137">INPUTS</span></span>

### <span data-ttu-id="07155-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="07155-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="07155-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07155-139">OUTPUTS</span></span>

### <span data-ttu-id="07155-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07155-140">System.Boolean</span></span>

## <span data-ttu-id="07155-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="07155-141">NOTES</span></span>

## <span data-ttu-id="07155-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07155-142">RELATED LINKS</span></span>
