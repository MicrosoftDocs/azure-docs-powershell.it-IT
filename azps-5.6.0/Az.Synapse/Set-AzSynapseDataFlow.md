---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4254a301e599dac542a099b9c4f2ebace8929ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952974"
---
# <span data-ttu-id="1eb5c-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="1eb5c-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="1eb5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eb5c-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb5c-103">Crea o aggiorna un flusso di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="1eb5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1eb5c-104">SYNTAX</span></span>

### <span data-ttu-id="1eb5c-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1eb5c-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eb5c-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="1eb5c-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eb5c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1eb5c-107">DESCRIPTION</span></span>
<span data-ttu-id="1eb5c-108">Il cmdlet **Set-AzSynapseDataFlow** crea un flusso di dati o aggiorna un flusso di dati esistente nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="1eb5c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1eb5c-109">EXAMPLES</span></span>

### <span data-ttu-id="1eb5c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1eb5c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="1eb5c-111">Questo comando crea un flusso di dati denominato ContosoDataFlow nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="1eb5c-112">Il comando basa il flusso di dati sulle informazioni DataFlow.jssu file.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="1eb5c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1eb5c-113">PARAMETERS</span></span>

### <span data-ttu-id="1eb5c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1eb5c-114">-AsJob</span></span>
<span data-ttu-id="1eb5c-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1eb5c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1eb5c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb5c-116">-DefaultProfile</span></span>
<span data-ttu-id="1eb5c-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eb5c-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="1eb5c-118">-DefinitionFile</span></span>
<span data-ttu-id="1eb5c-119">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-119">The JSON file path.</span></span>

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

### <span data-ttu-id="1eb5c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1eb5c-120">-Name</span></span>
<span data-ttu-id="1eb5c-121">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb5c-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1eb5c-122">-WorkspaceName</span></span>
<span data-ttu-id="1eb5c-123">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1eb5c-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1eb5c-124">-WorkspaceObject</span></span>
<span data-ttu-id="1eb5c-125">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1eb5c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1eb5c-126">-Confirm</span></span>
<span data-ttu-id="1eb5c-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eb5c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb5c-128">-WhatIf</span></span>
<span data-ttu-id="1eb5c-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eb5c-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eb5c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb5c-131">CommonParameters</span></span>
<span data-ttu-id="1eb5c-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb5c-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1eb5c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb5c-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="1eb5c-134">INPUTS</span></span>

### <span data-ttu-id="1eb5c-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1eb5c-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1eb5c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1eb5c-136">OUTPUTS</span></span>

### <span data-ttu-id="1eb5c-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="1eb5c-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="1eb5c-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="1eb5c-138">NOTES</span></span>

## <span data-ttu-id="1eb5c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1eb5c-139">RELATED LINKS</span></span>
