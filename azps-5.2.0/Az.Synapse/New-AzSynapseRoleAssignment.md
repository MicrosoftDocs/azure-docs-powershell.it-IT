---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 6fdb2a51354df01c308629eaedb09cba3a8d2fdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341932"
---
# <span data-ttu-id="45ef7-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="45ef7-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="45ef7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45ef7-102">SYNOPSIS</span></span>
<span data-ttu-id="45ef7-103">Crea un'assegnazione di ruolo di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="45ef7-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="45ef7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45ef7-104">SYNTAX</span></span>

### <span data-ttu-id="45ef7-105">NewByWorkspaceNameAndNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="45ef7-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ef7-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45ef7-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ef7-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45ef7-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ef7-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="45ef7-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ef7-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="45ef7-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45ef7-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45ef7-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45ef7-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45ef7-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ef7-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="45ef7-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45ef7-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45ef7-113">DESCRIPTION</span></span>
<span data-ttu-id="45ef7-114">Il cmdlet **New-AzSynapseRoleAssignment** crea un'assegnazione di ruolo di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="45ef7-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="45ef7-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45ef7-115">EXAMPLES</span></span>

### <span data-ttu-id="45ef7-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="45ef7-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="45ef7-117">Questo comando assegna ContosoRole all'utente il cui nome principale è Contosoname.</span><span class="sxs-lookup"><span data-stu-id="45ef7-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="45ef7-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="45ef7-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="45ef7-119">Questo comando assegna ContosoRole all'utente il cui nome principale è Contosoname tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="45ef7-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="45ef7-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45ef7-120">PARAMETERS</span></span>

### <span data-ttu-id="45ef7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45ef7-121">-AsJob</span></span>
<span data-ttu-id="45ef7-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="45ef7-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45ef7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ef7-123">-DefaultProfile</span></span>
<span data-ttu-id="45ef7-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45ef7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45ef7-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="45ef7-125">-ObjectId</span></span>
<span data-ttu-id="45ef7-126">ID Azure AD ObjectId dell'utente, del gruppo o del servizio Principal.</span><span class="sxs-lookup"><span data-stu-id="45ef7-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="45ef7-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="45ef7-127">-RoleDefinitionId</span></span>
<span data-ttu-id="45ef7-128">ID del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="45ef7-128">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="45ef7-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="45ef7-129">-RoleDefinitionName</span></span>
<span data-ttu-id="45ef7-130">Nome del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="45ef7-130">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="45ef7-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="45ef7-131">-ServicePrincipalName</span></span>
<span data-ttu-id="45ef7-132">ServicePrincipalName dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="45ef7-132">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="45ef7-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="45ef7-133">-SignInName</span></span>
<span data-ttu-id="45ef7-134">L'indirizzo di posta elettronica o il nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="45ef7-134">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="45ef7-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="45ef7-135">-WorkspaceName</span></span>
<span data-ttu-id="45ef7-136">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="45ef7-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="45ef7-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="45ef7-137">-WorkspaceObject</span></span>
<span data-ttu-id="45ef7-138">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="45ef7-138">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="45ef7-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45ef7-139">-Confirm</span></span>
<span data-ttu-id="45ef7-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45ef7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45ef7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45ef7-141">-WhatIf</span></span>
<span data-ttu-id="45ef7-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45ef7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45ef7-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45ef7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45ef7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ef7-144">CommonParameters</span></span>
<span data-ttu-id="45ef7-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ef7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ef7-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45ef7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ef7-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45ef7-147">INPUTS</span></span>

### <span data-ttu-id="45ef7-148">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="45ef7-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="45ef7-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45ef7-149">OUTPUTS</span></span>

### <span data-ttu-id="45ef7-150">Microsoft. Azure. Commands. sinapsi. Models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="45ef7-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="45ef7-151">Note</span><span class="sxs-lookup"><span data-stu-id="45ef7-151">NOTES</span></span>

## <span data-ttu-id="45ef7-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45ef7-152">RELATED LINKS</span></span>
