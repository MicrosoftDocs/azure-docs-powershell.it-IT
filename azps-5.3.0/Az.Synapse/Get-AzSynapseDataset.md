---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474566"
---
# <span data-ttu-id="abfe0-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="abfe0-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="abfe0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="abfe0-102">SYNOPSIS</span></span>
<span data-ttu-id="abfe0-103">Ottiene informazioni sui set di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="abfe0-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="abfe0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abfe0-104">SYNTAX</span></span>

### <span data-ttu-id="abfe0-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="abfe0-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abfe0-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="abfe0-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abfe0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abfe0-107">DESCRIPTION</span></span>
<span data-ttu-id="abfe0-108">Il cmdlet **Get-AzSynapseDataset** ottiene le informazioni sui DataSet nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="abfe0-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="abfe0-109">Se specifichi il nome di un DataSet, questo cmdlet ottiene le informazioni su tale set di dati.</span><span class="sxs-lookup"><span data-stu-id="abfe0-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="abfe0-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i DataSet nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="abfe0-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="abfe0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abfe0-111">EXAMPLES</span></span>

### <span data-ttu-id="abfe0-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="abfe0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="abfe0-113">Questo comando consente di ottenere informazioni su tutti i DataSet nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="abfe0-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="abfe0-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="abfe0-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="abfe0-115">Questo comando consente di ottenere informazioni sul DataSet denominato ContosoDataset nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="abfe0-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="abfe0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="abfe0-116">PARAMETERS</span></span>

### <span data-ttu-id="abfe0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abfe0-117">-DefaultProfile</span></span>
<span data-ttu-id="abfe0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="abfe0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abfe0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="abfe0-119">-Name</span></span>
<span data-ttu-id="abfe0-120">Nome del DataSet.</span><span class="sxs-lookup"><span data-stu-id="abfe0-120">The dataset name.</span></span>

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

### <span data-ttu-id="abfe0-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="abfe0-121">-WorkspaceName</span></span>
<span data-ttu-id="abfe0-122">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="abfe0-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="abfe0-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="abfe0-123">-WorkspaceObject</span></span>
<span data-ttu-id="abfe0-124">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="abfe0-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="abfe0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abfe0-125">CommonParameters</span></span>
<span data-ttu-id="abfe0-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abfe0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abfe0-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abfe0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abfe0-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="abfe0-128">INPUTS</span></span>

### <span data-ttu-id="abfe0-129">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="abfe0-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="abfe0-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abfe0-130">OUTPUTS</span></span>

### <span data-ttu-id="abfe0-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="abfe0-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="abfe0-132">Note</span><span class="sxs-lookup"><span data-stu-id="abfe0-132">NOTES</span></span>

## <span data-ttu-id="abfe0-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abfe0-133">RELATED LINKS</span></span>
