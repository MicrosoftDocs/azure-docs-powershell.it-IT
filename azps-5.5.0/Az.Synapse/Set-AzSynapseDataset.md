---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198334"
---
# <span data-ttu-id="3cf87-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="3cf87-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="3cf87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cf87-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf87-103">Crea o aggiorna un set di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3cf87-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="3cf87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cf87-104">SYNTAX</span></span>

### <span data-ttu-id="3cf87-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3cf87-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf87-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="3cf87-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cf87-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3cf87-107">DESCRIPTION</span></span>
<span data-ttu-id="3cf87-108">Il cmdlet **Set-AzSynapseDataset** crea un set di dati o aggiorna un set di dati esistente nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3cf87-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="3cf87-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cf87-109">EXAMPLES</span></span>

### <span data-ttu-id="3cf87-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3cf87-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="3cf87-111">Questo comando crea un set di dati denominato ContosoDataset nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3cf87-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="3cf87-112">Il comando basa il set di dati sulle informazioni Dataset.jssu file.</span><span class="sxs-lookup"><span data-stu-id="3cf87-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="3cf87-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cf87-113">PARAMETERS</span></span>

### <span data-ttu-id="3cf87-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cf87-114">-AsJob</span></span>
<span data-ttu-id="3cf87-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3cf87-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cf87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf87-116">-DefaultProfile</span></span>
<span data-ttu-id="3cf87-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf87-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf87-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="3cf87-118">-DefinitionFile</span></span>
<span data-ttu-id="3cf87-119">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="3cf87-119">The JSON file path.</span></span>

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

### <span data-ttu-id="3cf87-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3cf87-120">-Name</span></span>
<span data-ttu-id="3cf87-121">Il nome del set di dati.</span><span class="sxs-lookup"><span data-stu-id="3cf87-121">The dataset name.</span></span>

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

### <span data-ttu-id="3cf87-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3cf87-122">-WorkspaceName</span></span>
<span data-ttu-id="3cf87-123">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="3cf87-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3cf87-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3cf87-124">-WorkspaceObject</span></span>
<span data-ttu-id="3cf87-125">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="3cf87-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3cf87-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cf87-126">-Confirm</span></span>
<span data-ttu-id="3cf87-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cf87-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf87-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf87-128">-WhatIf</span></span>
<span data-ttu-id="3cf87-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cf87-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cf87-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cf87-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf87-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf87-131">CommonParameters</span></span>
<span data-ttu-id="3cf87-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf87-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf87-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3cf87-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf87-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="3cf87-134">INPUTS</span></span>

### <span data-ttu-id="3cf87-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3cf87-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3cf87-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cf87-136">OUTPUTS</span></span>

### <span data-ttu-id="3cf87-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="3cf87-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="3cf87-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="3cf87-138">NOTES</span></span>

## <span data-ttu-id="3cf87-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cf87-139">RELATED LINKS</span></span>
