---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201379"
---
# <span data-ttu-id="2e408-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="2e408-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="2e408-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e408-102">SYNOPSIS</span></span>
<span data-ttu-id="2e408-103">Ottiene informazioni sui trigger in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2e408-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="2e408-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e408-104">SYNTAX</span></span>

### <span data-ttu-id="2e408-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2e408-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e408-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="2e408-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e408-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e408-107">DESCRIPTION</span></span>
<span data-ttu-id="2e408-108">Il cmdlet **Get-AzSynapseTrigger** ottiene le informazioni sui trigger in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2e408-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="2e408-109">Se specifichi il nome di un trigger, il cmdlet otterrà le informazioni sul trigger.</span><span class="sxs-lookup"><span data-stu-id="2e408-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="2e408-110">Se non specifichi un nome, il cmdlet riceverà informazioni su tutti i trigger nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2e408-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="2e408-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e408-111">EXAMPLES</span></span>

### <span data-ttu-id="2e408-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2e408-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="2e408-113">Ottiene un elenco di tutti i trigger creati nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2e408-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="2e408-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2e408-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="2e408-115">Ottiene un singolo trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2e408-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="2e408-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="2e408-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="2e408-117">Ottiene un singolo trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e408-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="2e408-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e408-118">PARAMETERS</span></span>

### <span data-ttu-id="2e408-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e408-119">-DefaultProfile</span></span>
<span data-ttu-id="2e408-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e408-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e408-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e408-121">-Name</span></span>
<span data-ttu-id="2e408-122">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="2e408-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e408-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2e408-123">-WorkspaceName</span></span>
<span data-ttu-id="2e408-124">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="2e408-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2e408-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2e408-125">-WorkspaceObject</span></span>
<span data-ttu-id="2e408-126">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e408-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2e408-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e408-127">CommonParameters</span></span>
<span data-ttu-id="2e408-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e408-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e408-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e408-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e408-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e408-130">INPUTS</span></span>

### <span data-ttu-id="2e408-131">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2e408-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2e408-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e408-132">OUTPUTS</span></span>

### <span data-ttu-id="2e408-133">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="2e408-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="2e408-134">Note</span><span class="sxs-lookup"><span data-stu-id="2e408-134">NOTES</span></span>

## <span data-ttu-id="2e408-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e408-135">RELATED LINKS</span></span>
