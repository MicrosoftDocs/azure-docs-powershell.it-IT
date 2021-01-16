---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: ea27b23174d9555e4153dc5ef8c4d053ef5a49b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368941"
---
# <span data-ttu-id="08060-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="08060-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="08060-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08060-102">SYNOPSIS</span></span>
<span data-ttu-id="08060-103">Riprende un pool SQL di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="08060-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="08060-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08060-104">SYNTAX</span></span>

### <span data-ttu-id="08060-105">ResumeByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08060-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08060-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08060-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08060-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08060-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08060-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08060-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08060-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08060-109">DESCRIPTION</span></span>
<span data-ttu-id="08060-110">Il cmdlet **Resume-AzSynapseSqlPool** riprende un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="08060-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="08060-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08060-111">EXAMPLES</span></span>

### <span data-ttu-id="08060-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08060-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="08060-113">Questo comando riprende un pool SQL di analisi delle sinapsi di Azure sospese.</span><span class="sxs-lookup"><span data-stu-id="08060-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="08060-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08060-114">PARAMETERS</span></span>

### <span data-ttu-id="08060-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08060-115">-AsJob</span></span>
<span data-ttu-id="08060-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="08060-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08060-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08060-117">-DefaultProfile</span></span>
<span data-ttu-id="08060-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08060-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08060-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08060-119">-InputObject</span></span>
<span data-ttu-id="08060-120">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="08060-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08060-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="08060-121">-Name</span></span>
<span data-ttu-id="08060-122">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="08060-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08060-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08060-123">-PassThru</span></span>
<span data-ttu-id="08060-124">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="08060-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="08060-125">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="08060-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="08060-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08060-126">-ResourceGroupName</span></span>
<span data-ttu-id="08060-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="08060-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08060-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08060-128">-ResourceId</span></span>
<span data-ttu-id="08060-129">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="08060-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08060-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="08060-130">-WorkspaceName</span></span>
<span data-ttu-id="08060-131">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="08060-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08060-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="08060-132">-WorkspaceObject</span></span>
<span data-ttu-id="08060-133">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="08060-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08060-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="08060-134">-Confirm</span></span>
<span data-ttu-id="08060-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08060-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08060-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08060-136">-WhatIf</span></span>
<span data-ttu-id="08060-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08060-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08060-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08060-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08060-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08060-139">CommonParameters</span></span>
<span data-ttu-id="08060-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08060-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08060-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08060-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08060-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08060-142">INPUTS</span></span>

### <span data-ttu-id="08060-143">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="08060-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="08060-144">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="08060-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="08060-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08060-145">OUTPUTS</span></span>

### <span data-ttu-id="08060-146">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="08060-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="08060-147">Note</span><span class="sxs-lookup"><span data-stu-id="08060-147">NOTES</span></span>

## <span data-ttu-id="08060-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08060-148">RELATED LINKS</span></span>
