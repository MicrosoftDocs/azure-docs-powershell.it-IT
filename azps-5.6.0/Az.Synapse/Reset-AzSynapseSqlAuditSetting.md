---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: 00d9682eb6562cfbfb9d06a4c8a6bac3b149cea1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973709"
---
# <span data-ttu-id="58f75-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="58f75-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="58f75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58f75-102">SYNOPSIS</span></span>
<span data-ttu-id="58f75-103">Rimuove le impostazioni di controllo di un'area di lavoro analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="58f75-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="58f75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58f75-104">SYNTAX</span></span>

### <span data-ttu-id="58f75-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58f75-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f75-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58f75-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f75-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58f75-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58f75-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="58f75-108">DESCRIPTION</span></span>
<span data-ttu-id="58f75-109">Il cmdlet **Reset-AzSynapseSqlAuditSetting** rimuove le impostazioni di controllo di un'area di lavoro analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="58f75-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="58f75-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58f75-110">EXAMPLES</span></span>

### <span data-ttu-id="58f75-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58f75-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="58f75-112">Questo comando rimuove le impostazioni di controllo di un'area di lavoro di Azure Synapse Analytics denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="58f75-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="58f75-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="58f75-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="58f75-114">Questo comando rimuove le impostazioni di controllo di un'area di lavoro di analisi di Azure Synapse denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="58f75-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="58f75-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58f75-115">PARAMETERS</span></span>

### <span data-ttu-id="58f75-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58f75-116">-AsJob</span></span>
<span data-ttu-id="58f75-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="58f75-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58f75-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f75-118">-DefaultProfile</span></span>
<span data-ttu-id="58f75-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58f75-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58f75-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58f75-120">-InputObject</span></span>
<span data-ttu-id="58f75-121">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="58f75-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58f75-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58f75-122">-PassThru</span></span>
<span data-ttu-id="58f75-123">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="58f75-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="58f75-124">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="58f75-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="58f75-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58f75-125">-ResourceGroupName</span></span>
<span data-ttu-id="58f75-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58f75-126">Resource group name.</span></span>

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

### <span data-ttu-id="58f75-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58f75-127">-ResourceId</span></span>
<span data-ttu-id="58f75-128">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="58f75-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="58f75-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="58f75-129">-WorkspaceName</span></span>
<span data-ttu-id="58f75-130">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="58f75-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="58f75-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58f75-131">-Confirm</span></span>
<span data-ttu-id="58f75-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58f75-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58f75-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58f75-133">-WhatIf</span></span>
<span data-ttu-id="58f75-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58f75-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58f75-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58f75-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58f75-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f75-136">CommonParameters</span></span>
<span data-ttu-id="58f75-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58f75-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f75-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="58f75-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f75-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="58f75-139">INPUTS</span></span>

### <span data-ttu-id="58f75-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="58f75-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="58f75-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58f75-141">OUTPUTS</span></span>

### <span data-ttu-id="58f75-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58f75-142">System.Boolean</span></span>

## <span data-ttu-id="58f75-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="58f75-143">NOTES</span></span>

## <span data-ttu-id="58f75-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58f75-144">RELATED LINKS</span></span>
