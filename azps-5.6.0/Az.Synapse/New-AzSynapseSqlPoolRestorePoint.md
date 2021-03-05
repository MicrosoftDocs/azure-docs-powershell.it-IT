---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 1f30dd8d0757e857934c1f8337e879cf1de8384e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963470"
---
# <span data-ttu-id="f62c7-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="f62c7-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="f62c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f62c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f62c7-103">Crea un nuovo punto di ripristino in un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f62c7-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f62c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f62c7-104">SYNTAX</span></span>

### <span data-ttu-id="f62c7-105">CreateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f62c7-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f62c7-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f62c7-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f62c7-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f62c7-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f62c7-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f62c7-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f62c7-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f62c7-109">DESCRIPTION</span></span>
<span data-ttu-id="f62c7-110">Il cmdlet **New-AzSynapseSqlPoolRestorePoint** crea un nuovo punto di ripristino da cui è possibile ripristinare un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f62c7-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="f62c7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f62c7-111">EXAMPLES</span></span>

### <span data-ttu-id="f62c7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f62c7-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="f62c7-113">Questo comando crea un punto di ripristino per SQL pool denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f62c7-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="f62c7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f62c7-114">PARAMETERS</span></span>

### <span data-ttu-id="f62c7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f62c7-115">-AsJob</span></span>
<span data-ttu-id="f62c7-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f62c7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f62c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f62c7-117">-DefaultProfile</span></span>
<span data-ttu-id="f62c7-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f62c7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f62c7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f62c7-119">-InputObject</span></span>
<span data-ttu-id="f62c7-120">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="f62c7-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f62c7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f62c7-121">-Name</span></span>
<span data-ttu-id="f62c7-122">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f62c7-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f62c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="f62c7-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f62c7-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62c7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f62c7-125">-ResourceId</span></span>
<span data-ttu-id="f62c7-126">Identificatore di risorsa del pool SQL synapse.</span><span class="sxs-lookup"><span data-stu-id="f62c7-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62c7-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="f62c7-127">-RestorePointLabel</span></span>
<span data-ttu-id="f62c7-128">L'etichetta a cui associa un punto di ripristino potrebbe non essere univoca.</span><span class="sxs-lookup"><span data-stu-id="f62c7-128">The label we associate a restore point with, may not be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62c7-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f62c7-129">-WorkspaceName</span></span>
<span data-ttu-id="f62c7-130">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="f62c7-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62c7-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f62c7-131">-WorkspaceObject</span></span>
<span data-ttu-id="f62c7-132">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="f62c7-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f62c7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f62c7-133">-Confirm</span></span>
<span data-ttu-id="f62c7-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f62c7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f62c7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f62c7-135">-WhatIf</span></span>
<span data-ttu-id="f62c7-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f62c7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f62c7-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f62c7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f62c7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62c7-138">CommonParameters</span></span>
<span data-ttu-id="f62c7-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f62c7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62c7-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f62c7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62c7-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="f62c7-141">INPUTS</span></span>

### <span data-ttu-id="f62c7-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f62c7-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f62c7-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f62c7-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f62c7-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f62c7-144">OUTPUTS</span></span>

### <span data-ttu-id="f62c7-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="f62c7-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="f62c7-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="f62c7-146">NOTES</span></span>

## <span data-ttu-id="f62c7-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f62c7-147">RELATED LINKS</span></span>
