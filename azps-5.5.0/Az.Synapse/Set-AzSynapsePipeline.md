---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188774"
---
# <span data-ttu-id="811eb-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="811eb-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="811eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="811eb-102">SYNOPSIS</span></span>
<span data-ttu-id="811eb-103">Crea una pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="811eb-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="811eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="811eb-104">SYNTAX</span></span>

### <span data-ttu-id="811eb-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="811eb-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="811eb-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="811eb-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="811eb-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="811eb-107">DESCRIPTION</span></span>
<span data-ttu-id="811eb-108">Il cmdlet **Set-AzSynapsePipeline** crea una pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="811eb-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="811eb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="811eb-109">EXAMPLES</span></span>

### <span data-ttu-id="811eb-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="811eb-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="811eb-111">Questo comando crea una pipeline denominata ContosoPipeline nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="811eb-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="811eb-112">Il comando basa la pipeline sulle informazioni del pipeline.jsfile.</span><span class="sxs-lookup"><span data-stu-id="811eb-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="811eb-113">Il file include informazioni sulle attività.</span><span class="sxs-lookup"><span data-stu-id="811eb-113">This file includes information about activities.</span></span>

### <span data-ttu-id="811eb-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="811eb-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="811eb-115">Questo comando crea una pipeline denominata ContosoPipeline nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="811eb-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="811eb-116">Il comando basa la pipeline sulle informazioni del pipeline.jsfile.</span><span class="sxs-lookup"><span data-stu-id="811eb-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="811eb-117">Il file include informazioni sulle attività.</span><span class="sxs-lookup"><span data-stu-id="811eb-117">This file includes information about activities.</span></span>

## <span data-ttu-id="811eb-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="811eb-118">PARAMETERS</span></span>

### <span data-ttu-id="811eb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="811eb-119">-AsJob</span></span>
<span data-ttu-id="811eb-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="811eb-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="811eb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="811eb-121">-DefaultProfile</span></span>
<span data-ttu-id="811eb-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="811eb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="811eb-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="811eb-123">-DefinitionFile</span></span>
<span data-ttu-id="811eb-124">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="811eb-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="811eb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="811eb-125">-Name</span></span>
<span data-ttu-id="811eb-126">Nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="811eb-126">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="811eb-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="811eb-127">-WorkspaceName</span></span>
<span data-ttu-id="811eb-128">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="811eb-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="811eb-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="811eb-129">-WorkspaceObject</span></span>
<span data-ttu-id="811eb-130">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="811eb-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="811eb-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="811eb-131">-Confirm</span></span>
<span data-ttu-id="811eb-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="811eb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="811eb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="811eb-133">-WhatIf</span></span>
<span data-ttu-id="811eb-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="811eb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="811eb-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="811eb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="811eb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="811eb-136">CommonParameters</span></span>
<span data-ttu-id="811eb-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="811eb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="811eb-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="811eb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="811eb-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="811eb-139">INPUTS</span></span>

### <span data-ttu-id="811eb-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="811eb-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="811eb-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="811eb-141">OUTPUTS</span></span>

### <span data-ttu-id="811eb-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="811eb-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="811eb-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="811eb-143">NOTES</span></span>

## <span data-ttu-id="811eb-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="811eb-144">RELATED LINKS</span></span>
