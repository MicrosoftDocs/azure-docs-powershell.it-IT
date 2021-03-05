---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: b70c30b7652c331571030917057339a9d2d7de3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963454"
---
# <span data-ttu-id="b3d81-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="b3d81-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="b3d81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3d81-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d81-103">Rimuove un set di dati dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b3d81-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="b3d81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3d81-104">SYNTAX</span></span>

### <span data-ttu-id="b3d81-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3d81-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3d81-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="b3d81-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3d81-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3d81-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3d81-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b3d81-108">DESCRIPTION</span></span>
<span data-ttu-id="b3d81-109">Il cmdlet **Remove-AzSynapseDataset** rimuove un set di dati dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b3d81-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="b3d81-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3d81-110">EXAMPLES</span></span>

### <span data-ttu-id="b3d81-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3d81-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="b3d81-112">Questo comando rimuove il set di dati denominato ContosoDataset dall'area di lavoro contosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b3d81-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="b3d81-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3d81-113">PARAMETERS</span></span>

### <span data-ttu-id="b3d81-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3d81-114">-AsJob</span></span>
<span data-ttu-id="b3d81-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b3d81-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3d81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d81-116">-DefaultProfile</span></span>
<span data-ttu-id="b3d81-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3d81-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3d81-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b3d81-118">-Force</span></span>
<span data-ttu-id="b3d81-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b3d81-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b3d81-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3d81-120">-InputObject</span></span>
<span data-ttu-id="b3d81-121">Oggetto set di dati.</span><span class="sxs-lookup"><span data-stu-id="b3d81-121">The dataset object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d81-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b3d81-122">-Name</span></span>
<span data-ttu-id="b3d81-123">Nome del set di dati.</span><span class="sxs-lookup"><span data-stu-id="b3d81-123">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3d81-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3d81-124">-PassThru</span></span>
<span data-ttu-id="b3d81-125">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b3d81-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b3d81-126">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b3d81-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b3d81-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b3d81-127">-WorkspaceName</span></span>
<span data-ttu-id="b3d81-128">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="b3d81-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3d81-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b3d81-129">-WorkspaceObject</span></span>
<span data-ttu-id="b3d81-130">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="b3d81-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d81-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3d81-131">-Confirm</span></span>
<span data-ttu-id="b3d81-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3d81-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3d81-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3d81-133">-WhatIf</span></span>
<span data-ttu-id="b3d81-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3d81-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3d81-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3d81-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3d81-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d81-136">CommonParameters</span></span>
<span data-ttu-id="b3d81-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d81-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d81-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b3d81-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d81-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="b3d81-139">INPUTS</span></span>

### <span data-ttu-id="b3d81-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b3d81-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b3d81-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="b3d81-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="b3d81-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3d81-142">OUTPUTS</span></span>

### <span data-ttu-id="b3d81-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3d81-143">System.Boolean</span></span>

## <span data-ttu-id="b3d81-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="b3d81-144">NOTES</span></span>

## <span data-ttu-id="b3d81-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3d81-145">RELATED LINKS</span></span>
