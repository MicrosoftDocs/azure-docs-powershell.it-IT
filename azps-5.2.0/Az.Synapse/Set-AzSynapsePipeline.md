---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354232"
---
# <span data-ttu-id="755c7-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="755c7-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="755c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="755c7-102">SYNOPSIS</span></span>
<span data-ttu-id="755c7-103">Crea una pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="755c7-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="755c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="755c7-104">SYNTAX</span></span>

### <span data-ttu-id="755c7-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="755c7-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="755c7-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="755c7-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="755c7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="755c7-107">DESCRIPTION</span></span>
<span data-ttu-id="755c7-108">Il cmdlet **set-AzSynapsePipeline** crea una pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="755c7-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="755c7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="755c7-109">EXAMPLES</span></span>

### <span data-ttu-id="755c7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="755c7-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="755c7-111">Questo comando crea una pipeline denominata ContosoPipeline nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="755c7-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="755c7-112">Il comando basa la pipeline sulle informazioni nella pipeline.jssu file.</span><span class="sxs-lookup"><span data-stu-id="755c7-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="755c7-113">Questo file include informazioni sulle attività.</span><span class="sxs-lookup"><span data-stu-id="755c7-113">This file includes information about activities.</span></span>

### <span data-ttu-id="755c7-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="755c7-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="755c7-115">Questo comando crea una pipeline denominata ContosoPipeline nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="755c7-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="755c7-116">Il comando basa la pipeline sulle informazioni nella pipeline.jssu file.</span><span class="sxs-lookup"><span data-stu-id="755c7-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="755c7-117">Questo file include informazioni sulle attività.</span><span class="sxs-lookup"><span data-stu-id="755c7-117">This file includes information about activities.</span></span>

## <span data-ttu-id="755c7-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="755c7-118">PARAMETERS</span></span>

### <span data-ttu-id="755c7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="755c7-119">-AsJob</span></span>
<span data-ttu-id="755c7-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="755c7-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="755c7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755c7-121">-DefaultProfile</span></span>
<span data-ttu-id="755c7-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="755c7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="755c7-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="755c7-123">-DefinitionFile</span></span>
<span data-ttu-id="755c7-124">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="755c7-124">The JSON file path.</span></span>

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

### <span data-ttu-id="755c7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="755c7-125">-Name</span></span>
<span data-ttu-id="755c7-126">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="755c7-126">The pipeline name.</span></span>

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

### <span data-ttu-id="755c7-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="755c7-127">-WorkspaceName</span></span>
<span data-ttu-id="755c7-128">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="755c7-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="755c7-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="755c7-129">-WorkspaceObject</span></span>
<span data-ttu-id="755c7-130">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="755c7-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="755c7-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="755c7-131">-Confirm</span></span>
<span data-ttu-id="755c7-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="755c7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="755c7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="755c7-133">-WhatIf</span></span>
<span data-ttu-id="755c7-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="755c7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="755c7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="755c7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="755c7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755c7-136">CommonParameters</span></span>
<span data-ttu-id="755c7-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755c7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755c7-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="755c7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755c7-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="755c7-139">INPUTS</span></span>

### <span data-ttu-id="755c7-140">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="755c7-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="755c7-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="755c7-141">OUTPUTS</span></span>

### <span data-ttu-id="755c7-142">Microsoft. Azure. Commands. sinapsi. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="755c7-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="755c7-143">Note</span><span class="sxs-lookup"><span data-stu-id="755c7-143">NOTES</span></span>

## <span data-ttu-id="755c7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="755c7-144">RELATED LINKS</span></span>
