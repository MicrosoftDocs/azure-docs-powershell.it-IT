---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384044"
---
# <span data-ttu-id="c8b88-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="c8b88-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="c8b88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8b88-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b88-103">Ottiene informazioni sulle pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c8b88-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="c8b88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8b88-104">SYNTAX</span></span>

### <span data-ttu-id="c8b88-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c8b88-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8b88-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="c8b88-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8b88-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8b88-107">DESCRIPTION</span></span>
<span data-ttu-id="c8b88-108">Il cmdlet **Get-AzSynapsePipeline** ottiene informazioni sulle pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c8b88-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="c8b88-109">Se specifichi il nome di una pipeline, questo cmdlet ottiene le informazioni sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8b88-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="c8b88-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutte le pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c8b88-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="c8b88-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8b88-111">EXAMPLES</span></span>

### <span data-ttu-id="c8b88-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8b88-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="c8b88-113">Questo comando consente di ottenere informazioni su tutte le pipeline nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c8b88-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="c8b88-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c8b88-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="c8b88-115">Questo comando ottiene le informazioni sulla pipeline denominata ContosoPipeline nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c8b88-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="c8b88-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c8b88-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="c8b88-117">Questo comando ottiene le informazioni sulla pipeline denominata ContosoPipeline nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8b88-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c8b88-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8b88-118">PARAMETERS</span></span>

### <span data-ttu-id="c8b88-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b88-119">-DefaultProfile</span></span>
<span data-ttu-id="c8b88-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8b88-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8b88-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8b88-121">-Name</span></span>
<span data-ttu-id="c8b88-122">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8b88-122">The pipeline name.</span></span>

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

### <span data-ttu-id="c8b88-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c8b88-123">-WorkspaceName</span></span>
<span data-ttu-id="c8b88-124">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="c8b88-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c8b88-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c8b88-125">-WorkspaceObject</span></span>
<span data-ttu-id="c8b88-126">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8b88-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c8b88-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b88-127">CommonParameters</span></span>
<span data-ttu-id="c8b88-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8b88-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b88-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8b88-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b88-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8b88-130">INPUTS</span></span>

### <span data-ttu-id="c8b88-131">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8b88-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c8b88-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8b88-132">OUTPUTS</span></span>

### <span data-ttu-id="c8b88-133">Microsoft. Azure. Commands. sinapsi. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="c8b88-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="c8b88-134">Note</span><span class="sxs-lookup"><span data-stu-id="c8b88-134">NOTES</span></span>

## <span data-ttu-id="c8b88-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8b88-135">RELATED LINKS</span></span>
