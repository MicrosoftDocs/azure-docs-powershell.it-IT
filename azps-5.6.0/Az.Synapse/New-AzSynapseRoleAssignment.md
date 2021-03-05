---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 7e216a6d2751ddd24e7d948cb6cca036c2a9b336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976077"
---
# <span data-ttu-id="955c0-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="955c0-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="955c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="955c0-102">SYNOPSIS</span></span>
<span data-ttu-id="955c0-103">Crea un'assegnazione di ruolo di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="955c0-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="955c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="955c0-104">SYNTAX</span></span>

### <span data-ttu-id="955c0-105">NewByWorkspaceNameAndNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="955c0-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955c0-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="955c0-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955c0-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="955c0-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955c0-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="955c0-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955c0-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="955c0-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="955c0-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="955c0-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="955c0-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="955c0-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955c0-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="955c0-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="955c0-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="955c0-113">DESCRIPTION</span></span>
<span data-ttu-id="955c0-114">Il cmdlet **New-AzSynapseRoleAssignment** crea un'assegnazione di ruolo di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="955c0-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="955c0-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="955c0-115">EXAMPLES</span></span>

### <span data-ttu-id="955c0-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="955c0-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="955c0-117">Questo comando assegna ContosoRole all'utente il cui nome dell'entità è ContosoName.</span><span class="sxs-lookup"><span data-stu-id="955c0-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="955c0-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="955c0-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="955c0-119">Questo comando assegna ContosoRole all'utente il cui nome dell'entità è ContosoName tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="955c0-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="955c0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="955c0-120">PARAMETERS</span></span>

### <span data-ttu-id="955c0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="955c0-121">-AsJob</span></span>
<span data-ttu-id="955c0-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="955c0-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="955c0-123">-DefaultProfile</span></span>
<span data-ttu-id="955c0-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="955c0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="955c0-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="955c0-125">-ObjectId</span></span>
<span data-ttu-id="955c0-126">ObjectId di Azure AD dell'utente, del gruppo o dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="955c0-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c0-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="955c0-127">-RoleDefinitionId</span></span>
<span data-ttu-id="955c0-128">ID del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="955c0-128">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c0-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="955c0-129">-RoleDefinitionName</span></span>
<span data-ttu-id="955c0-130">Nome del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="955c0-130">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c0-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="955c0-131">-ServicePrincipalName</span></span>
<span data-ttu-id="955c0-132">ServicePrincipalName dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="955c0-132">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c0-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="955c0-133">-SignInName</span></span>
<span data-ttu-id="955c0-134">Indirizzo di posta elettronica o nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="955c0-134">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c0-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="955c0-135">-WorkspaceName</span></span>
<span data-ttu-id="955c0-136">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="955c0-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c0-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="955c0-137">-WorkspaceObject</span></span>
<span data-ttu-id="955c0-138">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="955c0-138">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="955c0-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="955c0-139">-Confirm</span></span>
<span data-ttu-id="955c0-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="955c0-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="955c0-141">-WhatIf</span></span>
<span data-ttu-id="955c0-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="955c0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="955c0-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="955c0-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="955c0-144">CommonParameters</span></span>
<span data-ttu-id="955c0-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="955c0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="955c0-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="955c0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="955c0-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="955c0-147">INPUTS</span></span>

### <span data-ttu-id="955c0-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="955c0-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="955c0-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="955c0-149">OUTPUTS</span></span>

### <span data-ttu-id="955c0-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="955c0-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="955c0-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="955c0-151">NOTES</span></span>

## <span data-ttu-id="955c0-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="955c0-152">RELATED LINKS</span></span>
