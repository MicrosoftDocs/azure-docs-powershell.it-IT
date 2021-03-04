---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 0fa0069686a34fbd1ee60d31df96386a5d7959d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981853"
---
# <span data-ttu-id="43e5a-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="43e5a-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="43e5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="43e5a-103">Ottiene informazioni sui flussi di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="43e5a-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="43e5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43e5a-104">SYNTAX</span></span>

### <span data-ttu-id="43e5a-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43e5a-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43e5a-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="43e5a-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43e5a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="43e5a-107">DESCRIPTION</span></span>
<span data-ttu-id="43e5a-108">Il cmdlet **Get-AzSynapseDataFlow** ottiene informazioni sui flussi di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="43e5a-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="43e5a-109">Se si specifica il nome di un flusso di dati, questo cmdlet riceve informazioni sul flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="43e5a-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="43e5a-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i flussi di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="43e5a-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="43e5a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43e5a-111">EXAMPLES</span></span>

### <span data-ttu-id="43e5a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="43e5a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="43e5a-113">Questo comando recupera informazioni su tutti i flussi di dati nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="43e5a-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="43e5a-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="43e5a-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="43e5a-115">Questo comando recupera informazioni sul flusso di dati denominato ContosoDataFlow nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="43e5a-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="43e5a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43e5a-116">PARAMETERS</span></span>

### <span data-ttu-id="43e5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e5a-117">-DefaultProfile</span></span>
<span data-ttu-id="43e5a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43e5a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43e5a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="43e5a-119">-Name</span></span>
<span data-ttu-id="43e5a-120">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="43e5a-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e5a-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="43e5a-121">-WorkspaceName</span></span>
<span data-ttu-id="43e5a-122">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="43e5a-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="43e5a-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="43e5a-123">-WorkspaceObject</span></span>
<span data-ttu-id="43e5a-124">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="43e5a-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="43e5a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e5a-125">CommonParameters</span></span>
<span data-ttu-id="43e5a-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43e5a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e5a-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43e5a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e5a-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="43e5a-128">INPUTS</span></span>

### <span data-ttu-id="43e5a-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="43e5a-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="43e5a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43e5a-130">OUTPUTS</span></span>

### <span data-ttu-id="43e5a-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="43e5a-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="43e5a-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="43e5a-132">NOTES</span></span>

## <span data-ttu-id="43e5a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43e5a-133">RELATED LINKS</span></span>
