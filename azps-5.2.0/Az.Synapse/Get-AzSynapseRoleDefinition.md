---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339151"
---
# <span data-ttu-id="73461-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="73461-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="73461-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73461-102">SYNOPSIS</span></span>
<span data-ttu-id="73461-103">Ottiene una definizione del ruolo di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="73461-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="73461-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73461-104">SYNTAX</span></span>

### <span data-ttu-id="73461-105">GetByWorkspaceNameAndIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73461-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73461-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="73461-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73461-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73461-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73461-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="73461-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73461-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73461-109">DESCRIPTION</span></span>
<span data-ttu-id="73461-110">Il cmdlet **Get-AzSynapseRoleDefinition** ottiene una definizione del ruolo di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="73461-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="73461-111">Se non specifichi un nome di ruolo o un ID ruolo, questo cmdlet ottiene tutte le definizioni di ruolo.</span><span class="sxs-lookup"><span data-stu-id="73461-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="73461-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73461-112">EXAMPLES</span></span>

### <span data-ttu-id="73461-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="73461-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="73461-114">Questo comando consente di ottenere tutte le definizioni dei ruoli in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="73461-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="73461-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="73461-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="73461-116">Questo comando ottiene la definizione di ruolo in area di lavoro ContosoWorkspace con nome ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="73461-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="73461-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="73461-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="73461-118">Questo comando consente di ottenere tutte le definizioni dei ruoli in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="73461-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="73461-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73461-119">PARAMETERS</span></span>

### <span data-ttu-id="73461-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73461-120">-DefaultProfile</span></span>
<span data-ttu-id="73461-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73461-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73461-122">-ID</span><span class="sxs-lookup"><span data-stu-id="73461-122">-Id</span></span>
<span data-ttu-id="73461-123">ID del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="73461-123">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73461-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="73461-124">-Name</span></span>
<span data-ttu-id="73461-125">Nome del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="73461-125">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73461-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="73461-126">-WorkspaceName</span></span>
<span data-ttu-id="73461-127">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="73461-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73461-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="73461-128">-WorkspaceObject</span></span>
<span data-ttu-id="73461-129">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="73461-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73461-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73461-130">CommonParameters</span></span>
<span data-ttu-id="73461-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73461-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73461-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73461-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73461-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73461-133">INPUTS</span></span>

### <span data-ttu-id="73461-134">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="73461-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="73461-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73461-135">OUTPUTS</span></span>

### <span data-ttu-id="73461-136">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="73461-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="73461-137">Note</span><span class="sxs-lookup"><span data-stu-id="73461-137">NOTES</span></span>

## <span data-ttu-id="73461-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73461-138">RELATED LINKS</span></span>
