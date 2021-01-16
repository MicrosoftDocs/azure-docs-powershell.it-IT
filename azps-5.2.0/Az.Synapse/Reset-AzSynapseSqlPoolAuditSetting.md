---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 77299e9424f0a194776b1114146b76ef2be3329f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329053"
---
# <span data-ttu-id="d9f8b-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="d9f8b-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="d9f8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f8b-103">Rimuove le impostazioni di controllo di un pool SQL di analisi di una sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d9f8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9f8b-104">SYNTAX</span></span>

### <span data-ttu-id="d9f8b-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9f8b-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f8b-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9f8b-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f8b-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9f8b-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f8b-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9f8b-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9f8b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9f8b-109">DESCRIPTION</span></span>
<span data-ttu-id="d9f8b-110">Il cmdlet **Reset-AzSynapseSqlPoolAuditSetting** rimuove le impostazioni di controllo di un pool SQL di analisi di una sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d9f8b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9f8b-111">EXAMPLES</span></span>

### <span data-ttu-id="d9f8b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9f8b-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="d9f8b-113">Questo comando rimuove le impostazioni di controllo di un pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d9f8b-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d9f8b-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="d9f8b-115">Questo comando rimuove le impostazioni di controllo di un pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d9f8b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9f8b-116">PARAMETERS</span></span>

### <span data-ttu-id="d9f8b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9f8b-117">-AsJob</span></span>
<span data-ttu-id="d9f8b-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d9f8b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9f8b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f8b-119">-DefaultProfile</span></span>
<span data-ttu-id="d9f8b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9f8b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9f8b-121">-InputObject</span></span>
<span data-ttu-id="d9f8b-122">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-122">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d9f8b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9f8b-123">-Name</span></span>
<span data-ttu-id="d9f8b-124">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-124">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="d9f8b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9f8b-125">-PassThru</span></span>
<span data-ttu-id="d9f8b-126">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d9f8b-127">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d9f8b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9f8b-128">-ResourceGroupName</span></span>
<span data-ttu-id="d9f8b-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-129">Resource group name.</span></span>

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

### <span data-ttu-id="d9f8b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9f8b-130">-ResourceId</span></span>
<span data-ttu-id="d9f8b-131">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-131">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="d9f8b-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d9f8b-132">-WorkspaceName</span></span>
<span data-ttu-id="d9f8b-133">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d9f8b-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d9f8b-134">-WorkspaceObject</span></span>
<span data-ttu-id="d9f8b-135">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d9f8b-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d9f8b-136">-Confirm</span></span>
<span data-ttu-id="d9f8b-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9f8b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9f8b-138">-WhatIf</span></span>
<span data-ttu-id="d9f8b-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9f8b-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9f8b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f8b-141">CommonParameters</span></span>
<span data-ttu-id="d9f8b-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f8b-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9f8b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f8b-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9f8b-144">INPUTS</span></span>

### <span data-ttu-id="d9f8b-145">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d9f8b-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d9f8b-146">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d9f8b-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d9f8b-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9f8b-147">OUTPUTS</span></span>

### <span data-ttu-id="d9f8b-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9f8b-148">System.Boolean</span></span>

## <span data-ttu-id="d9f8b-149">Note</span><span class="sxs-lookup"><span data-stu-id="d9f8b-149">NOTES</span></span>

## <span data-ttu-id="d9f8b-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9f8b-150">RELATED LINKS</span></span>
