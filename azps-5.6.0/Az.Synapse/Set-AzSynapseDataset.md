---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: 1001aa2f282ab59e6ddc9e3e1ecc654950d8e30e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952973"
---
# <span data-ttu-id="c9f49-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="c9f49-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="c9f49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9f49-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f49-103">Crea o aggiorna un set di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9f49-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="c9f49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9f49-104">SYNTAX</span></span>

### <span data-ttu-id="c9f49-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c9f49-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f49-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="c9f49-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9f49-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c9f49-107">DESCRIPTION</span></span>
<span data-ttu-id="c9f49-108">Il cmdlet **Set-AzSynapseDataset** crea un set di dati o aggiorna un set di dati esistente nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9f49-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="c9f49-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9f49-109">EXAMPLES</span></span>

### <span data-ttu-id="c9f49-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9f49-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="c9f49-111">Questo comando crea un set di dati denominato ContosoDataset nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c9f49-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="c9f49-112">Il comando basa il set di dati sulle informazioni Dataset.jssu file.</span><span class="sxs-lookup"><span data-stu-id="c9f49-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="c9f49-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9f49-113">PARAMETERS</span></span>

### <span data-ttu-id="c9f49-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9f49-114">-AsJob</span></span>
<span data-ttu-id="c9f49-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c9f49-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9f49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f49-116">-DefaultProfile</span></span>
<span data-ttu-id="c9f49-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f49-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9f49-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c9f49-118">-DefinitionFile</span></span>
<span data-ttu-id="c9f49-119">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="c9f49-119">The JSON file path.</span></span>

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

### <span data-ttu-id="c9f49-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c9f49-120">-Name</span></span>
<span data-ttu-id="c9f49-121">Nome del set di dati.</span><span class="sxs-lookup"><span data-stu-id="c9f49-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f49-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c9f49-122">-WorkspaceName</span></span>
<span data-ttu-id="c9f49-123">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="c9f49-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c9f49-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c9f49-124">-WorkspaceObject</span></span>
<span data-ttu-id="c9f49-125">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9f49-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c9f49-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9f49-126">-Confirm</span></span>
<span data-ttu-id="c9f49-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9f49-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9f49-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f49-128">-WhatIf</span></span>
<span data-ttu-id="c9f49-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9f49-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9f49-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9f49-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9f49-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f49-131">CommonParameters</span></span>
<span data-ttu-id="c9f49-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9f49-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f49-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c9f49-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f49-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="c9f49-134">INPUTS</span></span>

### <span data-ttu-id="c9f49-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c9f49-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c9f49-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9f49-136">OUTPUTS</span></span>

### <span data-ttu-id="c9f49-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="c9f49-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="c9f49-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="c9f49-138">NOTES</span></span>

## <span data-ttu-id="c9f49-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9f49-139">RELATED LINKS</span></span>
