---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182727"
---
# <span data-ttu-id="7fac9-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7fac9-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="7fac9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fac9-102">SYNOPSIS</span></span>
<span data-ttu-id="7fac9-103">Elimina un'assegnazione di ruolo di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7fac9-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="7fac9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fac9-104">SYNTAX</span></span>

### <span data-ttu-id="7fac9-105">RemoveByWorkspaceNameAndNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7fac9-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fac9-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fac9-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fac9-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fac9-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fac9-108">RemoveByWorkspaceNameAndRoleIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fac9-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fac9-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fac9-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fac9-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fac9-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fac9-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fac9-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fac9-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fac9-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fac9-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fac9-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fac9-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fac9-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fac9-115">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7fac9-115">DESCRIPTION</span></span>
<span data-ttu-id="7fac9-116">Il cmdlet **Remove-AzSynapseRoleAssignment** elimina definitivamente un'assegnazione di ruolo di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7fac9-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="7fac9-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fac9-117">EXAMPLES</span></span>

### <span data-ttu-id="7fac9-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7fac9-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="7fac9-119">Questo comando elimina un'assegnazione di ruolo di Azure Synapse Analytics con un ID assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="7fac9-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="7fac9-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7fac9-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="7fac9-121">Questo comando elimina un'assegnazione di ruolo di Azure Synapse Analytics con un nome di ruolo e un nome dell'entità utente.</span><span class="sxs-lookup"><span data-stu-id="7fac9-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="7fac9-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7fac9-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="7fac9-123">Questo comando elimina un'assegnazione di ruolo di Azure Synapse Analytics con un ID assegnazione di ruolo tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="7fac9-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="7fac9-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fac9-124">PARAMETERS</span></span>

### <span data-ttu-id="7fac9-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fac9-125">-AsJob</span></span>
<span data-ttu-id="7fac9-126">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7fac9-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fac9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fac9-127">-DefaultProfile</span></span>
<span data-ttu-id="7fac9-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7fac9-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fac9-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7fac9-129">-ObjectId</span></span>
<span data-ttu-id="7fac9-130">ObjectId di Azure AD dell'utente, del gruppo o dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7fac9-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac9-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fac9-131">-PassThru</span></span>
<span data-ttu-id="7fac9-132">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7fac9-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7fac9-133">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7fac9-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7fac9-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="7fac9-134">-RoleAssignmentId</span></span>
<span data-ttu-id="7fac9-135">ID dell'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="7fac9-135">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac9-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7fac9-136">-RoleDefinitionId</span></span>
<span data-ttu-id="7fac9-137">ID del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="7fac9-137">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac9-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7fac9-138">-RoleDefinitionName</span></span>
<span data-ttu-id="7fac9-139">Nome del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="7fac9-139">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac9-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7fac9-140">-ServicePrincipalName</span></span>
<span data-ttu-id="7fac9-141">ServicePrincipalName dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7fac9-141">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac9-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="7fac9-142">-SignInName</span></span>
<span data-ttu-id="7fac9-143">Indirizzo di posta elettronica o nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7fac9-143">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac9-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7fac9-144">-WorkspaceName</span></span>
<span data-ttu-id="7fac9-145">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="7fac9-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac9-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7fac9-146">-WorkspaceObject</span></span>
<span data-ttu-id="7fac9-147">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="7fac9-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByWorkspaceObjectAndIdParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fac9-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fac9-148">-Confirm</span></span>
<span data-ttu-id="7fac9-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fac9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fac9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fac9-150">-WhatIf</span></span>
<span data-ttu-id="7fac9-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fac9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fac9-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fac9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fac9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fac9-153">CommonParameters</span></span>
<span data-ttu-id="7fac9-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fac9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fac9-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7fac9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fac9-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="7fac9-156">INPUTS</span></span>

### <span data-ttu-id="7fac9-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7fac9-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7fac9-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fac9-158">OUTPUTS</span></span>

### <span data-ttu-id="7fac9-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7fac9-159">System.Boolean</span></span>

## <span data-ttu-id="7fac9-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="7fac9-160">NOTES</span></span>

## <span data-ttu-id="7fac9-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fac9-161">RELATED LINKS</span></span>
