---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: b25ca2a026cf5d82aa25f69868ca8605fd75bced
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383263"
---
# <span data-ttu-id="35937-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="35937-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="35937-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35937-102">SYNOPSIS</span></span>
<span data-ttu-id="35937-103">Rimuove le impostazioni di controllo di un'area di lavoro di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="35937-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="35937-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35937-104">SYNTAX</span></span>

### <span data-ttu-id="35937-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35937-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35937-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35937-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35937-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35937-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35937-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35937-108">DESCRIPTION</span></span>
<span data-ttu-id="35937-109">Il cmdlet **Reset-AzSynapseSqlAuditSetting** rimuove le impostazioni di controllo di un'area di lavoro di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="35937-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="35937-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35937-110">EXAMPLES</span></span>

### <span data-ttu-id="35937-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35937-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="35937-112">Questo comando rimuove le impostazioni di controllo di un'area di lavoro di analisi di Azure sinapsi denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="35937-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="35937-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="35937-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="35937-114">Questo comando rimuove le impostazioni di controllo di un'area di lavoro di analisi di Azure sinapsi denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="35937-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="35937-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35937-115">PARAMETERS</span></span>

### <span data-ttu-id="35937-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35937-116">-AsJob</span></span>
<span data-ttu-id="35937-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="35937-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35937-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35937-118">-DefaultProfile</span></span>
<span data-ttu-id="35937-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35937-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35937-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35937-120">-InputObject</span></span>
<span data-ttu-id="35937-121">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="35937-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="35937-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35937-122">-PassThru</span></span>
<span data-ttu-id="35937-123">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="35937-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="35937-124">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="35937-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="35937-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35937-125">-ResourceGroupName</span></span>
<span data-ttu-id="35937-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="35937-126">Resource group name.</span></span>

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

### <span data-ttu-id="35937-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35937-127">-ResourceId</span></span>
<span data-ttu-id="35937-128">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="35937-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="35937-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="35937-129">-WorkspaceName</span></span>
<span data-ttu-id="35937-130">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="35937-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="35937-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35937-131">-Confirm</span></span>
<span data-ttu-id="35937-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35937-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35937-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35937-133">-WhatIf</span></span>
<span data-ttu-id="35937-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35937-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35937-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35937-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35937-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35937-136">CommonParameters</span></span>
<span data-ttu-id="35937-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35937-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35937-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35937-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35937-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35937-139">INPUTS</span></span>

### <span data-ttu-id="35937-140">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="35937-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="35937-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35937-141">OUTPUTS</span></span>

### <span data-ttu-id="35937-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35937-142">System.Boolean</span></span>

## <span data-ttu-id="35937-143">Note</span><span class="sxs-lookup"><span data-stu-id="35937-143">NOTES</span></span>

## <span data-ttu-id="35937-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35937-144">RELATED LINKS</span></span>
