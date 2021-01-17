---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356520"
---
# <span data-ttu-id="af473-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="af473-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="af473-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af473-102">SYNOPSIS</span></span>
<span data-ttu-id="af473-103">Crea un nuovo punto di ripristino in un pool di analisi SQL sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="af473-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="af473-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af473-104">SYNTAX</span></span>

### <span data-ttu-id="af473-105">CreateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af473-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af473-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af473-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af473-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af473-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af473-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af473-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af473-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af473-109">DESCRIPTION</span></span>
<span data-ttu-id="af473-110">Il cmdlet **New-AzSynapseSqlPoolRestorePoint** crea un nuovo punto di ripristino a cui può essere ripristinato un pool di analisi SQL di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="af473-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="af473-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af473-111">EXAMPLES</span></span>

### <span data-ttu-id="af473-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="af473-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="af473-113">Questo comando crea un punto di ripristino per il pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="af473-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="af473-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af473-114">PARAMETERS</span></span>

### <span data-ttu-id="af473-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af473-115">-AsJob</span></span>
<span data-ttu-id="af473-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="af473-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af473-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af473-117">-DefaultProfile</span></span>
<span data-ttu-id="af473-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af473-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af473-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af473-119">-InputObject</span></span>
<span data-ttu-id="af473-120">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="af473-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="af473-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="af473-121">-Name</span></span>
<span data-ttu-id="af473-122">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="af473-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="af473-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af473-123">-ResourceGroupName</span></span>
<span data-ttu-id="af473-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af473-124">Resource group name.</span></span>

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

### <span data-ttu-id="af473-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af473-125">-ResourceId</span></span>
<span data-ttu-id="af473-126">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="af473-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="af473-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="af473-127">-RestorePointLabel</span></span>
<span data-ttu-id="af473-128">L'etichetta con cui associamo un punto di ripristino può non essere univoca.</span><span class="sxs-lookup"><span data-stu-id="af473-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="af473-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="af473-129">-WorkspaceName</span></span>
<span data-ttu-id="af473-130">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="af473-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="af473-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="af473-131">-WorkspaceObject</span></span>
<span data-ttu-id="af473-132">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="af473-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="af473-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af473-133">-Confirm</span></span>
<span data-ttu-id="af473-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af473-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af473-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af473-135">-WhatIf</span></span>
<span data-ttu-id="af473-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af473-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af473-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af473-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af473-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af473-138">CommonParameters</span></span>
<span data-ttu-id="af473-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af473-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af473-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af473-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af473-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af473-141">INPUTS</span></span>

### <span data-ttu-id="af473-142">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="af473-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="af473-143">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="af473-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="af473-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af473-144">OUTPUTS</span></span>

### <span data-ttu-id="af473-145">Microsoft. Azure. Commands. sinapsi. Models. PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="af473-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="af473-146">Note</span><span class="sxs-lookup"><span data-stu-id="af473-146">NOTES</span></span>

## <span data-ttu-id="af473-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af473-147">RELATED LINKS</span></span>
