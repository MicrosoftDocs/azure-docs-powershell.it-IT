---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189185"
---
# <span data-ttu-id="667fc-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="667fc-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="667fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="667fc-102">SYNOPSIS</span></span>
<span data-ttu-id="667fc-103">Ottiene informazioni sulle pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="667fc-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="667fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="667fc-104">SYNTAX</span></span>

### <span data-ttu-id="667fc-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="667fc-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="667fc-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="667fc-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="667fc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="667fc-107">DESCRIPTION</span></span>
<span data-ttu-id="667fc-108">Il cmdlet **Get-AzSynapsePipeline** ottiene informazioni sulle pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="667fc-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="667fc-109">Se specifichi il nome di una pipeline, questo cmdlet ottiene le informazioni sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="667fc-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="667fc-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutte le pipeline nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="667fc-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="667fc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="667fc-111">EXAMPLES</span></span>

### <span data-ttu-id="667fc-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="667fc-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="667fc-113">Questo comando consente di ottenere informazioni su tutte le pipeline nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="667fc-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="667fc-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="667fc-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="667fc-115">Questo comando ottiene le informazioni sulla pipeline denominata ContosoPipeline nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="667fc-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="667fc-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="667fc-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="667fc-117">Questo comando ottiene le informazioni sulla pipeline denominata ContosoPipeline nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="667fc-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="667fc-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="667fc-118">PARAMETERS</span></span>

### <span data-ttu-id="667fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667fc-119">-DefaultProfile</span></span>
<span data-ttu-id="667fc-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="667fc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="667fc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="667fc-121">-Name</span></span>
<span data-ttu-id="667fc-122">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="667fc-122">The pipeline name.</span></span>

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

### <span data-ttu-id="667fc-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="667fc-123">-WorkspaceName</span></span>
<span data-ttu-id="667fc-124">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="667fc-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="667fc-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="667fc-125">-WorkspaceObject</span></span>
<span data-ttu-id="667fc-126">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="667fc-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="667fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667fc-127">CommonParameters</span></span>
<span data-ttu-id="667fc-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="667fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667fc-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="667fc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667fc-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="667fc-130">INPUTS</span></span>

### <span data-ttu-id="667fc-131">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="667fc-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="667fc-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="667fc-132">OUTPUTS</span></span>

### <span data-ttu-id="667fc-133">Microsoft. Azure. Commands. sinapsi. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="667fc-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="667fc-134">Note</span><span class="sxs-lookup"><span data-stu-id="667fc-134">NOTES</span></span>

## <span data-ttu-id="667fc-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="667fc-135">RELATED LINKS</span></span>
