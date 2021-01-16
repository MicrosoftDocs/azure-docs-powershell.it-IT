---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: dea0770af8cca14ebd523f67b69d7a12931183ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384131"
---
# <span data-ttu-id="5dc73-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="5dc73-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="5dc73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5dc73-102">SYNOPSIS</span></span>
<span data-ttu-id="5dc73-103">Abilita la sicurezza dei dati avanzata in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5dc73-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="5dc73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5dc73-104">SYNTAX</span></span>

### <span data-ttu-id="5dc73-105">EnableByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5dc73-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dc73-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dc73-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dc73-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dc73-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5dc73-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dc73-108">DESCRIPTION</span></span>
<span data-ttu-id="5dc73-109">Il cmdlet **Enable-AzSynapseSqlAdvancedDataSecurity** Abilita la sicurezza dei dati avanzata in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5dc73-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="5dc73-110">Advanced Data Security è un pacchetto di sicurezza unificato che include la classificazione dei dati, la valutazione delle vulnerabilità e la protezione avanzata delle minacce per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5dc73-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="5dc73-111">Verrà creato automaticamente un nuovo account di archiviazione per il salvataggio delle valutazioni della vulnerabilità.</span><span class="sxs-lookup"><span data-stu-id="5dc73-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="5dc73-112">Se un account di archiviazione è stato creato in precedenza per questo scopo, verrà usato al suo posto)</span><span class="sxs-lookup"><span data-stu-id="5dc73-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="5dc73-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5dc73-113">EXAMPLES</span></span>

### <span data-ttu-id="5dc73-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5dc73-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="5dc73-115">Questo comando Abilita la sicurezza dei dati avanzata dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5dc73-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="5dc73-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5dc73-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="5dc73-117">Questo comando consente la sicurezza dei dati avanzata dell'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="5dc73-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="5dc73-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5dc73-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="5dc73-119">Questo comando Abilita la sicurezza dei dati avanzata dell'area di lavoro tramite pipeline e non abilita automaticamente la valutazione della vulnerabilità.</span><span class="sxs-lookup"><span data-stu-id="5dc73-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="5dc73-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5dc73-120">PARAMETERS</span></span>

### <span data-ttu-id="5dc73-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5dc73-121">-AsJob</span></span>
<span data-ttu-id="5dc73-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5dc73-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5dc73-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dc73-123">-DefaultProfile</span></span>
<span data-ttu-id="5dc73-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5dc73-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dc73-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="5dc73-125">-DeploymentName</span></span>
<span data-ttu-id="5dc73-126">Specificare un nome personalizzato per la distribuzione avanzata della sicurezza dei dati.</span><span class="sxs-lookup"><span data-stu-id="5dc73-126">Supply a custom name for Advanced Data Security deployment.</span></span>

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

### <span data-ttu-id="5dc73-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="5dc73-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="5dc73-128">Non abilitare automaticamente la valutazione della vulnerabilità (non verrà creato un account di archiviazione).</span><span class="sxs-lookup"><span data-stu-id="5dc73-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="5dc73-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5dc73-129">-InputObject</span></span>
<span data-ttu-id="5dc73-130">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="5dc73-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5dc73-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dc73-131">-ResourceGroupName</span></span>
<span data-ttu-id="5dc73-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5dc73-132">Resource group name.</span></span>

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

### <span data-ttu-id="5dc73-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5dc73-133">-ResourceId</span></span>
<span data-ttu-id="5dc73-134">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="5dc73-134">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="5dc73-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5dc73-135">-WorkspaceName</span></span>
<span data-ttu-id="5dc73-136">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="5dc73-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5dc73-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5dc73-137">-Confirm</span></span>
<span data-ttu-id="5dc73-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dc73-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dc73-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dc73-139">-WhatIf</span></span>
<span data-ttu-id="5dc73-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5dc73-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dc73-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5dc73-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dc73-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dc73-142">CommonParameters</span></span>
<span data-ttu-id="5dc73-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dc73-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dc73-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dc73-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dc73-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5dc73-145">INPUTS</span></span>

### <span data-ttu-id="5dc73-146">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5dc73-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5dc73-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5dc73-147">OUTPUTS</span></span>

### <span data-ttu-id="5dc73-148">Microsoft. Azure. Commands. sinapsi. Models. WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="5dc73-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="5dc73-149">Note</span><span class="sxs-lookup"><span data-stu-id="5dc73-149">NOTES</span></span>

## <span data-ttu-id="5dc73-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5dc73-150">RELATED LINKS</span></span>
