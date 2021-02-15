---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197391"
---
# <span data-ttu-id="1a193-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="1a193-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="1a193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a193-102">SYNOPSIS</span></span>
<span data-ttu-id="1a193-103">Recupera informazioni sui set di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1a193-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="1a193-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a193-104">SYNTAX</span></span>

### <span data-ttu-id="1a193-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a193-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a193-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="1a193-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a193-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1a193-107">DESCRIPTION</span></span>
<span data-ttu-id="1a193-108">Il cmdlet **Get-AzSynapseDataset** ottiene informazioni sui set di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1a193-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="1a193-109">Se si specifica il nome di un set di dati, questo cmdlet ottiene informazioni sul set di dati.</span><span class="sxs-lookup"><span data-stu-id="1a193-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="1a193-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i set di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1a193-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="1a193-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a193-111">EXAMPLES</span></span>

### <span data-ttu-id="1a193-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a193-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="1a193-113">Questo comando recupera informazioni su tutti i set di dati nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1a193-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1a193-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1a193-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="1a193-115">Questo comando recupera informazioni sul set di dati denominato ContosoDataset nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1a193-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="1a193-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a193-116">PARAMETERS</span></span>

### <span data-ttu-id="1a193-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a193-117">-DefaultProfile</span></span>
<span data-ttu-id="1a193-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a193-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a193-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1a193-119">-Name</span></span>
<span data-ttu-id="1a193-120">Il nome del set di dati.</span><span class="sxs-lookup"><span data-stu-id="1a193-120">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a193-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1a193-121">-WorkspaceName</span></span>
<span data-ttu-id="1a193-122">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="1a193-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1a193-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1a193-123">-WorkspaceObject</span></span>
<span data-ttu-id="1a193-124">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="1a193-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1a193-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a193-125">CommonParameters</span></span>
<span data-ttu-id="1a193-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a193-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a193-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1a193-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a193-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="1a193-128">INPUTS</span></span>

### <span data-ttu-id="1a193-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1a193-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1a193-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a193-130">OUTPUTS</span></span>

### <span data-ttu-id="1a193-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="1a193-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="1a193-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="1a193-132">NOTES</span></span>

## <span data-ttu-id="1a193-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a193-133">RELATED LINKS</span></span>
