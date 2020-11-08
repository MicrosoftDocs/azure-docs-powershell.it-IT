---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 6fdb2a51354df01c308629eaedb09cba3a8d2fdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199779"
---
# <span data-ttu-id="15c95-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="15c95-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="15c95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15c95-102">SYNOPSIS</span></span>
<span data-ttu-id="15c95-103">Crea un'assegnazione di ruolo di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="15c95-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="15c95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15c95-104">SYNTAX</span></span>

### <span data-ttu-id="15c95-105">NewByWorkspaceNameAndNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="15c95-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c95-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c95-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c95-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c95-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c95-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c95-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c95-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c95-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15c95-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c95-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15c95-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c95-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c95-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c95-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15c95-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15c95-113">DESCRIPTION</span></span>
<span data-ttu-id="15c95-114">Il cmdlet **New-AzSynapseRoleAssignment** crea un'assegnazione di ruolo di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="15c95-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="15c95-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15c95-115">EXAMPLES</span></span>

### <span data-ttu-id="15c95-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="15c95-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="15c95-117">Questo comando assegna ContosoRole all'utente il cui nome principale è Contosoname.</span><span class="sxs-lookup"><span data-stu-id="15c95-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="15c95-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="15c95-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="15c95-119">Questo comando assegna ContosoRole all'utente il cui nome principale è Contosoname tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="15c95-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="15c95-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15c95-120">PARAMETERS</span></span>

### <span data-ttu-id="15c95-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15c95-121">-AsJob</span></span>
<span data-ttu-id="15c95-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="15c95-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15c95-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c95-123">-DefaultProfile</span></span>
<span data-ttu-id="15c95-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15c95-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c95-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="15c95-125">-ObjectId</span></span>
<span data-ttu-id="15c95-126">ID Azure AD ObjectId dell'utente, del gruppo o del servizio Principal.</span><span class="sxs-lookup"><span data-stu-id="15c95-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="15c95-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="15c95-127">-RoleDefinitionId</span></span>
<span data-ttu-id="15c95-128">ID del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="15c95-128">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="15c95-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="15c95-129">-RoleDefinitionName</span></span>
<span data-ttu-id="15c95-130">Nome del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="15c95-130">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="15c95-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="15c95-131">-ServicePrincipalName</span></span>
<span data-ttu-id="15c95-132">ServicePrincipalName dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="15c95-132">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="15c95-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="15c95-133">-SignInName</span></span>
<span data-ttu-id="15c95-134">L'indirizzo di posta elettronica o il nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="15c95-134">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="15c95-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="15c95-135">-WorkspaceName</span></span>
<span data-ttu-id="15c95-136">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="15c95-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="15c95-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="15c95-137">-WorkspaceObject</span></span>
<span data-ttu-id="15c95-138">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="15c95-138">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="15c95-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="15c95-139">-Confirm</span></span>
<span data-ttu-id="15c95-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15c95-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15c95-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15c95-141">-WhatIf</span></span>
<span data-ttu-id="15c95-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15c95-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15c95-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15c95-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15c95-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c95-144">CommonParameters</span></span>
<span data-ttu-id="15c95-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15c95-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c95-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15c95-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c95-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15c95-147">INPUTS</span></span>

### <span data-ttu-id="15c95-148">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="15c95-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="15c95-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15c95-149">OUTPUTS</span></span>

### <span data-ttu-id="15c95-150">Microsoft. Azure. Commands. sinapsi. Models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="15c95-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="15c95-151">Note</span><span class="sxs-lookup"><span data-stu-id="15c95-151">NOTES</span></span>

## <span data-ttu-id="15c95-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15c95-152">RELATED LINKS</span></span>
