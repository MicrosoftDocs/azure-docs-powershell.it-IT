---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189189"
---
# <span data-ttu-id="76557-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="76557-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="76557-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76557-102">SYNOPSIS</span></span>
<span data-ttu-id="76557-103">Ottiene informazioni sui flussi di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="76557-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="76557-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76557-104">SYNTAX</span></span>

### <span data-ttu-id="76557-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76557-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76557-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="76557-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76557-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76557-107">DESCRIPTION</span></span>
<span data-ttu-id="76557-108">Il cmdlet **Get-AzSynapseDataFlow** ottiene le informazioni sui flussi di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="76557-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="76557-109">Se specifichi il nome di un flusso di dati, questo cmdlet ottiene le informazioni sul flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="76557-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="76557-110">Se non specifichi un nome, questo cmdlet recupera le informazioni su tutti i flussi di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="76557-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="76557-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76557-111">EXAMPLES</span></span>

### <span data-ttu-id="76557-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="76557-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="76557-113">Questo comando consente di ottenere informazioni su tutti i flussi di dati nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="76557-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="76557-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="76557-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="76557-115">Questo comando consente di ottenere informazioni sul flusso di dati denominato ContosoDataFlow nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="76557-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="76557-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76557-116">PARAMETERS</span></span>

### <span data-ttu-id="76557-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76557-117">-DefaultProfile</span></span>
<span data-ttu-id="76557-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76557-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76557-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="76557-119">-Name</span></span>
<span data-ttu-id="76557-120">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="76557-120">The data flow name.</span></span>

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

### <span data-ttu-id="76557-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="76557-121">-WorkspaceName</span></span>
<span data-ttu-id="76557-122">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="76557-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="76557-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="76557-123">-WorkspaceObject</span></span>
<span data-ttu-id="76557-124">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="76557-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="76557-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76557-125">CommonParameters</span></span>
<span data-ttu-id="76557-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76557-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76557-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76557-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76557-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76557-128">INPUTS</span></span>

### <span data-ttu-id="76557-129">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="76557-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="76557-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76557-130">OUTPUTS</span></span>

### <span data-ttu-id="76557-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="76557-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="76557-132">Note</span><span class="sxs-lookup"><span data-stu-id="76557-132">NOTES</span></span>

## <span data-ttu-id="76557-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76557-133">RELATED LINKS</span></span>
