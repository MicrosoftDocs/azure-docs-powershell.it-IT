---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 77299e9424f0a194776b1114146b76ef2be3329f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383274"
---
# <span data-ttu-id="32180-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="32180-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="32180-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32180-102">SYNOPSIS</span></span>
<span data-ttu-id="32180-103">Rimuove le impostazioni di controllo di un pool SQL di analisi di una sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="32180-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="32180-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32180-104">SYNTAX</span></span>

### <span data-ttu-id="32180-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32180-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32180-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32180-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32180-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32180-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32180-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32180-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32180-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32180-109">DESCRIPTION</span></span>
<span data-ttu-id="32180-110">Il cmdlet **Reset-AzSynapseSqlPoolAuditSetting** rimuove le impostazioni di controllo di un pool SQL di analisi di una sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="32180-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="32180-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32180-111">EXAMPLES</span></span>

### <span data-ttu-id="32180-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="32180-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="32180-113">Questo comando rimuove le impostazioni di controllo di un pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="32180-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="32180-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="32180-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="32180-115">Questo comando rimuove le impostazioni di controllo di un pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="32180-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="32180-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32180-116">PARAMETERS</span></span>

### <span data-ttu-id="32180-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32180-117">-AsJob</span></span>
<span data-ttu-id="32180-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="32180-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32180-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32180-119">-DefaultProfile</span></span>
<span data-ttu-id="32180-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32180-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32180-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32180-121">-InputObject</span></span>
<span data-ttu-id="32180-122">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="32180-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32180-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="32180-123">-Name</span></span>
<span data-ttu-id="32180-124">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="32180-124">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32180-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32180-125">-PassThru</span></span>
<span data-ttu-id="32180-126">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="32180-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="32180-127">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="32180-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="32180-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32180-128">-ResourceGroupName</span></span>
<span data-ttu-id="32180-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="32180-129">Resource group name.</span></span>

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

### <span data-ttu-id="32180-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32180-130">-ResourceId</span></span>
<span data-ttu-id="32180-131">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="32180-131">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="32180-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="32180-132">-WorkspaceName</span></span>
<span data-ttu-id="32180-133">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="32180-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="32180-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="32180-134">-WorkspaceObject</span></span>
<span data-ttu-id="32180-135">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="32180-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32180-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32180-136">-Confirm</span></span>
<span data-ttu-id="32180-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32180-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32180-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32180-138">-WhatIf</span></span>
<span data-ttu-id="32180-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32180-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32180-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32180-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32180-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32180-141">CommonParameters</span></span>
<span data-ttu-id="32180-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32180-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32180-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32180-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32180-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32180-144">INPUTS</span></span>

### <span data-ttu-id="32180-145">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="32180-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="32180-146">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="32180-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="32180-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32180-147">OUTPUTS</span></span>

### <span data-ttu-id="32180-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32180-148">System.Boolean</span></span>

## <span data-ttu-id="32180-149">Note</span><span class="sxs-lookup"><span data-stu-id="32180-149">NOTES</span></span>

## <span data-ttu-id="32180-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32180-150">RELATED LINKS</span></span>
