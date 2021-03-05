---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6161a0ca463973fad1ac7bac5df6487cf23cd0e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967197"
---
# <span data-ttu-id="c6818-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="c6818-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="c6818-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6818-102">SYNOPSIS</span></span>
<span data-ttu-id="c6818-103">Ottiene informazioni sulle pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c6818-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="c6818-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6818-104">SYNTAX</span></span>

### <span data-ttu-id="c6818-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6818-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6818-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="c6818-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6818-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c6818-107">DESCRIPTION</span></span>
<span data-ttu-id="c6818-108">Il cmdlet **Get-AzSynapsePipeline** ottiene informazioni sulle pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c6818-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="c6818-109">Se si specifica il nome di una pipeline, questo cmdlet ottiene informazioni sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="c6818-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="c6818-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutte le pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c6818-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="c6818-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6818-111">EXAMPLES</span></span>

### <span data-ttu-id="c6818-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c6818-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="c6818-113">Questo comando recupera informazioni su tutte le pipeline dell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c6818-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="c6818-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c6818-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="c6818-115">Questo comando ottiene informazioni sulla pipeline denominata ContosoPipeline nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c6818-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="c6818-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c6818-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="c6818-117">Questo comando recupera informazioni sulla pipeline denominata ContosoPipeline nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="c6818-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c6818-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6818-118">PARAMETERS</span></span>

### <span data-ttu-id="c6818-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6818-119">-DefaultProfile</span></span>
<span data-ttu-id="c6818-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6818-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6818-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c6818-121">-Name</span></span>
<span data-ttu-id="c6818-122">Nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="c6818-122">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6818-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c6818-123">-WorkspaceName</span></span>
<span data-ttu-id="c6818-124">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="c6818-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6818-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c6818-125">-WorkspaceObject</span></span>
<span data-ttu-id="c6818-126">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="c6818-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6818-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6818-127">CommonParameters</span></span>
<span data-ttu-id="c6818-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6818-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6818-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c6818-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6818-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="c6818-130">INPUTS</span></span>

### <span data-ttu-id="c6818-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c6818-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c6818-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6818-132">OUTPUTS</span></span>

### <span data-ttu-id="c6818-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="c6818-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="c6818-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="c6818-134">NOTES</span></span>

## <span data-ttu-id="c6818-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6818-135">RELATED LINKS</span></span>
