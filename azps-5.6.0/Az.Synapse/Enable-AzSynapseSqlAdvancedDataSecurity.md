---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 2b937f147eebecd8a2aac7e2a70de1af4aa20c4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981870"
---
# <span data-ttu-id="6879e-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="6879e-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="6879e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6879e-102">SYNOPSIS</span></span>
<span data-ttu-id="6879e-103">Abilita Advanced Data Security in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6879e-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="6879e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6879e-104">SYNTAX</span></span>

### <span data-ttu-id="6879e-105">EnableByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6879e-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6879e-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6879e-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6879e-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6879e-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6879e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6879e-108">DESCRIPTION</span></span>
<span data-ttu-id="6879e-109">Il cmdlet **Enable-AzSynapseSqlAdvancedDataSecurity** abilita Advanced Data Security in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6879e-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="6879e-110">Advanced Data Security è un pacchetto di sicurezza unificato che include la classificazione dei dati, la valutazione delle vulnerabilità e Advanced Threat Protection per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6879e-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="6879e-111">Verrà creato automaticamente un nuovo account di archiviazione per il salvataggio delle valutazioni di vulnerabilità.</span><span class="sxs-lookup"><span data-stu-id="6879e-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="6879e-112">Se un account di archiviazione è stato creato in precedenza per questo scopo, verrà usato al suo posto)</span><span class="sxs-lookup"><span data-stu-id="6879e-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="6879e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6879e-113">EXAMPLES</span></span>

### <span data-ttu-id="6879e-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6879e-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="6879e-115">Questo comando abilita l'area di lavoro Advanced Data Security.</span><span class="sxs-lookup"><span data-stu-id="6879e-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="6879e-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6879e-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="6879e-117">Questo comando abilita l'area di lavoro Advanced Data Security tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="6879e-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="6879e-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6879e-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="6879e-119">Questo comando abilita l'area di lavoro Advanced Data Security tramite pipeline e non abilita automaticamente la valutazione delle vulnerabilità.</span><span class="sxs-lookup"><span data-stu-id="6879e-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="6879e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6879e-120">PARAMETERS</span></span>

### <span data-ttu-id="6879e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6879e-121">-AsJob</span></span>
<span data-ttu-id="6879e-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6879e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6879e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6879e-123">-DefaultProfile</span></span>
<span data-ttu-id="6879e-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6879e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6879e-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="6879e-125">-DeploymentName</span></span>
<span data-ttu-id="6879e-126">Specificare un nome personalizzato per la distribuzione di Advanced Data Security.</span><span class="sxs-lookup"><span data-stu-id="6879e-126">Supply a custom name for Advanced Data Security deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6879e-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="6879e-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="6879e-128">Non abilitare automaticamente la valutazione della vulnerabilità (non verrà creato un account di archiviazione).</span><span class="sxs-lookup"><span data-stu-id="6879e-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="6879e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6879e-129">-InputObject</span></span>
<span data-ttu-id="6879e-130">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="6879e-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: EnableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6879e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6879e-131">-ResourceGroupName</span></span>
<span data-ttu-id="6879e-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6879e-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6879e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6879e-133">-ResourceId</span></span>
<span data-ttu-id="6879e-134">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="6879e-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6879e-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6879e-135">-WorkspaceName</span></span>
<span data-ttu-id="6879e-136">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="6879e-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6879e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6879e-137">-Confirm</span></span>
<span data-ttu-id="6879e-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6879e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6879e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6879e-139">-WhatIf</span></span>
<span data-ttu-id="6879e-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6879e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6879e-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6879e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6879e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6879e-142">CommonParameters</span></span>
<span data-ttu-id="6879e-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6879e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6879e-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6879e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6879e-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="6879e-145">INPUTS</span></span>

### <span data-ttu-id="6879e-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6879e-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6879e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6879e-147">OUTPUTS</span></span>

### <span data-ttu-id="6879e-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="6879e-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="6879e-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="6879e-149">NOTES</span></span>

## <span data-ttu-id="6879e-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6879e-150">RELATED LINKS</span></span>
