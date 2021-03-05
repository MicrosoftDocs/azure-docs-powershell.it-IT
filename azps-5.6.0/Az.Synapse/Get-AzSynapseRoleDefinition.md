---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: 061cd16f4a2c9099be73fa2c2bdb54ff9f089949
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008254"
---
# <span data-ttu-id="98892-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="98892-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="98892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98892-102">SYNOPSIS</span></span>
<span data-ttu-id="98892-103">Ottiene una definizione di ruolo di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="98892-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="98892-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98892-104">SYNTAX</span></span>

### <span data-ttu-id="98892-105">GetByWorkspaceNameAndIdParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98892-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98892-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="98892-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98892-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98892-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98892-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="98892-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98892-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="98892-109">DESCRIPTION</span></span>
<span data-ttu-id="98892-110">Il cmdlet **Get-AzSynapseRoleDefinition** ottiene una definizione del ruolo di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="98892-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="98892-111">Se non si specifica un nome di ruolo o un ID ruolo, questo cmdlet ottiene tutte le definizioni di ruolo.</span><span class="sxs-lookup"><span data-stu-id="98892-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="98892-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98892-112">EXAMPLES</span></span>

### <span data-ttu-id="98892-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="98892-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="98892-114">Questo comando recupera tutte le definizioni di ruolo in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="98892-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="98892-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="98892-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="98892-116">Questo comando recupera la definizione di ruolo nell'area di lavoro ContosoWorkspace con il nome ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="98892-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="98892-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="98892-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="98892-118">Questo comando recupera tutte le definizioni di ruolo in un'area di lavoro tramite una pipeline.</span><span class="sxs-lookup"><span data-stu-id="98892-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="98892-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98892-119">PARAMETERS</span></span>

### <span data-ttu-id="98892-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98892-120">-DefaultProfile</span></span>
<span data-ttu-id="98892-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98892-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98892-122">-Id</span><span class="sxs-lookup"><span data-stu-id="98892-122">-Id</span></span>
<span data-ttu-id="98892-123">ID del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="98892-123">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="98892-124">-Name</span><span class="sxs-lookup"><span data-stu-id="98892-124">-Name</span></span>
<span data-ttu-id="98892-125">Nome del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="98892-125">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="98892-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="98892-126">-WorkspaceName</span></span>
<span data-ttu-id="98892-127">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="98892-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="98892-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="98892-128">-WorkspaceObject</span></span>
<span data-ttu-id="98892-129">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="98892-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="98892-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98892-130">CommonParameters</span></span>
<span data-ttu-id="98892-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98892-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98892-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98892-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98892-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="98892-133">INPUTS</span></span>

### <span data-ttu-id="98892-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="98892-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="98892-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98892-135">OUTPUTS</span></span>

### <span data-ttu-id="98892-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="98892-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="98892-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="98892-137">NOTES</span></span>

## <span data-ttu-id="98892-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98892-138">RELATED LINKS</span></span>
