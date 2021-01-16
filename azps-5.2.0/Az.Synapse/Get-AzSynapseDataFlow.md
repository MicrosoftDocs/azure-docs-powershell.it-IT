---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339271"
---
# <span data-ttu-id="be408-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="be408-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="be408-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be408-102">SYNOPSIS</span></span>
<span data-ttu-id="be408-103">Ottiene informazioni sui flussi di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="be408-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="be408-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be408-104">SYNTAX</span></span>

### <span data-ttu-id="be408-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be408-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be408-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="be408-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be408-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be408-107">DESCRIPTION</span></span>
<span data-ttu-id="be408-108">Il cmdlet **Get-AzSynapseDataFlow** ottiene le informazioni sui flussi di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="be408-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="be408-109">Se specifichi il nome di un flusso di dati, questo cmdlet ottiene le informazioni sul flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="be408-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="be408-110">Se non specifichi un nome, questo cmdlet recupera le informazioni su tutti i flussi di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="be408-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="be408-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be408-111">EXAMPLES</span></span>

### <span data-ttu-id="be408-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="be408-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="be408-113">Questo comando consente di ottenere informazioni su tutti i flussi di dati nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="be408-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="be408-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="be408-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="be408-115">Questo comando consente di ottenere informazioni sul flusso di dati denominato ContosoDataFlow nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="be408-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="be408-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be408-116">PARAMETERS</span></span>

### <span data-ttu-id="be408-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be408-117">-DefaultProfile</span></span>
<span data-ttu-id="be408-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be408-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be408-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="be408-119">-Name</span></span>
<span data-ttu-id="be408-120">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="be408-120">The data flow name.</span></span>

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

### <span data-ttu-id="be408-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="be408-121">-WorkspaceName</span></span>
<span data-ttu-id="be408-122">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="be408-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="be408-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="be408-123">-WorkspaceObject</span></span>
<span data-ttu-id="be408-124">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="be408-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="be408-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be408-125">CommonParameters</span></span>
<span data-ttu-id="be408-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be408-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be408-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be408-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be408-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be408-128">INPUTS</span></span>

### <span data-ttu-id="be408-129">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="be408-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="be408-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be408-130">OUTPUTS</span></span>

### <span data-ttu-id="be408-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="be408-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="be408-132">Note</span><span class="sxs-lookup"><span data-stu-id="be408-132">NOTES</span></span>

## <span data-ttu-id="be408-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be408-133">RELATED LINKS</span></span>
