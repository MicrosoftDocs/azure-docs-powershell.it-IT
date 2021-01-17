---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334696"
---
# <span data-ttu-id="a1acd-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a1acd-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="a1acd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1acd-102">SYNOPSIS</span></span>
<span data-ttu-id="a1acd-103">Rimuove le impostazioni avanzate di protezione dalle minacce da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a1acd-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="a1acd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1acd-104">SYNTAX</span></span>

### <span data-ttu-id="a1acd-105">ClearByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1acd-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1acd-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1acd-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1acd-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1acd-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1acd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1acd-108">DESCRIPTION</span></span>
<span data-ttu-id="a1acd-109">Il cmdlet **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** rimuove le impostazioni avanzate di protezione dalle minacce da un'area di lavoro di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a1acd-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a1acd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1acd-110">EXAMPLES</span></span>

### <span data-ttu-id="a1acd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1acd-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a1acd-112">Questo comando rimuove le impostazioni avanzate di protezione dalle minacce da un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a1acd-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a1acd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1acd-113">PARAMETERS</span></span>

### <span data-ttu-id="a1acd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1acd-114">-AsJob</span></span>
<span data-ttu-id="a1acd-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a1acd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1acd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1acd-116">-DefaultProfile</span></span>
<span data-ttu-id="a1acd-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1acd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1acd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1acd-118">-InputObject</span></span>
<span data-ttu-id="a1acd-119">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1acd-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a1acd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1acd-120">-PassThru</span></span>
<span data-ttu-id="a1acd-121">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a1acd-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a1acd-122">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="a1acd-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a1acd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1acd-123">-ResourceGroupName</span></span>
<span data-ttu-id="a1acd-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1acd-124">Resource group name.</span></span>

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

### <span data-ttu-id="a1acd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1acd-125">-ResourceId</span></span>
<span data-ttu-id="a1acd-126">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a1acd-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="a1acd-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a1acd-127">-WorkspaceName</span></span>
<span data-ttu-id="a1acd-128">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a1acd-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a1acd-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1acd-129">-Confirm</span></span>
<span data-ttu-id="a1acd-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1acd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1acd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1acd-131">-WhatIf</span></span>
<span data-ttu-id="a1acd-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1acd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1acd-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1acd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1acd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1acd-134">CommonParameters</span></span>
<span data-ttu-id="a1acd-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1acd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1acd-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1acd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1acd-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1acd-137">INPUTS</span></span>

### <span data-ttu-id="a1acd-138">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a1acd-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a1acd-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1acd-139">OUTPUTS</span></span>

### <span data-ttu-id="a1acd-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1acd-140">System.Boolean</span></span>

## <span data-ttu-id="a1acd-141">Note</span><span class="sxs-lookup"><span data-stu-id="a1acd-141">NOTES</span></span>

## <span data-ttu-id="a1acd-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1acd-142">RELATED LINKS</span></span>
